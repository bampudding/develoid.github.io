---
layout: post
title:  "안드로이드 I/O 스케쥴러(Schedulers)"
author: SiRyuA
categories:
- Android
tags:
- Android
- I/O
- Schedulers
---

## I/O 스케쥴러란?
운영체제에서 저장소(Storage)에 파일의 입력과 출력 방식을 관리하는 방식을 말합니다. 스케쥴러 정책에 따라서 성능 및 배터리 효율에 차이가 있습니다.


## I/O 스케쥴러의 공통된 목표
1. 저장소(Storage) 검색의 소요 시간을 최소화 합니다.
2. 특정 프로세서의 I/O 요청의 우선 순위를 지정합니다.
3. 각 실행중인 프로세스에 저장소 대역폭 공유를 제공합니다.
4. 특정 요청에 대해서 특정 기한 전에 동작 될 것을 보장합니다.


## 스케쥴러의 종류
1. CFQ
  * 프로세스 별 I/O 대역 폭을 균등하게 분배하는 것에 맞추어져있음
  * 각 프로세스에 할당되는 시간은 상위 프로세서의 우선순위에 따라 다름
  * 장점
    > * 일반적인 처리량 테스트에서 가장 우수한 성능
    > * 많은 장치에서 안정적
    > * 다양한 저장소에서 성능 발휘
    > * 더 많은 리소스가 필요로한 프로세스는 높은 우선순위 지정가능
  * 단점
    > * I/O 대기시간이 느림
    > * 테스트 및 실제 사용량이 다른 오버 헤드 있음

2. Deadline
  * 서비스 시작 시간을 보장에 맞추어져있음
  * 모든 I/O 작업에 작업 기한을 정함
  * 프로세서 처리 대기열 관리하며, 정렬된 대기열에서 일괄적으로 요청 처리
  * 장점
    > * 주어진 프로세스의 I/O 대기시간을 줄이는데 탁월
    > * 특정 부하 작업에서 CFQ 보다 우수한 성능
    > * 벤치마크에서 잘 수행됨
    > * 스케쥴링 오버 헤드가 낮음
    > * 최신 Linux 커널에서 매우 안정적
  * 단점
    > * CFQ 보다 적은 I/O 처리량
    > * 다른 프로세스보다 I/O 프로세스의 우선 순위를 지정 할 수 없음

3. VR
  * 다른 스케쥴링과 달리, 동기식/비동기식 요청이 별도 처리되지 않음
  * 작업 기한에 대해서 공정하게 균형
  * 장점
    > * 무작위 기록에 좋음
  * 단점
    > * 때로는 불안정하고 신뢰 할 수 없음

4. Noop
  * 들어오는 모든 I/O 요청을 선입 선출 대기열에 삽입 후 병합 구현
  * SSD, Flash Drive 같은 저장장치에서 사용 권장
  * 장점
    > * 낮은 I/O 대기시간, 향상된 응답성
    > * 매우 낮은 스케쥴 오버헤드
    > * 매우 안정적(SSD 의 일부 시스템 기본 값으로 사용됨)
  * 단점
    > * 벤치마크 성능 저하

5. BFQ
  * CFQ 와 달리, 처리시간을 할당하지않고 저장공간을 할당함
  * 할당된 공간이 꽉 찰때까지 프로세스에 부여
  * 읽지 않은 작업에 많은 공간 부여
  * 프로세스에 부여된 공간은 프로세스 동작 시간에 따라 다름
  * 장점
    > * 성능면에서는 CFQ와 일치하는 우수한 I/O 처리량
    > * CFQ 보다 향상된 I/O 대기시간, 향상된 응답성
    > * CFQ 보다 균형이 잘 맞음
    > * 몇몇 커스텀 커널 및 리눅스 배포판에서 기본 값
  * 단점
    > * 벤치마크 성능 좋지 않음, 일부 영역에서 매우 안좋음

6. FIOPS (Fair IOPS)
  * 플래시 기반 저장장치에 대해서 "I/O 검색 시간 없음"을 가정하여 설계되었음
  * 읽기/쓰기의 I/O 비용은 일반적으로 순환 미디어와 다르며, 요청은 요청 크기와 대기 시간이 길고, 높은 처리량은 높으 IOPS 에 따라 달라짐
  * CFQ와 비슷하지만 처리 과정에서 차이가 있음
  * 장점
    > * I/O 대기시간이 좋으며, 일부 벤치마크에서 우수한 성능 발휘
  * 단점
    > * CFQ와 마찬가지로 일부 일정 오버헤드가 있음
    > * 특정 구성에서 버벅이는 문제가 있음
    > * 안정적인 스케쥴러가 아님

7. SIO (Simple I/O)
  * I/O 요청 처리 대기시간을 최소화 하기 위해 최소 오버 헤드를 유지하는 것을 목표로 함
  * 우선 대기열 개념은 없으며, 기본 병합만 함
  * Noop 와 Deadline 사이의 혼합
  * 요청을 재정렬하거나 정렬하지 않음
  * 장점
    > * I/O 대기시간이 매우 짧고 응답성 우수
    > * 매우 안정적
  * 단점
    > * 벤치마크 성능이 떨어짐

8. ROW
  * 모바일 장치의 사용자 경험을 염두하여 개발됨
  * I/O READ 요청을 위주로 맞추어져 있음
  * WRITE 요청에 대한 READ 요청을 하면 READ 대기시간이 크게 감소
  * 장점
    > * 낮은 READ 대기시간, 작업 전환에 대한 응답성
    > * 일반적으로 매우 안정적
  * 단점
    > * 잠재적으로 쓰기 대기시간이 길어 쓰기 성능 감소

9. ZEN
  * Noop, Deadline, SIO 스케쥴러 기반
  * FCFS(First Come First Saves) 기반 알고리즘
  * 어떠한 정렬도 하지 않으며, 공정성을 위해 작업 기한을 사용
  * 비동기 요청보다 우선 순위가 높은 동기 요청을 처리함
  * 이외 Noop 과 VR 을 섞은 것과 거의 같음
  * 장점
    > * I/O 대기시간이 매우 뛰어나 응답성이 좋음
    > * 매우 안정적
    > * 균형이 잘잡혀있음
  * 단점
    > * 스케쥴링 오버헤드가 있지만 CFQ 보다 적음

10. SIOplus
  * SIO 스케쥴러 기반으로 향상시킨 것
  * 동기 읽기에 대한 비동기 읽기를 지정 가능
  * 장점
    > * 특정 작업 부하에서 SIO 보다 향상된 I/O 대기시간
  * 단점
    > * 벤치마크에서 SIO와 거의 동일하게 수행

11. FIFO (First In First Out)
  * 요청이 들어온 순서대로 우선순위를 지정 작업을 처리합니다.
  * 장점
    > * 낮은 I/O 대기시간, 향상된 응답성
    > * 매우 낮은 스케쥴러 오버헤드
    > * 매우 안정적이며 SSD 일부가 시스템 기본값으로 사용함
  * 단점
    > * 벤치마크 성능이 떨어짐

12. Tripndroid
  * Noop, Deadline, VR 에 기반한 I/O 스케쥴러로 최소한의 오버헤드
  * 장점
    > * I/O 대기시간 뛰어남
    > * 응답성이 좋음
    > * 균형이 잘 맞음
  * 단점
    > * CFQ와 마찬가지로 일부 일정 오버헤드가 있음

13. Test
  * 테스트 유틸리티가 추가된 Noop 스케쥴러
  * 테스트 케이스에 따라 특정 요청을 처리하고 그 결과를 에러코드에 따라서 PASS/FAIL 선언할 수 있음
  * 장점
    > * 커널 개발자에게 도움이 됨
  * 단점
    > * Noop 과 동일

14. Maple
  * Zen 및 SIO 기반
  * 별도의 읽기/쓰기 요청과 SIO의 향상된 전/후 요청처리 기능을 갖춘 ZEN 의 선착순 스타일 알고리즘 사용
  * 동기화 되기 전에 비동기 요청을 처리, 쓰기 전에 읽기 요청을 처리하도록 되어있음
  * 파일 복사와 같이 쓰기 작업이 많을 경우 부정적이만, UI 응답성이 향상됨
  * 장치가 대기상태일때 요청 만료 시간을 증가시켜 더 느리게 처리하게 함에 따라 오버헤드가 적음
  * 장점
    > * 모바일 장치를 염두해서 설계
    > * 특정 작업 부하에서 ZEN 보다 향상된 I/O 대기시간
  * 단점
    > * 일부 장치에서 매우 불안정할 수 있음



#### [보다 자세한 I/O스케쥴러 별 설명 보러가기](https://forum.xda-developers.com/showpost.php?p=59289783&postcount=3)


## 참조
[XDA-Developers](https://forum.xda-developers.com/showpost.php?p=59289783&postcount=3)

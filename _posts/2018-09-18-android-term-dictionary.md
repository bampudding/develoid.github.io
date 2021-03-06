---
layout: post
title:  "안드로이드 용어 사전"
author: SiRyuA
categories: Android
tags:
- Android
---

## APK
안드로이드의 어플리케이션 파일 명

## OTA
Over The Air의 약자, 컴퓨터 없이 단말기 상에서 업데이트를 진행하는 기술입니다. 3G/4G/Wi-Fi 등 많은 데이터 통신 수단을 활용하여 해당 기기의 업데이트 파일을 다운로드받아 리커버리로 설치하는 형식입니다.

## Dalvik
레지스터 머신 형태의 (register-based) 가상 머신이다. 적은 메모리 요구 사양에 최적화 되어있으며,
밑에 까린 프로세스 아이솔레이션, 메모리 관리, 스레딩 지원 등 운영 체제의 지원에 의존하나, 여러 개의 달빅 VM인스턴스가 동시에 돌아 갈 수 있다.

## ART
Anroid RunTime의 약자. Dalvik을 개선한 가상 머신이다. 기존 Dalvik 같은 경우 장치에 맞추어서 응용프로그램 실행시 매번 재 컴파일을 하였으나, ART 같은 경우 응용프로그램 설치시 미리 컴파일을 완료 한 뒤 저장하여 사용하는 형식이다.

## 개발자모드
"개발자 옵션"이라고 표기되는 설정의 메뉴창 중 하나. 조금 더 상세하게 시스템을 건들 수 있는 부분 중 하나이다.

## Eclipse(이클립스)
Java 프로그램 개발 도구, 안드로이드 어플리케이션을 제작할때 사용된다.

## Android Studio(안드로이드 스튜디오)
구글에서 만든 안드로이드 어플리케이션 제작 도구

## MIT App Inventor(MIT 앱 인벤터)
MIT에서 만든 그래픽언어기반의 어플리케이션 제작 도구, Eclips나 Android Studio에 비해서 보다 쉽게 다룰수 있다는 장점이 있다. (유치원생들도 다룰수 있는 수준)

## ADB
Android Debugging Bridge의 약자. 컴퓨터와 단말기를 연결하여 단말기를 제어하는 콘솔 프로그램입니다.

## SDK
Software Development Kit의 약자, 말 그대로 스프트웨어 제작 도구 모음이다.

## ADK
Android Open Accessory Development Kit, 안드로이드 액세서리 개발 도구 모음이다.

## PDK
Platform Development Kit의 약자로서, 제조사에 배포되는 플랫폼 제작 도구이다.

## NDK
Native Development Kit의 약자. 안드로이드 애플 리케이션에서 네이티브 코드의 구성요소들을 포함할 수있는 도구모음이다.

## Debugging(디버깅)
기계, 프로그램 등에서 초기에 일어날 수 있는 쉬운 고장과 결함등을 감소시키는 과정

## USB Debugging Mod(USB 디버깅 모드)
ADB·FASTBOOT와 같은 컴퓨터 프로그램을 통하여 단말기 제어시 그 권한을 상승시켜주는 모드입니다.

## Logcat
프로그램이 작동될때 기록이 되는데, 기록을 뽑아서 표시해주는 기능, 오류를 찾기 위해서 많이 사용된다.

## Kernel
컴퓨터 운영체계의 핵심. 기기의 하드웨어 드라이버를 포함하고 있음. 커널은 쉘(shell)과 대비, 셀은 운영체계의 가장 바깥 부분에 위치, 사용자의 명령에 대한 처리담당, 커널은 입출력연산 등 커널 서비스를 경쟁적 요구하는 모든 요청 처리하는 인터럽트 처리기, 어떤 프로그램들을 어떤 순서로 커널 처리 시간을 공휴 할 것인지 결정하는 스케쥴러, 스케줄이 끝나면 실제로 각 프로세스들에게 컴퓨터 사용권을 부여하는 슈퍼바이저(supervisor)등 포함되어있음. 커널은 메모리/저장장치 내 운영체계의 주소공간 관리, 이를 주변 장치들과 커널서비스 사용하는 다른 사용자에게 분배하는 메모리관리자를 가지고 있음. 커널 서비스는 운영체계의 다른 부분, 또는 프로그램 인터페이스들을 통해 요청됨. HW와 SW를 이어주는 다리라고 생각하면 편하며, 모든 전자제품에서의 핵심이다. 사용자가 자신의 목적에 맞추어 개량한 커스텀 커널도 있다.

## Bootloader(부트로더)
Boot - 컴퓨터 시스템을 시동하거나 초기화 시키는 것
Loader - 불러오는 장비
말 그대로 시스템을 부팅시키기 위한 영역입니다. 하드웨어가 먼저 시동되면 부트로더가 실행되어서 다음 시스템을 불러옵니다. 대다수 안드로이드 스마트폰에서는 부트로더가 잠겨있는데 이 부트로더를 여는 행위를 흔히 언락이라고 한다. 안드로이드 부트로더가 불러오는 것은 커널과 리커버리가 있습니다.

## Fastboot(패스트 부트)
USB를 통해 호스트로부터 안드로이드 기기에서 플래시 파일 시스템을 업데이트 하는데 사용되는 프로토콜

## Recovery (리커버리)
리커버리 - 장해회복처리
리커버리모드 - 장해 회복 처리 담당 모드, 즉 복구모드.
리커버리는 시스템을 부팅시키기 이전에 전반적으로, 시스템을 수정·백업·복구·캐시제거 등을 할 수 있는 관리도구, 흔히 이 모드를 사용하여 시스템에 오류가 발생하였을시 공장초기화 등으로 복구 할 수 있습니다. 또한 시스템을 업데이트 시, 해당 모드로 업데이트 파일을 설치하는 식으로 수정하여 업데이트합니다. 커스텀 리커버리는 기본 리커버리의 기능을 응용하여, 롬/커스텀펌웨어(이후 설명)를 설치 할 수 있도록 개량한 리커버리입니다. 대표적으로 CWM(Clock Work Mod), TWRP(TEAM WIN Recovery Project), 4eXT Recovery가 있습니다.

## Download Mode(다운로드모드)
스마트폰에서 컴퓨터와 연결하여 롬/펌웨어를 입히기 위해 대기하는 모드, 제조사별로 있으며, 조금식 다르다. 삼성에서는 Odin, LG에서는 KDZ와 ToT, HTC에서는 RUU등 다양하게 존재하며 다운로드 모드에서는 해당 펌웨어를 전송받아 설치를 한다.

## Partition(파티션)
컴퓨터에서 디스크나 메모리 등의 저장 매체를 나누는 것, 안드로이드에서는 System, Data, Boot, EFS 등 많은 영역으로 나누어져 있다.

## 시스템 파티션(System Partition)
롬/펌웨어의 프로그램 및 보조 자료들을 가지고 있는 영역입니다.

## 부트 파티션(Boot Partition)
부트로더, 커널 등을 가지고 있는 영역입니다.

## 리커버리 파티션(Recovery Partition)
리커버리 모드를 가지고 있는 영역입니다.

## 데이터 파티션(Data Partition)
사용자가 설치한 어플이나 사용자의 개인 파일등을 가지고 있는 영역입니다.

## EFS
Encrypting File System의 약자. 파일이나 폴더가 암호 형태로 저장되고 개인 사용자와 인가된 에이전트만 해독 할 수 있도록 된 암호화 기법. 스마트폰에서는 IMEI를 저장하는 파티션 영역을 칭하는 말이다.
이 부분에 문제가 생기면 스마트폰에서 IMEI가 사라지거나 통신이 안되는 현상이 발생된다.

## SU
Super User의 약자. Linux 제품군에서 최고 관리자 권한으로서 윈도우의 Administrator 권한이랑 비슷하다. 일반 사용자에게는 주어지지 않는 사용자 등록, 삭제, 시스템 수정, 기기 정지등의 작업이 가능하다.

## SU Binary
su권한 명령을 가진 파일을 말합니다. 부트로더 경로인 /system/bin/에 주입하여 사용되며 슈퍼유저 권한 부여시 사용됩니다

## Rooting(루팅)
제조사에서 막아둔 최고관리자 권한을 획득하는 행위

## Busy Box(비지박스)
리눅스 확장 명령어 묶음입니다. /mount, /umount 등 많은 명령어를 가지고 있으며, /system/bin에 주입하여 사용됩니다.

## Wipe(와이프)
system, data, cache, Dalvik Cache 등의 영역을 초기화 하는 행위를 말합니다.

## Flashing(플래싱)
리커버리에서 zip형태의 설치 파일통해 파일을 스마트폰에 설치하는 행위를 말합니다.

## Factory Reset(팩토리리셋/공장초기화)
시스템을 초기 상태로 되돌리는 행위를 말합니다. 리커버리나 시스템을 통해서 가능합니다.

## Cache
주 기억장치에 읽어들인 명령이나 프로그램들로 채워지는 버퍼 형태의 고속 기억 장치.
사람으로 비유하면 기억이라고 할 수 있다. 프로그램이나 데이터를 블록 단위로 불러와서 실행한다.

## Dalvik Cache
안드로이드의 어플리케이션은 자바로 작성됩니다. 그리고 자바로 작성된 모든 프로그램은 자바 가상머신이 필요로합니다. 안드로이드에는 가상머신으로 작동 된 어플리케이션을 나중에 더욱 더 빠르게 수행하기 위해 최적화 분석정보를 캐시로 작성하여 저장합니다. 달빅캐시는 가상머신을 빠르게 돌리기 위해 저장해놓은 캐시입니다.

## Framework(프레임워크)
복잡한 문제를 해결하거나 서술하는 데 사용하는 기본 개념 구조, 소프트웨어 패키지를 말한다.

## Stock(스톡/순정)
순정상태, 즉 제조사에서 만들어놓은 아무것도 안 건든 펌웨어를 말한다.

## Custom ROM(커스텀 롬)
사용자가 사용자의 편의성에 맞추어서 수정해놓은 펌웨어를 말한다. 대표적으로 CM(Cyanogen Mod), AOKP(Android Open Kang Project), Paranoid Android, Omni 등이 있습니다.

## Firmware(펌웨어)
하드웨어 및 소프트웨어를 종합적으로 관리, 제어하는 기본 소프트웨어입니다.

## Mod(모드)
유저가 만든 기능 또는 테마 어플 패키지 등을 말합니다.

## 벽돌
Rooting, Custom ROM 설치 하다가 무한 재부팅 현상이 발생하거나 조작이 불가능해진 상황의 기기

## 하드브릭
잘못된 커널이나 패치, 리파티션, 다운로드모드를 통한 순정 복구 등을 적용하다가 시스템의 파티션이 조각나거나 삭제되어서 발생하는 현상입니다. 이 경우 스마트폰이 켜지지 않거나, 컴퓨터 등의 호스트랑 연결했을때 아무런 연결이 뜨지 않는 경우입니다. 내부 시스템적으로 손상이 생겨서 단순히 PC만으로는 복구가 불가능하며 J-Tag를 필요로 합니다. 일부 제품에서는 단순히 PC만으로도 쉽게 복구 가능하다고 합니다.

## 소프트브릭
커스텀 롬이나 커널등을 잘 못 올렸을때 발생하는 현상입니다. 부트로더와 리커버리가 이상이 없으므로 다른 파일로 교체하여 설치하는 등 비교적 쉽게 복구 가능합니다.

## J-Tag
메인보드에 직접 꼽아서 사용하는 디버깅 도구입니다. USB보다 높은 개념입니다.

## Force Close(FC)
어플리케이션 강제 종료시 뜨는 에러코드 명입니다. 소프트웨어적으로 이상이 있을 시에만 나타납니다.

## Mount(마운트)
system, data 영역 등을 사용하기 위해서 연결하는 것을 말합니다. 연결을 끊을 시엔 Unmount(언마운트)라고 합니다.

## Boot Loop(무한부팅)
다양한 오류로 인하여 계속 스마트폰이 켜졋다가 다시 꺼지고 다시 부팅하는 현상을 말한다.

## Freezing(프리징)
말 그대로 스마트폰이 아무런 동작이 되지않고 얼어붙어버리는 현상을 말한다.

## Process(프로세스)
의도하는 목적 또는 효과에 따라 발생하는 사상의 과정, 어느 결과를 얻기 위해서 필요한 일련의 계통적인 동작태스크(task)와 같은 뜻으로 사용되는 경우가 있으며 여러 프로그램을 병행하여 실행하는
다중 프로그래밍(multiprogramming)을 행하는 기본적인 프로그램 단위라는 의미

## Rendering(랜더링)
2차원의 화상에 광원·위치·색상 등 외부의 정보를 고려하여 사실감을 불어넣어, 3차원 화상을 만드는 과정

## Reference Device(레퍼런스 디바이스)
구글에서 설계 및 SW를 담당하고 HW는 제조사에서 만드는 안드로이드 개발 메인 기기를 말한다.
Nexus 시리즈가 그 대표적인 예이다.

## Libraries(라이브러리)
컴퓨터 프로그램에서 자주 사용되는 부분 프로그램들을 모아놓은 것 입니다.
안드로이드에서는 NDK로 C/C++을 이용하여 개발합니다.

## OpenGL
2D와 3D를 정의한 컴퓨터 산업 표준 응용 프로그램 인터페이스 그래픽 관련 라이브러리 뭉치이다.

## SQLite
데이터베이스 관리 라이브러리입니다.

## Webkit(웹킷)
웹 브라우징을 위한 라이브러리 입니다.

## KDZ
LG의 펌웨어 복구 프로그램 입니다.

## ToT
LG의 펌웨어 복구 프로그램 입니다. KDZ보다 높은 개념입니다.

## Odin(오딘)
삼성의 펌웨어 복구 프로그램 입니다.

## RUU(루)
HTC의 펌웨어 복구 프로그램 입니다.
HTC 같은 경우 정말 극심한 하드브릭 이외에는 이 파일로 전부 복구 가능하다는 말이 있습니다.

## Binx
Vega(Pantech)의 펌웨어 복구 프로그램 입니다.

## SBF
모토로라의 펌웨어 복구 프로그램 입니다.

## RSD Lite
모토로라의 펌웨어 플래싱 프로그램입니다.

## Pit
삼성 제품군의 파티션 영역의 크기를 설정해놓은 파일입니다.

## AOSP
Android Open Source Project의 약자입니다.
구글에서 제공하는 안드로이드 소스이며, 롬/펌웨어 제작의 초석이 됩니다.

## Xposed
Xposed Framework를 칭한다. 사용자가 시스템을 수정하지 않고 기능이 담겨진 모듈등을 추가하여 사용 할 수 있도록 제작된 프레임워크이다. 정말 많은 모듈 파일이 존재하며 기존 시스템의 기능을 사용하면서 다른 기능들을 추가 할 수 있다는 장점이 있다.

## 가용램
사용이 가능한 램 메모리를 말한다. 가용램이 부족할수록 스마트폰은 버벅거리며 느려진다.

## Scaling Governor(가버너)
CPU 또는 GPU의 연산 처리시 클럭 동작 방식을 말합니다.

## APKTool
안드로이드 어플리케이션 파일인 APK를 디컴파일하여, 즉 분해하여 수정 할 수 있도록 제작된 프로그램이다.

## Cooking(쿠킹)
유저가 제조사에서 기본적으로 제공된 펌웨어나, 타 유자가 만든 롬/펌웨어를
자신의 목적에 맞추어서 수정하는 행위를 말합니다. 해당 행위를 전문적으로 하는 유저를 쿠커(Cooker)라고 부릅니다.

## Building(빌딩)
유저가 직접 안드로이드 소스를 다운로드 받아서 빌드(제작)하는 행위를 말합니다. 직접 다운로드 받은 소스 그 상태로 컴파일(제작)을 할 수도 있으며, 소스를 자신의 목적에 맞추어서 롬/펌웨어를 제작 할 수도 있습니다.

## Kang(캉)
안드로이드 소스를 자신의 목적에 맞추어서 수정하는 행위를 말합니다.

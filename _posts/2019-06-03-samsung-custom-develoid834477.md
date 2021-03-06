---
layout: post
title: '주요 기종의 통신사 펌웨어 변경 방법'
author: 'HD Voice'
categories: Samsung-Custom
tags:
- Samsung
- Device
- Custom
-
---


<p>안녕하세요 Android Pay (HD Voice) 입니다!</p>
<p>주요 기종의 통신사 펌웨어 변경 방법을 하나의 글로 통합해서 올립니다</p>
<p>녹스 보호하고 싶으시면 OEM 잠금해제는 하지 마시고 구글 계정은 그대로 두세요</p>
<p>다운로드 화면에서</p>
<p>OEM LOCK: ON</p>
<p>FRP LOCK: ON</p>
<p>이라고 뜨면 녹스는 이중으로 보호되는 상태입니다.</p>
<p>-</p>
<p>공통 사항</p>
<p>1번과 3번 방법을 제외하고 부트로더가 업데이트 될 경우 이 방법은 몇달간 막히게 됩니다</p>
<p>OTA 업데이트 할때 확인하세요!</p>
<p>스마트 스위치가 설치되어 있어야 합니다</p>
<p>오딘 v3.13.1과 SamFirm v0.3.6도 있어야 합니다</p>
<p>꼭 압축 푸세요</p>
<p>4번 방법은 RealTerm도 설치되어 있어야 합니다</p>
<p>당연히 데이터는 날라가니 완전히 백업하셔야 하구요!</p>
<p>각종 프로그램 다운로드 링크</p>
<p><a href="https://forum.xda-developers.com/galaxy-tab-s/general/tool-samfirm-samsung-firmware-t2988647">https://forum.xda-developers.com/galaxy-tab-s/general/tool-samfirm-samsung-firmware-t2988647</a></p>
<p>(SamFirm)</p>
<p><a href="https://forum.xda-developers.com/galaxy-s8+/how-to/guide-flash-oreo-g955fxxu1crb7-using-t3755789">https://forum.xda-developers.com/galaxy-s8+/how-to/guide-flash-oreo-g955fxxu1crb7-using-t3755789</a></p>
<p>(Odin v3.13.1)</p>
<p><a href="https://www.samsung.com/sec/support/smartswitch/">https://www.samsung.com/sec/support/smartswitch/</a></p>
<p>(Smart Switch)</p>
<p><a href="https://sourceforge.net/projects/realterm/">https://sourceforge.net/projects/realterm/</a></p>
<p>(RealTerm)</p>
<p>오딘에서 Start를 눌렀을때 FAIL이 뜬다면</p>
<p>Options 탭에서 Re-Partition이 선택되어 있다면 해제하고 다운로드 모드 나갔다 다시 들어오시구요</p>
<p>만약 아니라면 스마트 스위치를 실행해서 업데이트 하고 USB 드라이버 재설치 과정을 밟고</p>
<p>기기를 다시 뺐다 연결하고 다운로드 모드 나갔다 다시 진입하세요</p>
<p>그래도 안되면 그건 정품 케이블이 아니거나 다운로드 모드 진입하신게 아닌겁니다</p>
<p>SKT 유심 사용자의 경우 교통카드 사용 불가시 해결법입니다</p>
<p>캐시비는 거의 안될겁니다 아마</p>
<p>우선 SKT에서 출고된 폰을 가지고 계셔야 되요! (아이폰 등 외산폰 빼고 삼성 LG 다 되요)</p>
<p>현재 쓰고 있는 기기는 데이터 끄고 와이파이만 키셔야 되요</p>
<p>1. 현재 쓰고 있는 기기(이하 현폰)에서 유심을 뽑고 SKT 출고폰(이하 SK폰)으로 옮깁니다</p>
<p>2. 기변 문자가 올거에요 SK폰에서 데이터 켜고 모바일 티머니 앱을 설치하고 정상적으로 실행 시키고 그 상태에서 현폰으로 옮깁니다</p>
<p>3. 이제 SK폰에서 현폰으로 유심을 다시 옮기고 와이파이만 켜서 모바일 티머니 앱을 설치하고 정상적으로 실행시켜요</p>
<p>4. 그리고 재부팅 하시면 이제 모바일 티머니 앱도 되고 모바일 캐시비 앱도 되고 삼성 페이 교통카드 (티머니/캐시비)도 다 됩니다!!</p>
<p>-</p>
<p>1번</p>
<p>그냥 오딘으로 타 통신사 펌웨어 올리기</p>
<p>S7/S7+, 노트 FE, A5 2017, J5 2017 기기용</p>
<p>완벽히 바뀌나 일부 기기는 메인보드가 고장나버리는 경우도 발생하였으며 성공하여도 모델명이 달라 A/S 거부될수 있습니다</p>
<p>순정펌은 SamFirm으로 받을수 있고 사용법은 간단합니다</p>
<p>원 통신사의 순정펌(비상시 복원용)과 변경하고 싶은 통신사의 순정펌 둘다 받으세요</p>
<p>Model에 입력할 문구는</p>
<p>S7 기기는 "SM-G930X"</p>
<p>S7 기기는 "SM-G935X"</p>
<p>노트 FE 기기는 "SM-N935X"</p>
<p>A5 2017 기기는 "SM-A520X"</p>
<p>J5 2017 기기는 "SM-J530X"</p>
<p>이며 끝 부분 X는</p>
<p>SKT 기기는 "S"</p>
<p>KT 기기는 "K"</p>
<p>LG U+ 기기는 "L"</p>
<p>입력하셔야 합니다</p>
<p>Region에 입력할 문구는</p>
<p>SKT 기기는 SKC</p>
<p>KT 기기는 KTC</p>
<p>LG U+ 기기는 LUC</p>
<p>입니다</p>
<p>순정펌 압축 풀어주시구요</p>
<p>1. 폰 전원 끄고 다운로드 모드 진입을 위해 볼륨 다운+홈+전원 누르고 경고문이 뜨면 볼륨 업 누르시고 기기를 컴퓨터에 연결해주세요</p>
<p>그리고 오딘 실행해서 각 4개 파일을 맞는 슬롯에 AP BL CP CSC 넣어주시구요 (HOME_CSC 제외)</p>
<p>Start 눌러주세요</p>
<p>2. PASS 뜨고 부팅되면 초기 설정 해주시구요</p>
<p>찝찝하시면 설정 앱 내에서 전체 초기화 돌리시면 됩니다</p>
<p>끝!</p>
<p>-</p>
<p>2번</p>
<p>COMBINATION 롬으로 변경하기</p>
<p>노트 8(부트로더 4), A8 2018(부트로더 2) 기기용</p>
<p>상당히 간편하고 빠르며 안전하고 완벽히 바뀝니다</p>
<p>받아야 할 자료</p>
<p><a href="https://drive.google.com/file/d/11YLQzMj-DwBH7SMv0wbO6Drt3m51I-3O/view">https://drive.google.com/file/d/11YLQzMj-DwBH7SMv0wbO6Drt3m51I-3O/view</a></p>
<p>NOTE 8 N950N COMBINATION BOOTLOADER 4 ONLY</p>
<p><a href="https://mshare.io/file/Bt4dffFI">https://mshare.io/file/Bt4dffFI</a></p>
<p>A8 2018 A530N COMBINATION BOOTLOADER 2 ONLY</p>
<p>순정펌은 SamFirm으로 받을수 있고 사용법은 간단합니다</p>
<p>원 통신사의 순정펌(비상시 복원용)과 변경하고 싶은 통신사의 순정펌 둘다 받으세요</p>
<p>Model에 입력할 문구는</p>
<p>노트 8 기기는 "SM-N950N"</p>
<p>A8 2018 기기는 "SM-A530N"</p>
<p>이며 Region에 입력할 문구는</p>
<p>SKT 기기는 SKC</p>
<p>KT 기기는 KTC</p>
<p>LG U+ 기기는 LUC</p>
<p>입니다</p>
<p>순정펌 압축 풀어주시구요</p>
<p>1. 폰 전원 끄고 다운로드 모드 진입을 위해</p>
<p>노트 8은 볼륨 다운+빅스비+전원 누르고 경고문이 뜨면 볼륨 업 누르시고</p>
<p>A8 2018은 볼륨 다운+볼륨 업+전원 누르고 경고문이 뜨면 볼륨 업 누르시고</p>
<p>기기를 컴퓨터에 연결해주세요</p>
<p>그리고 오딘 실행해서 AP 슬롯에 COMBINATION 파일 넣어주시구요</p>
<p>Start 눌러주세요</p>
<p>2. PASS 뜨고 부팅되면 모델명이 뜰겁니다</p>
<p>끄고 다시 1번처럼 다운로드 모드 진입하시고 CSC 슬롯에 다운 받은 순정펌에 들어있는 HOME_CSC 파일 넣어주시구요</p>
<p>Start 눌러주세요</p>
<p>3. 밑에 IME 누르시고 *#243203855# 입력하시구요</p>
<p>변경하고 싶은 통신사의 CSC를 선택하시고 밑에 INSTALL 선택하시고 FULL CUSTOMIZATION 선택하셔야 되요</p>
<p>SKT는 SKC</p>
<p>KT는 KTC</p>
<p>LG U+는 LUC</p>
<p>이고 선택하면 자동 재부팅이 될거고 다시 부팅되면 다운로드 모드 오시구요</p>
<p>이상한 검은 화면에 빨간 글씨 뜨면서 아무것도 안되면 전원+볼륨 다운 7초 누르시고 꺼지는 즉시 다운로드 모드 오세요</p>
<p>4. 그리고 오딘 실행해서 지금 막 변경한 통신사 순정펌의 각 5개 파일을 맞는 슬롯에 AP BL CP CSC USERDATA 넣어주시구요 (HOME_CSC 제외)</p>
<p>Start 눌러주세요</p>
<p>5. PASS 뜨고 부팅되면 초기 설정 해주시구요</p>
<p>찝찝하시면 설정 앱 내에서 전체 초기화 돌리시면 됩니다</p>
<p>끝!</p>
<p>-</p>
<p>3번</p>
<p>시우연우파파님 방식 변경 방법</p>
<p>S8/S8+, 노트 8, A8 2018 기기용</p>
<p>부트로더 업데이트와 무관하게 언제든지 안전하게 변경 가능</p>
<p><a href="http://siwooyeonwoopapa.tistory.com/entry/%EA%B0%A4%EB%9F%AD%EC%8B%9C-S8-%EB%85%B8%ED%8A%B88-A8-2018-%ED%86%B5%EC%8B%A0%EC%82%AC-%EB%B3%80%EA%B2%BD%EB%B0%A9%EB%B2%95?category=663003">http://siwooyeonwoopapa.tistory.com/entry/%EA%B0%A4%EB%9F%AD%EC%8B%9C-S8-%EB%85%B8%ED%8A%B88-A8-2018-%ED%86%B5%EC%8B%A0%EC%82%AC-%EB%B3%80%EA%B2%BD%EB%B0%A9%EB%B2%95?category=663003</a></p>
<p><a href="http://siwooyeonwoopapa.tistory.com/entry/%EA%B0%A4%EB%9F%AD%EC%8B%9C-8%EC%84%B8%EB%8C%80-%EA%B8%B0%EA%B8%B0-%ED%86%B5%EC%8B%A0%EC%82%AC-%EB%B3%80%EA%B2%BD%EB%B2%95-S8-Note8-A8%EC%82%AC%EC%A7%84%ED%8F%AC%ED%95%A8-%EC%83%81%EC%84%B8%ED%95%98%EA%B2%8C-%EC%84%A4%EB%AA%85?category=663003">http://siwooyeonwoopapa.tistory.com/entry/%EA%B0%A4%EB%9F%AD%EC%8B%9C-8%EC%84%B8%EB%8C%80-%EA%B8%B0%EA%B8%B0-%ED%86%B5%EC%8B%A0%EC%82%AC-%EB%B3%80%EA%B2%BD%EB%B2%95-S8-Note8-A8%EC%82%AC%EC%A7%84%ED%8F%AC%ED%95%A8-%EC%83%81%EC%84%B8%ED%95%98%EA%B2%8C-%EC%84%A4%EB%AA%85?category=663003</a></p>
<p>자세한 변경 방법은 링크 참고 부탁드리며 일부 기기는 설정 앱에서 두 통신사 특화 설정이 뜰수 있습니다</p>
<p>찝찝하시면 설정 앱 내에서 전체 초기화 돌리시면 됩니다</p>
<p>끝!</p>
<p>-</p>
<p>4번</p>
<p>제 방식 변경 방법</p>
<p>S8/S8+, S9/S9+, 노트 9</p>
<p>변경 방법은 간편하고 빠르나 RealTerm 사용할때 잘 안된다며 마우스 클릭 난사하거나 중간에 선 뽑으시면 안됩니다</p>
<p>받아야 할 자료</p>
<p><a href="https://1drv.ms/u/s!AoZnUu8keuApitsgaofGhCM1CMMNOA">https://1drv.ms/u/s!AoZnUu8keuApitsgaofGhCM1CMMNOA</a></p>
<p>S8 G950N COMBINATION BOOTLOADER 3 ONLY</p>
<p><a href="https://1drv.ms/u/s!AoZnUu8keuApitshUAPBmkQPpvG9vw">https://1drv.ms/u/s!AoZnUu8keuApitshUAPBmkQPpvG9vw</a></p>
<p>S8+ G955N COMBINATION BOOTLOADER 3 ONLY</p>
<p><a href="https://1drv.ms/u/s!AoZnUu8keuApitsN0CW5aDamkoqiRw">https://1drv.ms/u/s!AoZnUu8keuApitsN0CW5aDamkoqiRw</a></p>
<p>S9 G960N COMBINATION BOOTLOADER 1 ONLY</p>
<p><a href="https://1drv.ms/u/s!AoZnUu8keuApitoSaDbbUorjYcFOcg">https://1drv.ms/u/s!AoZnUu8keuApitoSaDbbUorjYcFOcg</a></p>
<p>S9+ G965N COMBINATION BOOTLOADER 1 ONLY</p>
<p><a href="https://1drv.ms/u/s!AoZnUu8keuApittWwwl5wIJI8WEa_Q">https://1drv.ms/u/s!AoZnUu8keuApittWwwl5wIJI8WEa_Q</a></p>
<p>NOTE 9 N960N COMBINATION BOOTLOADER 2 ONLY</p>
<p>순정펌은 SamFirm으로 받을수 있고 사용법은 간단합니다</p>
<p>원 통신사의 순정펌(비상시 복원용)과 변경하고 싶은 통신사의 순정펌 둘다 받으세요</p>
<p>Model에 입력할 문구는</p>
<p>S8 기기는 "SM-G950N"</p>
<p>S8+ 기기는 "SM-G955N"</p>
<p>S9 기기는 "SM-G960N"</p>
<p>S9+ 기기는 "SM-G965N"</p>
<p>노트 9 기기는 "SM-N960N"</p>
<p>이며 Region에 입력할 문구는</p>
<p>SKT 기기는 SKC</p>
<p>KT 기기는 KTC</p>
<p>LG U+ 기기는 LUC</p>
<p>입니다</p>
<p>순정펌 압축 풀어주시구요</p>
<p>1. 폰 전원 끄고 다운로드 모드 진입을 위해</p>
<p>S8/S8+, S9/S9+ 기기는 볼륨 다운+빅스비+전원 누르고 경고문이 뜨면 볼륨 업 누르시고</p>
<p>노트 9 기기는 USB 빼고 볼륨 다운+빅스비 누른 상태에서 USB 연결하고 경고문이 뜨면 볼륨 업 누르시고</p>
<p>기기를 컴퓨터에 연결해주세요</p>
<p>그리고 오딘 실행해서 AP 슬롯에 COMBINATION 파일 넣어주시구요</p>
<p>Start 눌러주세요</p>
<p>2. PASS 뜨고 부팅되면 모델명이 뜰겁니다</p>
<p>이제 RealTerm을 실행하세요</p>
<p>(RealTerm만 실행하세요 RealTerm 옆에 다른 이름이 붙은 프로그램은 실행하시면 안됩니다)</p>
<p>그리고 Port 탭으로 가세요</p>
<p>Baud를 230400으로 맞추시고 Port 선택란을 열어서 ssudmdm0000 또는 그와 매우 비슷한것을 선택하세요</p>
<p>그리고 오른쪽에 Status에서 2개 또는 3개가 초록색으로 변할때 까지 Open을 누르세요</p>
<p>Send로 가고 첫번째 줄에 AT를 입력하고 Send ASCII를 누르세요</p>
<p>3. 4가지 유형 중 하나로 회신이 올겁니다</p>
<p>(간혹 순정펌에서 AT라고 뜨며 회신이 오는 경우가 있지만 확인과 변경은 불가능합니다)</p>
<p>1번 (정상)</p>
<p>+USB&nbsp; READY</p>
<p>BOOTING COMPLETED</p>
<p>AT</p>
<p>2번 (정상)</p>
<p>AT</p>
<p>3번 (정상)</p>
<p>OK</p>
<p>4번 (정상)</p>
<p>BOOTING COMPLETED</p>
<p>AT</p>
<p>5번 (확인 필요)</p>
<p>아무 응답 없음</p>
<p>1번 2번 3번 4번은 다음으로 넘어가시구요</p>
<p>5번은 연결이 제대로 되지 않았거나 화면을 꺼서 그럴수 있습니다</p>
<p>만약 다 제대로 했다면 EOL에서 +CR를 누르고 다시 발송해보세요</p>
<p>ERROR라고 뜬다면 정상이며 다음 단계로 넘어가시면 됩니다</p>
<p>만약 그래도 아무것도 안뜬다면 다음 단계로 넘어가고 그래도 안뜨면 다시 진행하세요</p>
<p>4. AT+PRECONFG=1,0 전송하세요</p>
<p>다음과 같이 회신이 옵니다</p>
<p>AT+PRECONFIG=1,0+PRECONFG:1,XXX</p>
<p>OK</p>
<p>(XXX는 현 CSC입니다)</p>
<p>5. AT+PRECONFG=2,XXX 전송하세요</p>
<p>XXX는 변경할 통신사이며 변경하고 싶은 통신사의 CSC를 입력하셔야 합니다</p>
<p>SKC는 SKT</p>
<p>KTC는 KT</p>
<p>LUC는 LG U+</p>
<p>KOO는 자급제</p>
<p>복원할때도 이렇게 하시면 됩니다</p>
<p>회신은 다음과 같이 옵니다</p>
<p>AT+PRECONFG=2,XXX+PRECONFG:2,OK</p>
<p>OK</p>
<p>(XXX는 바뀐 CSC입니다)</p>
<p>6. 다시 AT+PRECONFG=1,0 전송하세요</p>
<p>회신은 다음 두가지 유형 중 하나로 옵니다</p>
<p>1번</p>
<p>AT+PRECONFIG=1,0+PRECONFG:1,XXX+PRECO</p>
<p>OK</p>
<p>2번</p>
<p>AT+PRECONFIG=1,0+PRECONFG:1,XXX</p>
<p>OK</p>
<p>(XXX는 현 CSC입니다)</p>
<p>7. 그리고 오딘 실행해서 지금 막 변경한 통신사 순정펌의 각 5개 파일을 맞는 슬롯에 AP BL CP CSC USERDATA 넣어주시구요 (HOME_CSC 제외)</p>
<p>Start 눌러주세요</p>
<p>8. PASS 뜨고 부팅되면 초기 설정 해주시구요</p>
<p>찝찝하시면 설정 앱 내에서 전체 초기화 돌리시면 됩니다</p>
<p>끝!</p>
<p>-</p>
<p>끝났습니다 감사합니다 수고하셨습니다</p>

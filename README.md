## dandoor_ble

# 목표

- 블루투스를 이용해서 2차원 위치 추정하기
- 추정한 위치를 시각화하기
- 위치 정확도 도출하기

# 구현 방법

1. 핸드폰(스캐너)이 주변 nrf5340-dk(에드버타이저)를 감지하여 rssi 값을 수신
3. 측정된 rssi를 서버로 송신 
4. 받은 {devicename, rssi, macAddress}를 csv로 저장
5. ***를 이용해서 시각화

# RSSI 탐색 앱
6초에 한번씩 스캔을 시도하여 끊임없이 스캔을 시도한다.

구현된 기능
  1. updateLog()를 통한 TextView에 rssi 로그를 업데이트 하는 기능
     
추가적으로 필요한 기능
  1. scanFilters를 활용한 특정 장치만 스캔하는 기능
  2. 입력을 받아서 scanFilters에 추가하는 기능
  3. 서버 IP를 통해 데이터를 전송하는 기능

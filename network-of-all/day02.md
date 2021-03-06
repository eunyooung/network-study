# Network of All - DAY 2

## **Lesson 6 (네트워크의 규칙)**
- **프로토콜**: 통신하기 위한 규칙
    - 예1) 불어를 못하는 한국인과 한국어를 못하는 프랑스인이라면 영어로 대화한다는 규칙을 정해서 대화
    - 예2) 편지를 보낼 때 편지를 쓸 때부터 상대방에게 도착하기 까지 지켜야하는 독릭적인 여러 규칙을 거쳐야함

## **Lesson 7 (OSI 모델과 TCP/IP 모델)**
- **ISO(International Organization for Standardiation)**: 국제 표준화기구
- **OSI 모델**: ISO가 제정한 네트워크 기술의 기본이 되는 모델이며 데이터 송수신을 일곱개 계층으로 나눔.
    |계층|이름|설명|
    |:---:|:---:|:---|
    |7계층|응용 계층</br>(Application Layer, 애플리케이션 계층)|이메일 & 파일 전송, 웹사이트 조회 등 애플리케이션에 대한 서비스를 제공|
    |6계층|표현 계층</br>(Presentation Layer, 프레젠테이션 계층)|문자 코드, 압축, 암호화 등의 데이터를 변환|
    |5계층|세션 계층</br>(Session Layer)|세션 체결, 통신 방식을 결정|
    |4계층|전송 계층</br>(Transport Layer, 트랜스포트 계층)|신뢰할 수 있는 통신을 구현|
    |3계층|네트워크 계층</br>(Network Layer)|다른 네트워크와 통신하기 위한 경로 설정 및 논리 주소를 결정|
    |2계층|데이터 링크 계층</br>(Data Link Layer)|네트워크 기기 간의 데이터 전송 및 물리 주소를 결정|
    |1계층|물리 계층</br>(Physical Layer)|시스템 간의 물리적인 연결과 전기 신호를 변환 및 제어|
- **데이터 송신**: 상위 계층에서 하위 계층으로 데이터를 전달
- **데이터 수신**: 하위 계층에서 상위 계층으로 전달된 데이터를 받음
- 각 계층은 독릭적이므로 데이터가 전달되는 동안 다른 계층의 영향을 받지 않음
- **TCP/IP 모델**
    |**TCP/IP 모델**|
    |:---:|
    |응용계층|
    |전송 계층|
    |인터넷 계층|
    |네트워크 접속 계층|
- **OSI 모델**과 **TCP/IP 모델** 비교
    |**OSI 모델**|**TCP/IP 모델**|
    |:---:|:---:|
    |응용 계층|응용 계층|
    |표현 계층|응용 계층|
    |세션 계층|응용 계층|
    |전송 계층|전송 계층|
    |네트워크 계층|인터넷 계층|
    |데이터링크 계층|네트워크 접속 계층|
    |물리 계층|네트워크 접속 계층|

## **Lesson 8 (캡슐화와 역캡슐화)**
- **헤더**: 데이터에 추가한 데이터를 전송할 때 필요한 정보
- **트레일러**: 데이터를 전달할 때 데이터 마지막에 추가하는 정보
- **캡슐화**: 데이터 송신시 헤더를 붙혀 나가는 것
    - **(1)응용 계층 -> (2)전송 계층 -> (3)네트워크 계층 -> (4)데이터 링크 계층**
    - (1): 웹사이트를 접속하기 위한 요청 데이터
    - (2): 신뢰할 수 있는 통신을 구현하는 헤더를 데이터에 붙힘
    - (3): 다른 네트워크와 통신하는 헤더를 데이터에 붙힘
    - (4): 물리적인 통신 채널을 연결하기 위해 헤더와 트레일러를 데이터에 붙힘
- **역캡슐화**: 데이터 수신시 헤더를 제거해 나가는 것
    - 데이터 링크 계층 -> 네트워크 계층 -> 전송 계층 -> 응용 계층
- 송신측 데이터 링크 계층에서 만들어진 데이터는 최종적으로 **전기 신호**로 변환돼서 수신측에 도착
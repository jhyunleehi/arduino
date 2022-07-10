

# 기후 위기 대응

[![스스로 멸먕의 길을 걷는 인류](https://user-images.githubusercontent.com/13324737/178131419-54e8ff76-b405-4a2c-b9e3-b6d80140ef77.png)](https://www.youtube.com/embed/sMjAroVIp0k)





## Arduino

AVR 기반의 마이크로컨트롤러 Wiring에서 파생한 프로젝트다.

영어로 '아두이노', 이탈리아어로 '아르두이노'라고 읽는다. 영어권의 영향이 강한 국내에서 많이 사용되는 명칭은 아두이노. 이탈리아어로 '강력한 친구'라는 뜻이라는 듯. 2005년 이탈리아의 Massimo Banzi와 David Cuartielles가 처음 개발하였다. 개발자 Massimo Banzi가 직접 저술한 <Getting Started with Arduino>(번역명 <손에 잡히는 아두이노>)를 필두로 많은 입문서들이 나와 있다.

비관련자를 위해 쉽게 설명하자면, 간단한 초소형 컴퓨터 기판 에 이런저런 기능을 할 수 있도록 프로그래밍을 하여 다양한 기계나 작업, 작품에 써먹는 경우가 많은데, 그것들 중에서도 교육에 특화되어 특히 더 쉬운 사용법을 자랑하는 시스템이라 보면 간단하다. 
* 아두이노와 관련된 작품들을 보고싶다면 추천한다.
* http://www.instructables.com/tag/type-id/category-technology



우노 R3 버전으로 2013년 기준 레퍼런스 보드이자 가장 보편적으로 사용되는 보드다. 사용하는 마이크로컨트롤러는 ATMega328P로 16MHz로 동작하고 프로그램 저장용 플래시 32KB를 내장한 프로세서이다.

임베디드 개발 경험이 전혀 없는 사람을 위해 개발된 교육용 플랫폼이기 때문에 프로그램을 작성하고 보드에 프로그램을 올리는 과정을 단순화하여 다루기 쉽게 되어 있다.

##### 종류

1. arduino Uno : 14개 디지털 입출력, 6개 아나로그, USB, 파워젝
2. Arduino Nao
3. Arduino Lilypad
4. Arduino Mega 2560 : 54개 디지털 핀, 16개 아나로그, usb, power, reset

##### 특징

1. USB 연결
2. 32KB 메모리, SRAM 2K, EEPROM 1K (Mega 2560 버젼은 256KB)
3. 16Mhz
4. 통신:  12C 및 SPI 통신



#### Atmel에서 만든 범용 RISC 마이크로컨트롤러. 

* CPU, ROM, RAM, 플래시 메모리, ADC, DAC, GPIO가 다 들어 있다.
* ISP(In-System Programming) 인터페이스를 갖추고 있어서 별도의 롬 라이터 없이 PC에서 프린터 포트나 시리얼 포트, USB 인터페이스에 연결하는 ISP 장비를 통해 손쉽게 프로그램을 짜 넣을 수 있다
* 저렴한 가격에 ROM, RAM 걱정 없이 프로그램을 넣을 수 있기 때문에 많은 대학교의 전자공학과에서 마이크로컨트롤러나 임베디드 시스템과 관련된 과목에서 AVR을 대상으로 강의하는 경우가 많다.

* 겨우 8비트급 마이크로컨트롤러임에도 불구하고 RISC를 표방하고 있다.
* 전기밥솥, 엘리베이터 제어, 자동 판매기 등 높은 성능이 전혀 필요 없고 신뢰성이 필요한 제어 장치 부분은 앞으로도 계속 8비트 마이크로컨트롤러가 사용될 것이다. 
* 각종 용도별 어셈블리 및 C 소스 프로그램이 온 천지에 널려있다... Arduino 플랫폼 중 가장 기본이 되고 많이 사용되는 아두이노 우노 또한 이 AVR 기반이다. 커스텀 키보드에도 USB를 지원하는 ATMega32 계열 MCU가 자주 사용된다.

##### ATMEGA128 

AVR도 여러 모델이 있지만 그 중 ATMEGA128이 가장 인기가 좋다. 

* 가격, 기능, 확장성 등의 적절함은 말할 것도 없고 예제 코드가 정말 넘쳐난다. 
* 프로세서만 단독으로 구매하면 보통 1.5만원 미만이고 외부 장치 연결을 위해 이런저런 포트들을 덕지덕지 달고 있는 모듈 타입도 10만원을 채 넘지 않는다. 
* 그냥 사다가 RS232C 포트나 UART 포트에 꽂은 뒤 매뉴얼에 적힌 코드를 그대로 복붙해서 다운로드만 해도 의도한 대로 동작하는 모듈들이 많다. 이 정도로 예제 코드가 넘쳐나는데 ATMEGA128로 원하는 것을 못 만든다면… 애초에 ATMEGA128을 제대로 다룰 줄 모르든가 아니면 ATMEGA128 정도의 프로세서로는 만들 수 없는 물건일 가능성이 높다. 
* 가장 큰 장점은 전기적 특성이 매우 강하다는 것. 핀이 공급하거나 받을수 있는 전류 한계치가 다른 마이크로컨트롤러에 비해 높다. I/O에서 감당 가능한 전류가 40mA로 다른 마이크로컨트롤러들의 경우 이것의 절반이거나 10분의 1 정도밖에 안되는 경우도 허다하다. 
* 물론 8비트 마이크로컨트롤러인 만큼 연산 능력이나 클럭 속도, 메모리 어드레스 영역은 상당히 제한된다. AVR 시리즈 중 고급형에 해당하는 ATMega급의 최대 동작 속도가 20MHz에 머물고 있으며, 그나마 이는 일부 모델만 해당되고 대부분은 16MHz가 한계이다. 대부분의 경우 FPU가 없을 뿐만 아니라 32비트 단정도 실수를 제대로 처리하기에는 워드 길이가 8비트로 크게 제약되는 나머지 소프트웨어적인 실수 연산 처리도 쉽지 않으므로 복잡한 수학 연산 성능은 거의 없다고 생각하는 편이 좋다. 
* 그러나 8비트 마이크로컨트롤러의 특성 상 구조가 간단하다. 32비트급 이상의 고속 MPU에서 주로 볼 수 있는 CPU 코어에 관련된 MMU나 DRAM 컨트롤러 등의 여러 장치들의 특성을 사전에 익힐 필요가 없고 OS를 끼고 돌아가는 경우가 적기 때문에 그에 관련된 내용도 따로 스터디할 필요가 없다. 
* 즉 부팅하고 바로 유저가 작성한 코드로 점프하면 되기 때문에 다루기 쉽다는 것이지, C 코드 문법이 쉽다는 의미가 아니다. 유지보수가 간단하며, I/O핀이 전기적으로 강인한 경우가 많고, 워낙 오랫동안 사용되어 오면서 검증된 안정성과 무엇보다도 32비트급 마이크로컨트롤러에 비해 단가가 매우 싸기 때문에 단순 제어 분야에서는 현업에서도 여전히 널리 사용되고 있다.



#### AVR란?

ATMEL사가 개발한 AVR은 현재 8비트 AVR과 32비트 AVR을 제공하고 있는 마이크로 컨트롤러이다. AVR의 다양한 명령과 쉬운 구조를 띄고 있어 마이크로 컨트로로러 이해하는데 쉽게 접근할 수 있으며, 가격이 저렴하고 응용하기 쉬워 산업시장에서도 많이 사용되어 지고 있다.

*  AVR은 1개의 클록 사이클에 1개의 명령을 처리 할 수 있으며, 1.8V에서 5.5V까지 어느 전압이든 동작 시킬 수 있다. 
* picoPower 기술이 적용된 제품의 경우 저 전력 설계가 가능하고, 32개의 범용 레지스터와 RISC 구조의 디자인은 C언어에 적합하여 제품을 빠르게 개발하는데 도움이 된다. 
* 재부에 플래시 메모리를 제공함으로서 새로 개발되는 제품의 크기를 줄일 수 있고, 제품의 크기가 줄면서 원가 절감에도 도움이 된다. 
*  6핀 또는 10핀 인터페이스로 제공되는 ISP(In-System Programming)기능이나 JTAG 기능은 쉽게 제품을 개발하는데 도움이 된다.



#### 아두이노 주의 사항

* 8비트 임베디드 시스템 프로그래밍에 있어서는 프로그램 최적화에 매우 신경써야 한다. 마이크로 컨트롤러같이 메모리 리소스가 크게 제한되는 장치에서 프로그래밍을 할 경우 항상 주의해야 하는 부분이다. 아두이노는 성능이 매우 떨어지기 때문에 다른 기계에서는 문제없을만한 부분이 유독 문제를 일으키기도 한다. 
* C에서 함수가 중복 호출될 경우 스택 오버플로를 일으키면서 장비가 정지될 수 있다. 예를 들어, 장비가 정지했는데 개발 도중에 동작 테스트를 위해 추가한 Serial.print();문 몇 줄을 지워보니 추가한 코드들이 갑자기 정상적으로 돌아가는 경우도 있다. 이 때문에 deploy판에 디버그용 print를 지우고 보내는 것은 기본이다. 하드웨어 시리얼로 블루투스 통신을 한다던지 등 예외적인 경우에만 놔두는 것이 좋다.
* 아두이노 자체의 성능 제약을 피하려면, 라즈베리 파이 같은 다른 장치를 연결해 연산은 다른 데에서 처리하고, 아두이노는 센서나 액추에이터 등을 관리하는 기계로만 사용하는 게 나을 수도 있다. 
* 아두이노에 Firmata라는 펌웨어를 올리면 Firmata 프로토콜을 통해서 외부에서 아두이노를 컨트롤할 수 있게 된다. Processing을 비롯해 꽤 많은 언어를 이용하여 Firmata로 아두이노를 컨트롤할 수 있으니 이쪽을 알아보는 것도 괜찮다. 이걸 잘 활용하면 아두이노에는 최소한의 코드만 올리고 연산 부하가 큰 나머지 부분은 PC나 라즈베리 파이 같은 별도의 장치의 자원을 사용하여 돌리는 식으로 동작시키는 게 가능하다. 아두이노 자체로는 센서값 읽어서 판단하고 트윗올리는 것만 짜넣어도 빡빡한 경우가 있으니 판을 크게 벌일 거라면 다른 장치를 사용해 통제하는 걸 고려해보자. 
* 판이 크지 않다고 하더라도 외부 컴퓨터-아두이노 사이의 통신이 필요한 프로젝트인 경우, 시리얼 통신으로 메시지를 주고받는 것보다 자연스러운 형태로 코딩이 가능하므로 Firmata를 적극 사용해보는 것도 괜찮다. 이런 과정이 번거롭다면 내부 플래시와 램 용량이 크게 늘어난 아두이노 두에 혹은 2016년 기준 최신형인 제로나 전술한 101 또는 Primo, Star를 쓰는 것도 좋은 선택.
* 아두이노 IDE에 내장된 ArduinoISP 예제를 이용하여 다른 아두이노에 업로드를 할 경우, ArduinoISP로 업로드받은 아두이노는 부트로더가 지워진다! 그렇기 때문에 웬만하면 USB TO UART 컨버터를 이용해 업로드하자.
* 아두이노 컴파일러에서 소스 코드를 보드에 업로드 할 때, 우분투 같은 리눅스로 하는 것이 윈도우로 하는 것 보다 훨씬 빠르다.



### [ARDUINO 개념](https://yozm.wishket.com/magazine/detail/234/)



##### 출력장치

* DC 모터
* 스테퍼 모터
* 서보 모터
* 솔레이노이드
* LCD 디스플레이
* LEF 표시등
* 스피커

##### Arduino UNO 보드



##### Arduino 소프트웨어 IDE

* 아두이노 코드는 스케치라고 부름
* C 계역 언어
* 자체 라이브러리



##### 인기 있는 이유

1. 마이크로 컨트롤러를 사용하기 쉽게 만들어 졌다.
2. 단순한 USB 케이블로 연결
3. 다른 부품들과 쉽게 연결
4. 외부 전원 연결 잭 (건전지 가능)





#### [Arduino Libraries](https://www.arduino.cc/reference/en/libraries/)

* [Libraries](https://www.arduino.cc/reference/en/libraries/) 
* IOT Cloud [API](https://www.arduino.cc/reference/en/iot/api/)





### 무선통신

#### nRF24L01

* [무선통신으로 조이스틱-서보모터제어](https://rasino.tistory.com/258?category=1038094)
* [nRF24L01 RF무선통신](https://rasino.tistory.com/255?category=1038094) : 100m 공간, 안테나 800m 송수신 가능





## [DIY 메카솔루션 오픈 랩](https://blog.naver.com/roboholic84)



### 환경 설치

#### Arduino 설치

https://www.arduino.cc/

* [IDE 스케치 설치](https://blog.naver.com/PostView.naver?blogId=roboholic84&logNo=222662992879&categoryNo=30&parentCategoryNo=&from=thumbnailList)
* 



#### 온거리 센서 보드

NANO 33 BLE Sense의 APDS9960센서는 센서에서 적외선을 출력하여 반사되어 돌아오는 빛을 이용해 거리를 측정할 수 있습니다. 이때 센서에서 적외선이 출력되기 때문에 센서를 바라보지 않는 것이 좋습니다. 환경에 따라 다르겠지만, 대략 65 ~ 200mm에서 측정이 되었습니다.

```c
#include <Arduino_APDS9960.h>
void setup() {
  Serial.begin(9600);
  while (!Serial); // 시리얼 모니터가 켜졌을때만 작동합니다.
  if (!APDS.begin()) { // 센서 초기화가 실패하면 오류를 발생시킵니다.
    Serial.println("APDS9960센서 오류!");
    while (1);
  }
}
void loop() {
  if (APDS.proximityAvailable()) { // 센서의 값이 읽혔을 때 작동합니다.
    // - 0   => close
    // - 255 => far
    // - -1  => 오류
    int proximity = APDS.readProximity(); // 센서의 값을 변수에 저장합니다.
    Serial.println(proximity);
  }
  delay(100);
}
```



#### push button



```c
void setup() {
  pinMode(13,OUTPUT);
  pinMode(2,INPUT);
}

void loop() {
  int val = digitalRead(2);
  if(val ==  HIGH ) // 표시되어 있는 if문의 HIGH를 LOW만 바꿔도 풀업/풀다운이 변경 가능합니다.
    digitalWrite(13,HIGH);
  else
    digitalWrite(13,LOW);
  delay(1);
}
```



### 자동차

#### 4WD 

* [4WD](https://blog.naver.com/PostView.naver?blogId=roboholic84&logNo=220986481120&categoryNo=30&parentCategoryNo=&from=thumbnailList)

* [aliexpress](https://ko.aliexpress.com/item/1005001854590552.html?spm=a2g0o.detail.100009.3.f4952ce5CJl7Q6&gps-id=pcDetailLeftTopSell&scm=1007.13482.271138.0&scm_id=1007.13482.271138.0&scm-url=1007.13482.271138.0&pvid=f9ce3011-d06f-4f77-9821-614ec6413d95&_t=gps-id%3ApcDetailLeftTopSell%2Cscm-url%3A1007.13482.271138.0%2Cpvid%3Af9ce3011-d06f-4f77-9821-614ec6413d95%2Ctpp_buckets%3A668%232846%238107%231934&pdp_ext_f=%7B%22sku_id%22%3A%2212000027653092910%22%2C%22sceneId%22%3A%223482%22%7D&pdp_npi=2%40dis%21KRW%21%2165557.0%21%21%21%21%21%40210323b516574531144281393e94e4%2112000027653092910%21rec&gatewayAdapt=glo2kor)







#### 서버 모터 

##### PWM을 이용한 서버 모터 제어

* [PWM](https://m.blog.naver.com/emperonics/221725399383)
* [아두이노 모션 만들기](https://blog.naver.com/emperonics/221699682773)
* [아두이노 서보 제어](https://blog.naver.com/emperonics/221699682773)



#### 앱 인벤터

##### 앱인벤터

* [1. MIT App Inventor](https://rasino.tistory.com/268?category=1068055)
* [2. 설치](https://rasino.tistory.com/269?category=1068055)
* [3. 따라하기](https://rasino.tistory.com/271?category=1068055)
* [4. 화면이동](https://rasino.tistory.com/272?category=1068055)
* [5. 날짜 시간 체크박스](https://rasino.tistory.com/276?category=1068055)
* [6. 사진 글자 SNS 보내기](https://rasino.tistory.com/288?category=1068055)
* [7. 사진글자 보내기](https://rasino.tistory.com/290?category=1068055)
* [8.사진저장소](https://rasino.tistory.com/305?category=1068055)









### 해결해야 할 과제 

* 발견한 다음에는 이미 늦는 것 아닌가 ? (강풍에서 발생하는 산불)
* 산불 말고도 뭔가 환경적 문제를 복합적으로 해결할 수 있는 Device가 되어야 하지 않을까? 새소리 분석해서 (살고 있는 새들 분포)
* 센서 (불꽃,연기,온도, 현재 위치 GPS 모듈)
* 전력 문제 (저전력모드, 충전)
* 이동성
* 통신문제 (노드간 통신, 중간 노드 끊어 질때, 최종 노드 연결 방법(역방향), RF통신, Wifi, )
* 앱 프로그램
* IOT cloud

#### 전력 문제

* [Arduidno 저전력 상태](https://fishpoint.tistory.com/5656)
* 







### 이산화 탄소 포집 기술

기후 변화로 인한 최악의 사태를 피하기 위해선 2050년까지 '넷 제로(탄소중립)' 즉, 온실가스의 순배출을 '제로(0)'에 가깝게 해야 한다. 이는 우리가 대기로 배출하는 이산화탄소 등 온실가스의 양만큼, 이를 다시 대기로부터 흡수해야 한다는 뜻이기도 하다.

* [직접 포집 기술](https://www.bbc.com/korean/features-61206039)

* 직접 공기 포집(DAC)' :  "산림조성이나 오래된 숲을 복원하는 작업을 통상적으로 환경에 덜 해롭다고 인식하는 경향이 있기에 일반적으로 더 선호하지만, 장기적인 측면에서는 효과적이지 않다"

* "나무가 탄소를 흡수하는 능력은 일시적입니다. 전체 산림을 유지하지 않는 이상 나무가 성장을 멈추면 탄소 제거도 멈추기 때문

  



#### [일론머스스크도 찾고 있는 탄소 포집 기술](https://dream.kotra.or.kr/kotranews/cms/news/actionKotraBoardDetail.do?SITE_NO=3&MENU_ID=180&CONTENTS_NO=1&bbsGbn=243&bbsSn=243&pNttSn=187066)



이산화탄소 포집, 활용, 저장(Carbon Capture, Utilization and Storage, CCUS)을 의미하는 CCUS 기술은 화석연료의 사용 등으로 인해 대량의 이산화탄소가 생산되는 근원지에서 그 이산화탄소가 공기 중으로 방출되는 것을 방지하는 기술을 통합적으로 이른다. 온실가스 감축에 대한 범세계적 논의가 그 어느 때보다 활발한 가운데 최근 들어서야 지구 온난화를 저지할 기술로 주목받고 있지만 사실 CCUS는 약 45년 동안 전 세계에서 다양한 방식으로 사용되며 온실가스 배출량 감소에 기여해왔다. CCUS 기술은 크게 3가지 단계로 분류된다. 

1. 포집: 석탄 및 천연가스 화력발전소, 제철소, 시멘트 공장, 정유 공장 등과 같은 대규모 산업 공정 시설에서 생산된 다른 가스에서 이산화탄소를 분리하는 기술

2. 운송: 분리된 이산화탄소를 압축해 파이프라인, 트럭, 선박 또는 다른 방법을 통해 저장에 적합한 장소까지 운송하는 기술

3. 사용 또는 저장: 포집한 이산화탄소를 필요한 곳에 사용하거나 이산화탄소가 대기중으로 빠져나가는 것을 막기 위해 1km 이상의 깊은 지하 암석층에 저장하는 기술

##### 2050년까지 이산화탄소 포집.저장  3.6기가톤

글로벌CCS연구소가 탄소 배출 제로(Net-zero Emission)에 도달하기 위해 얼마나 많은 이산화탄소를 포집하고 저장해야 하는지에 대해 90개의 시나리오를 분석한 결과, 탄소 배출 제로를 달성하려면 2050년까지 전 세계 이산화탄소 포집·저장 용량이 연간 3.6기가톤에 달해야 하는 것으로 밝혀졌다. 그러나 오늘날 전 세계적으로 설치된 CCUS 시설의 포집 용량은 약 40메가톤에 그치고 있어 이산화탄소 포집, 저장 역량이 약 100배 이상 늘어나야 탄소 제로 목표를 실현할 수 있을 것으로 전망된다. CCUS 기술은 1970년대부터 사용돼 왔지만 아직 시장 확장 가능성이 무궁무진하고 새로운 기술이 등장할 수 있는 분야라는 이야기다. 테슬라의 CEO 일론 머스크가 최고의 탄소 포집 기술 상금으로 1억 달러를 기부하겠다는 약속을 내건 것도 탄소 포집 분야에서 혁신을 기대할 수 있기 때문으로 해석할 수 있다.



#### 국내 기업 동향: CCUS(Carbon Capture, Utilization, Storage)

CCUS 사업에 진출해 가시적인 성과를 내고 있는 건설사는 DL이앤씨와 삼성엔지니어링이다.

* DL이앤씨는 친환경 신사업 분야 등 사업구조 재편에 나서고 있다. 우선 탄소중립 시대에 발맞춰 이산화탄소 포집·활용·저장(CCUS) 사업을 차세대 먹거리 사업으로 육성 중이다. 이산화탄소는 포집·활용 과정을 거쳐 산업원료 및 제품으로 재생산되기 때문에 CCUS는 탄소중립 이행을 위한 필수 기술로 꼽힌다.

  연내 충남 서해그린환경의 폐기물 처리사업장에 연간 약 6만톤 규모의 이산화탄소를 포집하는 설비를 착공, 이르면 내년부터 본격적인 가동에 착수할 계획이다. 기존 폐기물 처리 시설을 친환경 시설로 탈바꿈해 탄소배출권 확보 가능성도 열어둔다는 계획이다.

  DL이앤씨는 탄소중립의 핵심으로 평가받는 탄소 포집 및 활용, 저장(CCUS) 사업 전반에 걸쳐 종합적인 솔루션을 제공하는 기업으로 도약하기 위한 청사진도 함께 공개했다.

* 삼성엔지니어링 역시 지구온난화 방지를 위한 수소·탄소중립 사업에 팔을 걷어붙였다. 수소 디벨로퍼로 도약하고자 이산화탄소 포집과 활용, 저장 기술 확보에 역량을 모으고 있다. 6월 글로벌에너지 기술 기업인 베이커휴즈와 'CCUS 및 수소 에너지 이용'과 관련한 업무협약을 맺은 바 있다. 



K-CCUS(한국형 CCUS) 추진단은 산업통상자원부 주도로 에너지 관련기업들과 한국전력공사 및 학계와 연계해 만든 컨트롤타워다. 민간기업 50개가 참여하고 있다. 여기에는 SK이노베이션, 두산중공업, 현대중공업, 한국조선해양, GS칼텍스, S-Oil, 영풍산업, 삼표산업 등 민간기업 50개가 참여 중이다.

* 현대오일뱅크, 동해가스전, SK이노베이션:  이들 연구원들은 국내에서 CCS, CCU를 위주로 연구를 진행하는 정유사들이 약진하고 있다며 블루수소 로드맵을 밝힌 현대오일뱅크, 동해가스전 및 EU REALIZE 프로젝트에 참여하는 SK이노베이션 등이 선두주자라고 평가했다. 

* 롯데케미칼 :   화학업체 중에서는 CCU 설비를 여수 1공장에 설치해 연 6만톤의 이산화탄소 포집을 위한 실증 연구를 진행하는 롯데케미칼에 주목할 필요가 있다고 했다.
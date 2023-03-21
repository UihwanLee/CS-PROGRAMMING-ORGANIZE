# Chapter03 - 컴퓨터 시스템과 운영체제

### 컴퓨터 시스템과 운영체제 개요

```
◼ 컴퓨터 시스템에서 하드웨어의 구조와 작동 원리의 핵심을 이해한다.
◼ 컴퓨터 시스템에서 운영체제의 위치와 역할을 알고, 그에 따른 운영체제의 전체 기능을 이해한다.
◼ 운영체제가 응용프로그램과 하드웨어 사이의 중개자로서 제공하는 시스템 호출과 인터럽트에 대해 자세히 이해한다.
◼ 응용프로그램이 실행되는 2가지 모드, 사용자 모드와 커널 모드에 대해 이해하고, 이들을 두는 목적 등을 이해한다.
◼ 운영체제는 메모리 공간을 사용자 공간과 커널 공간으로 나누어 활용함을 이해한다.
◼ 운영체제 커널의 개념과 실체에 대해 충분히 이해한다.
```
 <hr>

### 1. 컴퓨터 시스템과 하드웨어
<br>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>컴퓨터 시스템의 범위</strong></span></summary>
    <ul>
     <li>컴퓨터 시스템의 계층</li> 
     <ul>
      <li>1) 응용프로그램 층</li>
      <li>2) 운영체제 층</li>
      <li>3) 컴퓨터 하드웨어 층</li>
     </ul>
     <li>컴퓨터 시스템 계층 구조의 특징</li> 
     <ul>
      <li>사용자는 응용프로그램과 GUI/도구프로그램(툴 /유틸리티)을 통해 컴퓨터 활용</li>
      <li>하드웨어는 모두 운영체제의 배타적 독점적 지배 받음</li>
      <li>사용자나 응용프로그램의 하드웨어에 대한 직접 접근 불허 → 반드시 운영체제를 통해서만 접근 가능</li>
     </ul>
  </ul>
  <img src="https://user-images.githubusercontent.com/36596037/226596063-13093717-c866-47f5-8bff-8980f7a92c72.png">
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>컴퓨터 하드웨어 설명</strong></span></summary>
    <ul>
     <li>CPU(Central Processing Unit)</li> 
     <ul>
      <li>컴퓨터의 가장 핵심 장치이며 프로그램 코드(기계 명령)를 해석하여 실행하는 중앙처리장치</li>
      <li>전원이 공급될 때 작동 시작, 메모리에 적재된 프로그램 실행</li>
     </ul>
     <li>메모리</li> 
     <ul>
      <li>CPU에 의해 실행되는 프로그램 코드와 데이터가 적재되는 공간 → 반도체 메모리 RAM</li>
      <li>프로그램은 실행되기 위해 반드시 메모리에 적재되어야 함</li>
     </ul>
     <li>캐시 메모리(Cache Memory)</li> 
     <ul>
      <li>CPU의 프로그램 실행 속도를 높이기 위해, CPU와 메모리 사이에 소량의 빠른 메모리(고가의 메모리)를 설치하게 되었음</li>
      <li>캐시 메모리가 있는 경우 CPU는 캐시 메모리에서만 프로그램 실행/li>
     </ul>
     <li>장치(device)들</li> 
     <ul>
      <li>키보드, 프린터, 스캐너 등</li>
     </ul>
     <li>버스(bus)</li> 
     <ul>
      <li>하드웨어들이 데이터를 주고받기 위해 0과 1의 디지털 신호가 지나가는 여러 가닥의 선을 다발로 묶어 부르는 용어</li>
      <li>버스의 종류(버스에 지나다니는 정보에 따라)</li>
      <ul>
       <li>주소 버스(address bus) - 주소 신호가 지나다니는 버스</li>
       <li>데이터 버스(data bus) - 데이터 신호가 지나다니는 버스</li>
       <li>제어 버스(control bus) - 제어 신호가 지나다니는 버스</li>
      </ul>
      <li>주소</li>
      <ul>
       <li>메모리, 입출력 장치나 저장 장치 내에 있는 저장소(레지스터들)에 대한 번지이며 0번지에서 시작하는 양수</li>
       <li>주소 버스는 주소 값이 전달되는 여러 선의 다발</li>
       <li>CPU는 메모리나 입출력 장치에 값을 쓰거나 읽을 때 반드시 주소를 발생시킴</li>
      </ul>
      <li>목적에 따라 버스 구분</li>
      <ul>
       <li>시스템 버스(system bus): CPU, 캐시 메모리, 메모리 등 빠른 하드웨어들 사이에 데이터 전송 → 고속도로에 비유</li>
       <li>입출력 버스(I/O bus) : 상대적으로 느린 입출력 장치들로 부터 입출력 데이터 전송 → 일반 도로에 비유</li>
      </ul>
  </ul>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>CPU와 메모리의 관계</strong></span></summary>
    <ul>
     <li>32비트 컴퓨터란?</li> 
     <ul>
      <li>32비트 CPU를 가진 컴퓨터</li>
     </ul>
     <li>32비트 CPU란?</li> 
     <ul>
      <li>한번에 32비트를 처리할 수 있는 내부구조(레지스터, ALU 등)를 갖는 CPU</li>
      <li>CPU에 32개의 주소선 있음</li>
      <ul>
       <li>CPU의 액세스 범위: 232개의 서로 다른 주소(0 ~ 232-1 번지)</li>
       <li>한 번지의 공간이 1바이트이므로, 232개의 주소 = 232 바이트 = 4GB</li>
       <li>32비트 CPU를 가진 컴퓨터에 4GB이상 메모리를 설치할 경우에는 4GB를 넘어선 영역은 사용할 수 없음</li>
     </ul>
      <li>CPU에 입출력 되는 32개의 데이터 선 있음</li>
     </ul>
  </ul>
  <img src="https://user-images.githubusercontent.com/36596037/226597511-a77f671a-c2b5-4c49-bf6c-d98a4938b456.png">
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>CPU의 일생 – CPU 레지스터, 명령 처리 과정</strong></span></summary>
    <ul>
     <li>CPU 레지스터들</li> 
     <ul>
      <li>PC(Program Counter) - 다음에 실행할 명령의 메모리 주소 저장</li>
      <li>IR(Instruction Register) - 현재 실행하기 위해 메모리로부터 읽어 온 명령 저장</li>
      <li>SP(Stack Pointer) - 스택의 톱 메모리 주소 저장</li>
      <li>상태 레지스터(status register) - CPU의 상태 정보나 인터럽트 금지 등의 제어 정보 저장</li>
      <li>데이터 레지스터들(data registers) - 연산에 사용되거나 사용될 데이터들 저장</li>
      <li>기타 특수용도 레지스터들 - 페이지 테이블이 저장된 메모리 주소를 가리키는 레지스터 등</li>
     </ul>
     <li>CPU 명령 사이클(instruction cycle) – CPU의 일생</li> 
     <ul>
      <li>CPU가 하나의 명령을 실행하는 과정</li>
      <li>CPU는 전원이 켜진 후 단순하게 명령 사이클 반복</li>
     </ul>
  </ul>
  <img src="https://user-images.githubusercontent.com/36596037/226598440-174eb550-33fc-4386-8f55-a8a819990933.png">
  <img src="https://user-images.githubusercontent.com/36596037/226598485-fc82c863-037e-451a-8e5e-3fef18f41570.png">
</details>
 
 <details>
  <summary><span style="border-bottom:0.05em solid"><strong>스택(Stack)은 어디에 있는가?</strong></span></summary>
    <ul>
     <li>프로그램이 실행되기 위해 운영체제가 할당하는 4개의 공간</li> 
     <ul>
      <li>1) 코드(code) 공간 – 프로그램 코드 적재</li>
      <li>2) 데이터(data) 공간 - 전역 변수들이 적재되는 공</li>
      <li>3) 힙(heap) 공간 – 프로그램에서 동적 할당 받는 공간</li>
      <li>4) 스택(stack) 공간 – 함수가 호출될 때 매개변수, 지역변수 등 저장</li>
     </ul>
     <li>스택</li> 
     <ul>
      <li>메모리의 일부를 스택으로 사용하도록 할당된 공간</li>
      <li>C운영체제는 각 프로그램에게 스택 공간을 할당하며 SP 레지스터는 현재 CPU가 실행중인 프로그램의 스택 꼭대기 주소를 가리킴</li>
     </ul>
  </ul>
  <img src="https://user-images.githubusercontent.com/36596037/226599142-f2afdea1-5d74-4b2c-94c8-cdf4f69b665b.png">
</details>
 
<details>
  <summary><span style="border-bottom:0.05em solid"><strong>컨텍스트(Context, 문맥)</strong></span></summary>
    <ul>
     <li>한 프로그램이 실행 중인 일체의 상황 혹은 상황 정보</li> 
     <ul>
      <li>CPU 레지스터들의 값</li>
      <ul>
       <li>PC(코드 주소), SP(스택 주소), 기타 다른 레지스터들의 값</li>
      </ul>
      <li>메모리</li>
      <ul>
       <li>프로그램 코드와 데이터, 스택, 동적 할당을 받아 저장한 값</li>
      </ul>
      <li>축소 정의한 컨텍스트(문맥)의 정의</li>
      <ul>
       <li>메모리의 내용은 문맥 교환시에도 유지되므로 CPU 레지스터들의 값만으로 정의</li>
      </ul>
     </ul>
 </ul>
 <img src="https://user-images.githubusercontent.com/36596037/226600101-5c7b03ee-1f69-4237-8b9c-192a70d5274a.png">
</details>
 
 <details>
  <summary><span style="border-bottom:0.05em solid"><strong>컨텍스트 스위칭(문맥 교환)</strong></span></summary>
    <ul>
     <li>CPU가 현재 프로그램의 실행을 중지하고 다른 프로그램을 실행할 때 발생</li> 
     <li>컨텍스트 스위칭 과정</li> 
     <ul>
      <li>1) 현재 실행중인 프로그램의 컨텍스트(CPU 레지스터들의 값)를 메모리에 저장</li> 
      <li>2) 새로 실행시킬 프로그램의 저장된 컨텍스트(CPU 레지스터들의 값)를 CPU에 복귀</li> 
     </ul>
  </ul>
   <img src="https://user-images.githubusercontent.com/36596037/226600195-23b5a2c6-17c1-457a-8007-8510897010ed.png">
</details>

<hr>

### 2. 컴퓨터 시스템의 계층 구조와 운영체제 인터페이스
<br>
 
<details>
  <summary><span style="border-bottom:0.05em solid"><strong>컴퓨터 시스템 계층 구조</strong></span></summary>
    <ol>
     <li>사용자</li> 
     <li>응용프로그램</li> 
     <li>운영체제</li> 
     <ul>
      <li>커널 코드</li> 
      <li>디바이스 드라이버</li> 
     </ul>
     <li>하드웨어</li> 
  </ol>
   <img src="https://user-images.githubusercontent.com/36596037/226600676-17241ac6-5de0-4895-a23d-873c9629f63a.png">
</details>
 
<details>
  <summary><span style="border-bottom:0.05em solid"><strong>컴퓨터 시스템이 계층 구조로 설계된 이유</strong></span></summary>
    <ul>
     <li>계층간 독립성 확보(칸막이가 있다고 생각 = 다른 계층의 상세 내용은 몰라도 사용 가능)를 위해</li> 
     <ul>
      <li>사용자</li> 
      <ul>
       <li>운영체제나 하드웨어에 대해 몰라도 응용프로그램으로 컴퓨터 활용</li> 
      </ul>
      <li>응용프로그램</li> 
      <ul>
       <li>컴퓨터 하드웨어의 타입이나 구조, 제어 방법을 몰라도 개발 가능</li>
       <li>컴퓨터 하드웨어가 바뀌어도 응용프로그램을 다시 작성할 필요 없음</li>
      </ul>
      <li>운영체제</li> 
      <ul>
       <li>운영체제는 장치 관련된 모든 작업을 디바이스 드라이버에게 요청</li>
       <li>응용프로그램과 하드웨어 사이의 인터페이스</li>
      </ul>
  </ul>
</details>
 
<details>
  <summary><span style="border-bottom:0.05em solid"><strong>왜 운영체제가 필요한가?</strong></span></summary>
    <ul>
     <li>운영체제가 없다면</li> 
     <ul>
      <li>응용프로그램이나 사용자가 직접 하드웨어를 제어해야 함</li> 
      <li>하드웨어에 대한 지식이 필요하며, 충돌, 관리, 보안의 문제 발생</li> >
     </ul>
     <li>운영체제의 필요성 → 자원에 대한 충돌 해결, 성능 최적화, 사용자의 시스템 사용 효율화</li>
  </ul>
</details>
 
 <details>
  <summary><span style="border-bottom:0.05em solid"><strong>운영체제의 구성 요소와 커널</strong></span></summary>
  <img src="https://user-images.githubusercontent.com/36596037/226601783-78d3bab0-f9d1-4839-91ee-8be87ccec5aa.png">
</details>
 
 <details>
  <summary><span style="border-bottom:0.05em solid"><strong>운영체제 구성</strong></span></summary>
    <ul>
     <li>운영체제 = 커널 + 툴 + 디바이스 드라이버</li> 
     <ul>
      <li>1) 커널(kernel)</li> 
      <ul>
       <li>운영체제의 핵심 부분, 좁은 의미의 운영체제, 부팅 후 메모리에 상주하는 코드와 데이터이며 운영체제의 핵심 기능 모두 구현</li> 
       <li>커널 코드는 함수들의 집합이며 커널 기능을 이용하려면 응용프로그램은 반드시 시스템 호출 사용</li> >
      </ul>
      <li>2) 도구(tool) 소프트웨어와 GUI</li>
      <ul>
       <li>사용자가 컴퓨터를 편리하게 사용할 수 있도록 제공하는 툴 소프트웨어 혹은 툴 응용프로그램</li> 
      </ul>
      <li>3) 디바이스 드라이버(device driver)</li>
      <ul>
       <li>장치를 직접 제어하고 입출력을 담당하는 소프트웨어</li> 
      </ul>
     </ul>
  </ul>
 <img src="https://user-images.githubusercontent.com/36596037/226602418-bcd23719-7efb-4663-bd8c-a1e040e896e2.png">
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>커널의 형태에 따른 구분</strong></span></summary>
    <ul>
     <li>모놀리식(Monolithic) 커널</li> 
     <ul>
      <li>단일 커널이라고도 부르며 커널의 모든 기능이 하나의 덩어리로 구현됨 → Unix, Linux, DOS, Solaris 등</li> 
     </ul>
     <li>마이크로(Micro) 커널</li> 
     <ul>
      <li>기본 핵심 기능만 커널에 구현하고 나머지 기능은 ‘서버’라는 프로세스로 제공 → Mach, QNX, Symbian, Mac OS X, Minix</li> 
     </ul>
     <li>하이브리드(혼합형) 커널</li> 
     <ul>
      <li>현재는 순수 마이크로 커널 방식은 없고 모놀리식 커널과 마이크로 커널의 장단점을 섞어서 사용 → Windows</li> 
     </ul>
  </ul>
</details>
 
 <details>
  <summary><span style="border-bottom:0.05em solid"><strong>운영체제 커널 인터페이스: 시스템 호출과 인터럽트</strong></span></summary>
    <ul>
     <li>커널에 접근하는 2가지의 인터페이스: 시스템 호출과 인터럽트</li> 
     <ul>
      <li>1) 시스템 호출 → 응용 프로그램에서 커널을 호출하는 방법</li> 
      <li>2) 인터럽트 → 하드웨어에서 커널을 호출하는 방법</li> 
     </ul>
     <li>1) 시스템 호출(system call)</li> 
     <ul>
      <li>커널과 응용프로그램 사이의 인터페이스이며 응용프로그램에서 커널 기능을 사용할 수 있는 유일한 방법</li> 
      <li>시스템 호출 라이브러리를 통해 다양한 시스템 호출 함수 제공하며 운영체제 패키지에 포함됨</li> 
     </ul>
     <li>2) 인터럽트(interrupt)</li> 
     <ul>
      <li>커널과 하드웨어 장치 사이의 인터페이스</li> 
      <li>인터럽트가 발생하면</li> 
      <ul>
       <li>① CPU는 하던 일을 중단하고 인터럽트 서비스 루틴(ISR: Interrupt Service Routine) 실행</li> 
       <li>② 인터럽트 서비스 루틴은 대부분 디바이스 드라이버 내에 있음</li> 
       <li>③ 인터럽트 서비스 루틴은 커널 영역에 적재</li> 
       <li>④ CPU는 인터럽트 서비스 루틴의 실행을 마치면 하던 작업 계속</li> 
      </ul>
      <li>인터럽트 활용</li> 
      <ul>
       <li>운영체제가 장치에게 지시한 입출력 작업의 완료, 예고 없는 네트워크 데이터의 도착, 키보드나 마우스의 입력, 부족한 배터리 경고 등 장치와 관련된 모든 이벤트 처리</li> 
      </ul>
     </ul>
  </ul>

<img src="https://user-images.githubusercontent.com/36596037/226603160-f959d282-3a8c-47b1-b2d5-79f417260c1f.png">
</details>
 
<hr>

### 3. 커널과 시스템 호출
<br>
 
  <details>
  <summary><span style="border-bottom:0.05em solid"><strong>응용프로그램의 자원 접근 문제</strong></span></summary>
    <ul>
     <li>근래의 운영체제는 다수의 응용프로그램이 한 컴퓨터에서 동시에 실행되는 형태</li> 
     <li>다양한 문제점</li> 
     <ul>
      <li>응용프로그램이 직접 컴퓨터 자원에 접근하면 충돌과 훼손 발생</li> 
      <li>다른 응용프로그램이 적재된 메모리 훼손 가능</li> 
     </ul>
     <li>해결 방안</li> 
     <ul>
      <li>응용프로그램의 자원 접근을 불허하며 자원에 대한 모든 접근은 커널에만 부여</li> 
     </ul>
     <li>구체적인 해결 방법</li> 
     <ul>
      <li>1) 메모리 공간을 사용자 공간과 커널 공간으로 분리 → 응용프로그램은 사용자 공간에만 적재, 커널은 커널 공간에만 적재</li>
      <li>2) CPU의 실행 모드를 사용자 모드와 커널 모드로 분리</li>
      <li>3) 응용프로그램이 커널 기능을 이용하고자 할 때, 시스템 호출을 이용해서만 커널 코드 이용</li>
     </ul>
  </ul>
</details>
 
 <details>
  <summary><span style="border-bottom:0.05em solid"><strong>사용자 공간과 커널 공간</strong></span></summary>
    <ul>
     <li>운영체제는 CPU로 액세스(접근) 할 수 있는 전체 주소공간을 2개의 공간으로 분리</li> 
     <ul>
      <li>1) 사용자 공간(user space)</li> 
      <ul>
       <li>응용프로그램이 적재되고 응용프로그램의 변수가 만들어지고, 동적으로 할당 받는 공간</li> 
       <li>사용자 모드로만 동작</li> 
      </ul>
      <li>2) 커널 공간(kernel space)</li> 
      <ul>
       <li>커널만 사용할 수 있는 공간</li> 
       <li>커널 코드, 커널 데이터 등 커널에 의해 배타적으로사용되는 공간이며 디바이스 드라이버도 포함됨</li> 
       <li>커널 모드로만 동작</li> 
      </ul> 
     </ul>
  </ul>
<img src="https://user-images.githubusercontent.com/36596037/226605299-6fddb95d-13f5-49d7-9948-f3f495732771.png">
</details>
 
  <details>
  <summary><span style="border-bottom:0.05em solid"><strong>사용자 공간 크기의 의미</strong></span></summary>
    <ul>
     <li>사용자 공간 크기</li> 
     <ul>
      <li>한 응용프로그램의 최대 크기 결정</li> 
      <ul>
       <li>프로그램 코드 + 데이터(전역변수) + 힙(동적할당) + 스택 합친 크기</li> 
       <li>예) 32비트 Windows 운영체제에서 사용자 공간 2GB → 응용프로그램을 2GB 크기이상 개발할 수 없음</li> 
      </ul>
     </ul>
     <li>사용자 공간의 주소 범위</li> 
     <ul>
      <li>응용프로그램은 운영체제가 설정한 사용자 공간의 주소 범위를 넘어설 수 없음</li> 
      <ul>
       <li>예) 32비트 Windows 운영체제에서 응용프로그램은 0~7FFFFFFF 범위의 주소를 넘어 액세스하면 바로 종료(심각한 오류</li> 
      </ul>
     </ul>
  </ul>
<img src="https://user-images.githubusercontent.com/36596037/226606196-7e99e653-6abf-413b-90ee-4a32242723cf.png">
</details>
 
 <details>
  <summary><span style="border-bottom:0.05em solid"><strong>가상(논리) 주소 공간</strong></span></summary>
    <ul>
     <li>가상(virtual, 논리) 주소공간 = 사용자 공간 + 커널 공간</li>
     <li>개념</li>
     <ul>
      <li>근래의 운영체제에서 사용자나 응용프로그램 관점에서 보는 주소 범위(공간)</li> 
      <ul>
       <li>물리 메모리의 주소 범위(공간)와 다름</li> 
      </ul>
      <li>프로그래머는 자신의 프로그램이 항상 물리 주소(메모리 주소) 0번지 부터 시작해 연속적으로 배치/실행되며, 
       또한 실행시에는 CPU의 전체 주소 공간(물리 주소 공간)을 혼자만 사용할 수 있다고 착각</li> 
     </ul>
     <li>가상(virtual, 논리) 주소공간 = 사용자 공간 + 커널 공간</li>
      <ul>
       <li>각 응용프로그램 마다 2GB의 사용자 주소 공간을 가짐)</li> 
       <li>커널 공간은 2GB의 커널 주소 공간을 가짐</li> 
     </ul>
  </ul>
<img src="https://user-images.githubusercontent.com/36596037/226606861-0b380de4-e76d-498a-bac3-7608423cd86c.png">
</details>
 
 <details>
  <summary><span style="border-bottom:0.05em solid"><strong>가상(논리) 주소 공간 - 2가지 해결</strong></span></summary>
    <ul>
     <li>사용자 공간의 충돌 해결</li>
     <ul>
      <li>부분 적재의 개념</li> 
      <ul>
       <li>응용프로그램의 가상(논리) 주소 공간의 전체가 반드시 물리 메모리에 위치하지 않아도 되며, 당장 실행에 필요한 부분만 물리 메모리에 위치해도 됨 → 매핑 테이블을 이용해 관리</li> 
      </ul>
      <li>각 응용프로그램의 가상 주소 공간을 물리 주소 공간으로 매핑</li> 
      <li>여러 응용프로그램의 사용자 공간이 물리 메모리를 나누어 사용</li> 
      <li>커널 공간 역시 물리 메모리에 매핑</li> 
     </ul>
     <li>물리 메모리가 작은 경우에 대한 해결</li>
      <ul>
       <li>운영체제는 물리 메모리를 하드 디스크에 저장하여 물리 메모리의 빈 영역 확보 → 가상 메모리 기법</li> 
       <li>프로그램의 일부분 만을 물리 메모리에 적대하고 실행 → 부분 적재 (프로세스의 공간 중에서 일부분 만 물리 메모리로 적재)</li> 
     </ul>
  </ul>
<img src="https://user-images.githubusercontent.com/36596037/226607910-904c2d04-be0b-4474-bf9a-60e2d224f070.png">
<img src="https://user-images.githubusercontent.com/36596037/226607927-775d15bf-ef11-4a60-80fc-5568d1ec582e.png">
</details>
 
<details>
  <summary><span style="border-bottom:0.05em solid"><strong>사용자 모드와 커널 모드</strong></span></summary>
    <ul>
     <li>특정 시점에서 CPU는 사용자 모드와 커널 모드 중에서 하나의 모드로만 실행</li>
     <ul>
      <li>CPU 내부에 모드 상태를 나타내는 ‘(모드) 상태 레지스터’ 있음.</li> 
      <ul>
       <li>CPU 마다 구성이 다르며 상태 레지스터의 일부로 모드 비트를 지원</li> 
      </ul>
     </ul>
     <li>1) 사용자 모드(user mode)</li>
      <ul>
       <li>CPU의 모드 비트 = 1</li> 
       <li>CPU는 사용자 공간에 있는 코드나 데이터를 액세스하는 중</li> 
       <li>CPU의 커널 공간 접근 불허 → 응용프로그램으로부터 커널 영역을 보호</li> 
       <li>특권 명령(privileged instruction) 실행 불허</li> 
       <ul>
        <li>특권 명령 – 입출력 장치 등 하드웨어나 시스템 중단 등 시스템 관련 처리를 위해 설계된 특별한 명령</li> 
      </ul>
     </ul>
     <li>2) 커널 모드(kernel mode, supervisor mode)</li>
     <ul>
       <li>CPU의 모드 비트 = 0</li> 
       <li>CPU가 커널 공간에서 실행하는 중</li> 
       <li>특권 명령 사용 가능하며 모든 메모리 공간의 사용이 가능</li> 
     </ul>
  </ul>
<img src="https://user-images.githubusercontent.com/36596037/226608771-9c76e890-23b9-4b08-ad77-e1444b51060f.png">
</details>
 
<details>
  <summary><span style="border-bottom:0.05em solid"><strong>사용자 모드에서 커널 모드로의 전환</strong></span></summary>
    <ul>
     <li>사용자 모드에서 커널 모드로 전환하는 경우는 오직 두 가지 경우만 존재</li>
     <ul>
      <li>시스템 호출과 인터럽트 발생</li> 
     </ul>
     <li>1) 시스템 호출</li>
      <ul>
       <li>응용 프로그램에서 호출</li> 
       <li>시스템 호출을 실행하는 특별한 기계 명령에 의해 진행</li> 
     </ul>
     <li>2) 인터럽트 발생</li>
     <ul>
       <li>하드웨어에 의해서 발생</li> 
       <li>CPU는 인터럽트 서비스 루틴 실행</li> 
       <li>인터럽트 서비스 루틴이 끝나면 CPU는 사용자 모드로 자동 전환</li> 
     </ul>
  </ul>
<img src="https://user-images.githubusercontent.com/36596037/226609381-e6735aab-64de-4e02-ac0b-6ced7c9f0170.png">
</details>
 
 <details>
  <summary><span style="border-bottom:0.05em solid"><strong>특권 명령</strong></span></summary>
    <ul>
     <li>특권 명령 → CPU 기계어(명령어)의 일부</li>
     <ul>
      <li>입출력 장치로부터의 입출력(I/O), 시스템 중단, 컨텍스트 스위칭, 인터럽트 금지 등 특별한 목적으로 설계된 CPU 명령</li> 
      <li>커널 모드에서만 실행</li> 
     </ul>
     <li>특권 명령 종류</li>
      <ul>
       <li>I/O 명령</li> 
       <li>Halt 명령 → CPU의 작동을 중지시키는 명령. CPU를 유휴 상태로 만듦</li> 
       <li>인터럽트 플래그를 켜고 끄는 명령</li> 
       <li>타이머 설정 명령</li> 
       <li>컨텍스트 스위칭 명령</li> 
       <li>메모리 지우기 명령</li> 
       <li>장치 상태 테이블 수정 등의 명령</li> 
     </ul>
  </ul>
</details>
 
  <details>
  <summary><span style="border-bottom:0.05em solid"><strong>시스템 호출</strong></span></summary>
    <ul>
     <li>사용자 공간의 코드에서 커널 서비스를 요청하는 과정</li>
     <li>운영체제는 시스템 호출 라이브러리 제공</li>
     <li>시스템 호출은 함수 호출에 비해 많은 시간 비용 → 시스템 호출을 많이 할수록 프로그램 실행 속도 저하</li>
  </ul>
</details>
 

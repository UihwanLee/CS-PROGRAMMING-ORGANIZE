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

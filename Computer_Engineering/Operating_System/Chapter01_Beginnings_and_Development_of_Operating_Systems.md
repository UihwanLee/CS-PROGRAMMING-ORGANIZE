# Chapter01 - 운영체제의 시작과 발전

### 운영체제의 시작과 발전

```
◼ 운영체제의 정의와 목표를 알고 기능을 간단히 이해한다.
◼ 운영체제가 없던 시절에서 운영체제가 생겨나는 태동 과정을 앎으로써 운영체제의 발단과 역할을 이해한다. 
◼ 원시 운영체제 이후 운영체제의 발전 과정을 이해한다.
◼ 다중프로그래밍의 출현이 가져온 컴퓨터 시스템과 운영체제의 발전과 영향을 이해한다.
◼ 운영체제의 종류와 특징을 간단히 이해한다
```
 <hr>

### 1. 운영체제의 개념
<br>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>운영체제 정의</strong></span></summary>
    <ul>
     <li>컴퓨터 사용자와 컴퓨터 하드웨어 사이에서 중계 역할을 하면서, 프로그램의 실행을 관리하고 제어하는 시스템 소프트웨어</li> 
     <li>컴퓨터가 켜질 때 처음으로 적재되어 나머지 모든 프로그램의 실행을 제어하고 사용자의 요청을 처리해주는 소프트웨어</li>
     <li>컴퓨터의 자원을 독점적으로 관리하는 특별한 소프트웨어</li>
    </ul>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>운영체제의 정의에서 핵심 단어</strong></span></summary>
    <ol>
     <li>운영체제는 컴퓨터의 모든 자원(resource) 관리</li> 
     <ul>
      <li>하드웨어 자원 - CPU, 캐시, 메모리, 키보드, 마우스, 디스플레이, 하드디스크, 프린터 등</li> 
      <li>소프트웨어 자원 - 응용프로그램</li>
      <li>데이터 자원 - 파일, 데이터베이스 등</li>
     </ul>
     <li>운영체제는 자원에 대한 독점(exclusive) 권한 소유</li>
     <ul>
      <li>자원에 대한 모든 관리 권한은 운영체제에게 만 있음</li> 
     </ul>
     <li>운영체제는 관리자(supervisor)</li>
     <ul>
      <li>실행중인 프로그램 관리, 메모리 관리, 파일과 디스크 장치 관리, 입출력 장치 관리, 사용자 계정 등 관리 등</li> 
     </ul>
     <li>운영체제는 소프트웨어(softwarer)</li>
     <ul>
      <li>커널(kernel)이라고 불리는 핵심 코드와 UI를 비롯한 도구 프로그램들(tool/utility) 및 장치를 제어하는 디바이스 드라이버들로 구성</li> 
     </ul>
  </ol>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>운영체제의 목적</strong></span></summary>
    <ul>
     <li>사용자에게 컴퓨터 사용의 편리성 제공</li> 
     <li>컴퓨터가 켜질 때 처음으로 적재되어 나머지 모든 프로그램의 실행을 제어하고 사용자의 요청을 처리해주는 소프트웨어</li>
     <li>컴퓨터의 자원 관리 효율성</li>
    </ul>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>운영체제의 기능</strong></span></summary>
    <ol>
     <li><span style="color:red">프로세스 관리</span>(process management)</li> 
     <li><span style:"color:red">메모리 관리</span>(memory management)</li>
     <li><span style:"color:red">파일 시스템 관리</span>(file system management)</li>
     <li><span style:"color:red">장치 관리</span>(device management)</li>
     <li>네트워크 관리</li> 
     <li>보안 관리</li>
     <li>기타 관리</li>
    </ol>
 <img src="https://user-images.githubusercontent.com/36596037/226588714-5577e30b-9b4f-48a6-9e2b-b7c02bc4e864.png">
</details>

<hr>

### 2. 운영체제의 태동
<br>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>운영체제의 태동</strong></span></summary>
    <ol>
     <li>고정 프로그래밍 방식 - 1940년대</li> 
     <li>내장 프로그래밍 방식 – 1945년 이후</li>
     <li>프로그램 로딩 시대</li> 
     <li>원시 운영체제 GM OS의 탄생 - 1955년</li>
     <li>최초의 운영체제 GM-NAA I/O 개발 - 1956~1957년</li>
    </ol>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>고정 프로그램 컴퓨터(fixed program computer) </strong></span></summary>
    <ol>
     <li>운영체제에 대한 개념 없음</li> 
     <li>소프트웨어와 하드웨어의 분리 개념 없음 → 모든 것이 하드웨어로 제작</li>
    </ol>
  <img src="https://user-images.githubusercontent.com/36596037/226590784-8d635f6b-de1f-4bd6-85b1-ad63a9e1b682.png">
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>내장 프로그래밍 방식</strong></span></summary>
    <ol>
     <li>CPU와 메모리 분리</li> 
     <li>소프트웨어와 하드웨어 분리</li>
     <li>실행할 프로그램을 메모리에 담고, CPU가 프로그램을 실행하는 방식</li>
     <ul>
      <li>고정 프로그래밍 방식에 비해 획기적인 변화</li> 
      <li>하드웨어의 변화(배선 작업) 없이, 실행시키려는 프로그램만 메모리에 적재</li>
     </ul>
     <li>프로그램은 입력 장치를 통해 메모리에 적재 : 펀치 카드 -> 카드 리더기</li>
    </ol>
  <img src="https://user-images.githubusercontent.com/36596037/226590784-8d635f6b-de1f-4bd6-85b1-ad63a9e1b682.png">
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>프로그램 로더의 발견 – 운영체제 개념 시작</strong></span></summary>
    <ol>
     <li>프로그램 로딩 시대</li> 
     <li>로더 프로그램 필요</li>
     <ul>
      <li>개발자가 뒷 카드들을 메모리에 적재하는 프로그램을 첫번째 카드에 작성하는 반복되는 시간 낭비를 줄일 필요</li> 
      <li>이 코드를 로더(loader)라고 부르며 로더는 모든 사용자(개발자)에게 공통으로 필요</li> 
     </ul>
     <li>로더가 운영체제로 발전</li>
     <ul>
      <li>로더는 오늘날 운영체제의 가장 기본적인 기능</li> 
     </ul>
    </ol>
  <img src="https://user-images.githubusercontent.com/36596037/226590784-8d635f6b-de1f-4bd6-85b1-ad63a9e1b682.png">
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>최초의 운영체제 GM-NAA I/O 탄생</strong></span></summary>
    <ol>
     <li>로더 프로그램을 사용자 프로그램에서 분리하고 컴퓨터 내부에 기본으로 내장</li> 
     <li>그 당시 로더 프로그램을 모니터(Monitor)라고 불렀음</li>
     <li>운영체제 로서의 모습을 갖춤</li>
     <ul>
      <li>배치(batch) 방식 작동 → 개발자들이 작성하여 쌓아 놓은 작업들을 순서대로 하나씩 메모리에 적재, 한 번에 하나의 작업 실행</li> 
      <li>입출력 장치들을 제어하는 루틴들을 라이브러리 형식으로 갖추고 프로그램 사이에 공유 → 개발자는 입출력 코드를 작성할 필요 없음</li> 
     </ul>
     <li>IBM 704에서 GM-NAA-I/O 운영체제의 작동</li>
    </ol>
</details>

<hr>

### 3. 운영체제의 발전
<br>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>운영체제의 스케줄링 기법</strong></span></summary>
    <ul>
     <li>멀티 프로그래밍(Multi-programming) = 다중 프로그래밍</li>
     <ul>
      <li>단일 CPU 상에서 여러 프로그램을 메모리에 올리고 현재 실행 중인 프로세스가 입출력 작업을 요청하고 결과를 기다릴 동안 다른 프로세스를 수행할 수 있도록 하는 기법 → CPU 사용 효율 높임</li> 
     </ul>
     <li>멀티 태스킹(Multi-tasking)</li>
     <ul>
      <li>단일 CPU 상에서 다수의 작업(Task)을 운영체제 스케줄링에 의해 시간을 쪼개어(시분할) 번갈아 가면서 처리 → 동시 실행은 아니다</li> 
      <li>사용자에게는 다수의 작업이 동시에 처리되는 것처럼 느끼게 할 수 있다</li> 
     </ul>
     <li>멀티 프로세싱(Multi-processing)</li>
     <ul>
      <li>다수의 CPU/코어가 다수의 프로세스를 협력적으로 동시에 처리하는 것을 의미</li> 
     </ul>
     <li>멀티 스레딩(Multi-threading)</li>
     <ul>
      <li>다수의 CPU/코어가 프로세스(들)를 여러 개의 스레드들로 나누고 각 스레드들을 협력적으로 동시에 처리하는 것을 의미</li> 
     </ul>
    </ul>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>배치(Batch) 운영체제</strong></span></summary>
    <ul>
     <li>출현 배경</li>
     <ul>
      <li>컴퓨터의 노는 시간(idle 시간, 유휴시간)을 줄여 컴퓨터의 활용률 향상</li> 
     </ul>
     <li>배치 운영체제 컴퓨터 시스템</li>
     <ul>
      <li>개발자와 관리자의 구분하고 개발자는 펀치 카드를 입력 데크에 두고 결과 기다림</li> 
      <li>배치 운영체제는 자동으로 테이프 장치에 대기중인 프로그램을 한 번에 하나씩 적재하고, 실행</li> 
     </ul>
    </ul>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>다중프로그래밍(Multiprogramming) 운영체제 </strong></span></summary>
    <ul>
     <li>출현 배경</li>
     <ul>
      <li>배치 작업은 프로그램의 실행 형태로 인한 CPU의 유휴시간(idle 시간) 발생</li> 
     </ul>
     <li>다중프로그래밍 기법 출현</li>
     <ul>
      <li>미리 여러 프로그램을 메모리에 적재 → 메모리가 수용할 만큼 다수의 프로그램 적재</li> 
      <li>프로그램 실행 도중 I/O가 발생하면, CPU에게 메모리에 적재된 다른 프로그램 실행시킴 → CPU 활용률 증가</li> 
     </ul>
    </ul>
 <img src="https://user-images.githubusercontent.com/36596037/226593910-ae81615a-0f46-4db6-b9ff-6075ef3331de.png"> 
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>시분할 다중프로그래밍(Time Sharing Multiprogramming) 운영체제</strong></span></summary>
    <ul>
     <li>줄여서 시분할 운영체제라고 부름</li>
     <li>출현 배경</li>
     <ul>
      <li>배치 처리와 당시 다중프로그래밍의 다음 2가지 문제점 인식</li> 
      <ul>
       <li>1) 비 대화식 처리방식(non-interactive processing)</li> 
       <li>2) 느린 응답시간, 오랜 대기 시간 → 프로그램을 제출하고 하루 후에 결과 보기, 사용자의 즉각적인 대응 없음</li> 
      </ul>
     </ul>
     <li>초기 컴퓨터 시스템의 운영체제이나 근래의 운영체제들(Unix, Linux, Windows)도 시분할의 개념을 기초로 한다</li>
    </ul>
 <img src="https://user-images.githubusercontent.com/36596037/226594373-6b0ee776-a8c1-4527-b718-dc77dd94770e.png"> 
</details>

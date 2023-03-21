# 프로세스와 프로세스 관리

### 1. 프로세스 개요

 <br>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>프로그램(program)</strong></span></summary>
    <ul>
     <li>하드디스크 등의 저장 매체에 저장되어 있는 실행이 가능한 파일</li>
  </ul>
</details>
<details>
  <summary><span style="border-bottom:0.05em solid"><strong>프로세스(process)</strong></span></summary>
    <ul>
      <li>프로그램이 메모리(주기억장치)에 적재되어 실행 중인 프로그램</li>  
      <ul>
       <li>필요한 모든 자원(코드 공간, 데이터 공간, 스택 공간, 힙 공간)을 할당 받음</li> 
     </ul>
    </ul> 
    <details>
    <summary><span style="border-bottom:0.05em solid"><strong>프로세스의 특징(Computer Architecture)</strong></span></summary>
     <ul>
      <li> 운영체제는 프로그램을 메모리 적재하고 프로세스로 다룸 (프로그램 → 프로세스)</li>
      <li> 운영체제는 프로세스에게 실행에 필요한 메모리 할당하고 이곳에 코드와 데이터 등 적재</li>
      <li> 프로세스들은 서로 독립적인 메모리 공간을 가짐. 다른 프로세스의 영역에 접근 불허(보호)</li>
      <li> 운영체제는 각 프로세스의 메모리 위치와 크기 정보를 관리한다.</li>
      <li> 운영체제는 프로세스마다 고유한 번호(프로세스 ID) 할당</li>
      <li> 프로세스의 관한 모든 정보는 커널에 의해 관리</li>
      <li> 프로세스는 실행 – 대기 – 잠자기 – 대기 – 실행 - 종료 등의 생명 주기를 가짐</li>
      <li> 프로세스 생성, 실행, 대기, 종료 등의 모든 관리는 커널에 의해 수행</li>
    </ul>

</details>
  </ul>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>프로세스 관리</strong></span></summary>
    <ul>
     <li>프로세스의 생성에서 종료까지, 관리는 모두 커널에 의해 이루어짐</li> 
     <ul>
      <li>커널은 커널 영역에 프로세스 테이블(시스템에 한 개만 존재)을 만들고, 이 테이블을 이용해 프로세스들 목록을 관리</li>
     </ul>
  </ul>
</details>


<details>
  <summary><span style="border-bottom:0.05em solid"><strong>CPU 주소 공간 (CPU address space)</strong></span></summary>
    <ul>
      <li>CPU가 주소선을 통해 액세스할 수 있는 전체 물리 메모리 공간</li>
      <li>CPU 주소 공간 크기</li>
       <ul>
        <li>CPU 주소선(An-1 ~ A0)의 수에 의해 결정</li>
        <ul>
         <li>cPU → 32개의 주소선(A31 ~ A0) 지원 → 232 개의 주소 → 232 바이트 → 4GB 주소 공간</li>
        </ul>
        <li>하나의 번지에 할당되는 저장 공간 크기는 1B(바이트)이며 주소 공간은 0 번지부터 시작</li>
       </ul>
      <li>CPU 주소 공간보다 큰 메모리?</li>
       <ul>
        <li>있어도 액세스 불가능</li>
       </ul>
      <li>CPU 주소 공간보다 작은 양의 메모리?</li>
       <ul>
        <li>가능하며 CPU가 설치된 메모리의 주소 영역을 넘어 액세스하면 시스템 오류</li>
        <ul>
          <li>예) 32비트 CPU를 가진 컴퓨터(4GB까지 메모리 액세스 가능)에 2GB의 메모리가 설치되어 있을 때 2GB를 넘어서 액세스하면없는 메모리를 액세스하므로 심각한 오류 발생               </li>
        </ul>
      </ul>
  </ul>
</details>
<details>
  <summary><span style="border-bottom:0.05em solid"><strong>프로세스 구성 - 4개의 메모리 영역 - 1/2</strong></span></summary>
    <ul>
     <li>프로그램이 운영체제에 의해 프로세스로 변경되면 항상 사용자 공간에 4개의 구성 요소가 생성됨</li>
      <ul>
       <li>이 영역을 ‘프로세스 (영역)’ 또는 ‘프로세스 이미지‘ 라고도 표현</li>
      </ul>
     <li>4개의 메모리 영역(프로세스)</li>   
      <ul>
       <li>① 코드(code) 영역</li>  
       <li>② 데이터(data) 영역</li>  
       <li>③ 힙(heap) 영역</li>  
       <li>④ 스택(stack) 영역</li> 
     </ul>
     <li>각 영역의 특성 및 공유 사용(메모리 사용량 절약)을 위해서 4개의 영역으로 분리</li>  
     <li>프로세스의 크기는 CPU가 액세스 할 수 있는 범위보다 클 수 없으며</li>  
     <li>프로세스의 크기는 프로세스 마다 달라짐</li>
     <ul>
      <li>각 프로그램 마다 코드, 데이터 등의 크기가 다르기 때문임</li>   
      <li>또한 실행 중에도 힙 영역, 스택 영역의 크기가 달라져 프로세스의 크기가 변함</li>  
     </ul>
  </ul>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>프로세스 구성 - 4개의 메모리 영역 - 2/2</strong></span></summary>
    <ol>
     <li>코드(code) 영역</li>
      <ul>
       <li>실행될 프로그램 코드가 적재되는 영역</li>
       <li>사용자가 작성한 모든 함수의 코드와 사용자 코드에서 호출한 라이브러리 함수들의 코드</li>
      </ul>
     <li>데이터(data) 영역</li>   
      <ul>
       <li>프로그램에서 고정적으로 만든 변수 공간</li>  
       <li>사용자 프로그램과 라이브러리에서 선언한 전역 변수 공간(정적 데이터 포함)이 위치</li>  
     </ul>
     <li>힙(heap) 영역</li>
     <ul>
       <li>프로세스의 실행 도중에 동적으로 사용할 수 있도록 미리 할당한 공간</li>  
       <li>malloc() 등으로 할당 받는 공간은 힙 영역에서 할당</li>
       <li>힙 영역에서 아래 번지로 내려가면서 할당</li>
     </ul>
     <li>스택(stack) 영역</li>  
     <ul>
       <li>함수가 실행될 때 사용될 임시로 사용되는 정보를 위해 할당된 공간</li>  
       <ul>
        <li>지역변수들, 매개변수들, 함수 종료 후 돌아갈 주소 등</li>  
        <li>함수는 호출될 때, 스택 영역에서 위쪽으로 공간 할당되고,</li>
        <li>함수가 return하면 할당된 공간 반환</li>
       </ul>
       <li>함수 호출 외에 프로세스에서 필요시 사용 가능</li>
     </ul>
  </ol>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>프로세스 주소 공간</strong></span></summary>
    <ul>
     <li>프로세스가 실행 중에 접근할 수 있도록 허용된 주소의 최대 범위 → 2장에서 배운 가상 주소 공간</li>
     <li>프로세스 주소 공간은 가상 공간(논리 공간)이며 항상 0번지에서 시작하는 연속적인 주소프로세스 주소 공간은 가상 공간(논리 공간)이며 항상 0번지에서 시작하는 연속적인 주소</li>
    </ul>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>프로세스 주소 공간의 크기</strong></span></summary>
    <ul>
     <li>프로세스 주소 공간의 크기는 프로세스의 현재 크기와 다름</li>
     <li>프로세스 주소 공간의 크기 = CPU가 액세스할 수 있는 전체 크기</li>
     <ul>
      <li>32비트 CPU의 경우 4GB(윈도우, 리눅스 모두 동일)</li>
     </ul>
    </ul>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>프로세스의 크기</strong></span></summary>
    <ul>
     <li>①적재된 코드 + ②전역 변수 + ③힙 영역에서 현재 할당 받은 동적 메모리 공간 + ④스택 영역에 현재 저장된 데이터 크기</li>
     <li>③힙 영역은 프로세스 실행 중에 추가로 할당을 받거나 사용 후 다시 반납 → 크기가 가변적</li>
     <li>④스택 영역은 함수의 호출과 함께 할당되며, 완료되면 소멸 → 컴파일 시 최대 크기가 결정되며 실행시에 크기가 가변적</li>
     <li>결론적으로 프로세스의 크기는 실행하면서 변화된다</li>
    </ul>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>프로세스의 사용자 공간과 커널 공간</strong></span></summary>
    <ul>
     <li>프로세스 주소 공간 = 사용자 공간 + 커널 공간</li>
    </ul>
    <ol>
     <li>사용자 공간</li>
     <ul>
      <li>프로그램의 크기와 프로세스의 크기는 다르다</li>
      <li>프로세스의 코드, 데이터, 힙, 스택 영역이 순서대로 할당되는 공간</li>
      <li>힙은 데이터 영역 바로 다음부터 시작하고, 스택은 사용자 공간의 바닥에서 시작하여 거꾸로 자람 → 힙과 스택은 가변</li>
     </ul>
     <li>커널 공간</li>
     <ul>
      <li>프로세스가 시스템 호출을 통해 이용하는 커널 공간</li>
      <li>커널 코드, 커널 데이터, 커널 스택(커널 코드가 실행될 때)이 존재</li>
     </ul>
    </ol>
    <ul>
     <li>프로세스의 현재 크기와 관련된 결론</li>
     <ul>
      <li>프로세스의 코드와 데이터는 실행 파일에 결정된 상태로 코드 영역과데이터 영역에 적재 → 실행 중에 크기가 불변</li>
      <li>프로세스는 사용자 공간의 최대 범위까지 동적할당을 받으면서 힙 영역과 스택 영역을 늘려갈 수 있음 → 실행 중에 크기가 가변</li>
      <li>프로세스의 실질적인 현재 크기는 고정부분인 ①코드/②데이터 영역과 ③현재 할당 받은 힙 영역, ④현재 사용중인 스택 영역의 합으로 결정</li>
      <li>따라서 프로세스의 현재 크기는 실행 중에 수시로 변한다</li>
      <li>미할당 영역은 실행시에 메모리에 할당되지 않기 때문에 현재의 프로세스 크기 계산에서는 제외</li>
     </ul>
     <li>각 프로세스는 독립된 사용자 공간을 소유하며 하나의 커널 공간 공유<li>
     <li>커널 공간의 활용<li>
     <ul>
      <li>프로세스가 사용자 코드에서 시스템 호출을 통해 커널 코드 실행할 때 커널 공간 사용</li>
     </ul>
     <li>사용자 공간과 커널 공간의 결론<li>
     <ul>
      <li>프로세스마다 각각 사용자 주소 공간이 있다.</li>
      <li>시스템 전체에는 하나의 커널 주소 공간이 있다.</li>
      <li>모든 프로세스는 커널 주소 공간을 공유한다</li>
     </ul>
 </ul>
</details>
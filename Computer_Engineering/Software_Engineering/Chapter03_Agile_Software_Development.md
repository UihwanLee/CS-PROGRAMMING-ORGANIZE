# Chapter03 Agile Software Development

### Agile Software Development

```
애자일 소프트웨어 개발 방법을 이해한다.
◼ 애자일 소프트웨어 개발 방법의 근거, 애자일 선언을 이해하고 애자일과 계획 주도 개발의 차이점을 이해한다.
◼ 사용자 스토리, 리팩토링, 짝 프로그래밍과 테스트 우선 개발 등 중요한 애자일 개발 실무를 이해한다.
◼ 애자일 프로젝트 관리를 위한 스크럼(Scrum)을 이해한다.
◼ 대규모 소프트웨어 시스템을 개발하면서 애자일 개발 방법의 규모를 확장하고, 애자일 접근법과 계획 주도 방식을 결합하는 문제를 이해한다
```
 <hr>

### 1. Agile Software Development
<br>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>애자일 철학 4가지</strong></span></summary>
    <ul>
      <li>Individuals and interactions(의사소통과 상호작용)</li> 
      <li>Working software(문서화보다 개발에 집중)</li>
      <li>Customer collaboration(이해당사자와의 협업/협력)</li>
      <li>Responding to change(변경된 일정에 빠른 적응)</li>
   </ul>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>개요</strong></span></summary>
    <ul>
     <li>비즈니스 요구사항</li> 
     <ul>
      <li>소프트웨어를 빨리 개발하고, 배포해야 함</li> 
      <li>대부분의 비즈니스 시스템에서 가장 중요한 요구사항</li>
    </ul>
     <li>요구사항의 변경</li> 
     <ul>
      <li>시스템이 설치되고 사용자가 시스템을 경험한 후, 요구사항이 명확해짐</li> 
    </ul>
     <li>계획 주도 소프트웨어 개발 프로세스</li> 
     <ul>
      <li>요구사항 명세, 시스템 설계, 구축, 테스트의 프로세스는 신속한 SW 개발에 적합하지 않음</li> 
    </ul>
     <li>애자일 기법의 특징</li> 
     <ul>
      <li>1. 명세화, 설계 및 구현 프로세스가 중첩됨</li> 
      <li>2. 시스템을 증가분의 연속으로 구현</li>
      <li>3. 개발 프로세스를 지원하기 위해 방대한 도구를 사용하게 됨</li>
    </ul>
     <li>애자일 기법</li> 
     <ul>
      <li>2~3주마다 새로운 시스템을 만들어서 고객이 사용</li> 
      <li>요구사항에 대한 피드백을 빨리 확보하기 위해 고객이 개발 프로세스에 참여</li>
      <li>비공식적인 커뮤니케이션을 통해 문서화를 최소화</li>
    </ul>
   </ul> 
   <img src="https://user-images.githubusercontent.com/36596037/226624210-5571fa1b-db1c-4efa-86cf-ab34abddf3c1.png">  
</details>

<hr>

### 2. Agile Methods
<br>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>애자일 기법</strong></span></summary>
    <ul>
     <li>계획 주도 접근법</li> 
     <ul>
      <li>시스템에 대한 계획, 설계 및 문서화에 오버헤드가 많이 발생</li> 
    </ul>
     <li>애자일 기법</li> 
     <ul>
      <li>개발팀이 설계와 문서 작업보다는 소프트웨어 자체에 더 집중할 수 있도록 함</li> 
      <li>요구사항이 자주 변경되는 애플리케이션 개발에 적합</li> 
    </ul> 
     <li>애자일 기법의 적용</li> 
     <ul>
      <li>소프트웨어 회사가 중소 규모의 제품을 판매할 목적으로 개발하는 경우</li> 
      <li>고객이 개발 프로세스에 참여하겠다는 확실한 의사가 있고, 소프트웨어에 영향을 줄 수 있는 외부 이해당사자나 규제가 거의 없는 조직 내에서 
       이루어지는 맞춤형 시스템 개발인 경우</li> 
      <li>독립형 시스템인 경우</li> 
    </ul> 
   </ul>
   <img src="https://user-images.githubusercontent.com/36596037/226625270-cf8da44b-f607-4102-963a-3ceb134f86ba.png">  
 <img src="https://user-images.githubusercontent.com/36596037/226625274-b238f16e-ab2c-42c4-a751-95f18093e80c.png">  
</details>

<hr>

### 3. Agile Development Techniques
<br>

     
 <details>
  <summary><span style="border-bottom:0.05em solid"><strong>사용자 스토리</strong></span></summary>
    <ul>
     <li>소프트웨어 요구사항</li> 
     <ul>
      <li>애자일 기법에서는 요구 변경을 처리하기 위해 별도의 요구공학 활동을 두지 않음</li> 
      <li>요구사항을 구현하는 데 드는 노력과 자원을 추정</li>
    </ul>
     <li>사용자스토리의 주요 문제점</li> 
     <ul>
      <li>완전성</li> 
      <ul>
       <li>시스템의 중요한 요구사항 전체를 다룰 수 있을 정도로 충분한 사용자 스토리를 만들었는지 판단이 어려움</li> 
       <li>하나의 스토리가 어떤 활동에 대해 제대로 된 그림을 보여주는 것인지를 판단하기 어려움</li> 
     </ul> 
    </ul> 
   </ul>
   <img src="https://user-images.githubusercontent.com/36596037/226626470-88c47a53-4fbd-462d-95a8-b894bc98c930.png">  
</details>

 <details>
  <summary><span style="border-bottom:0.05em solid"><strong>짝 프로그래밍</strong></span></summary>
    <ul>
     <li>스크럼(Scrum)</li> 
     <ul>
      <li>애자일 프로젝트를 조직화하기 위한 프레임워크를 제공</li> 
      <li>진행중인 내용에 대한 외부 가시화를 제공</li>
    </ul>
     <li>Scrum sprint cycle</li> 
     <ul>
      <li>스프린트 주기는 보통 2~4주</li>  
      <li>팀은 완료 가능하다고 생각하는 가장 높은 우선순위의 항목을 선택</li>  
      <li>스프린트를 거치는 동안, 진척도를 점검하고 필요한 경우 업무의 우선순위를 변경하기 위해 팀은 매일 짧은 미팅인 스크럼을 진행</li>  
      <li>스크럼팀 사이에 매일 이루어지는 상호작용은 스크럼 보드를 통해 조정이 이루어짐</li>  
      <li>각 스프린트가 끝날 대는 모든 팀이 점검 미팅을 함</li>  
    </ul> 
   </ul>
</details>
<hr>

### 3. Agile Project Management
<br>
     
 <details>
  <summary><span style="border-bottom:0.05em solid"><strong>애자일 프로젝트 관리</strong></span></summary>
    <ul>
     <li>스크럼(Scrum)</li> 
     <ul>
      <li>애자일 프로젝트를 조직화하기 위한 프레임워크를 제공</li> 
      <li>진행중인 내용에 대한 외부 가시화를 제공</li>
    </ul>
     <li>Scrum sprint cycle</li> 
     <ul>
      <li>스프린트 주기는 보통 2~4주</li>  
      <li>팀은 완료 가능하다고 생각하는 가장 높은 우선순위의 항목을 선택</li>  
      <li>스프린트를 거치는 동안, 진척도를 점검하고 필요한 경우 업무의 우선순위를 변경하기 위해 팀은 매일 짧은 미팅인 스크럼을 진행</li>  
      <li>스크럼팀 사이에 매일 이루어지는 상호작용은 스크럼 보드를 통해 조정이 이루어짐</li>  
      <li>각 스프린트가 끝날 대는 모든 팀이 점검 미팅을 함</li>  
    </ul> 
   </ul>
   <img src="https://user-images.githubusercontent.com/36596037/226627240-2410c109-7fef-4b1b-8f69-fdb514b6855c.png"> 
   <img src="https://user-images.githubusercontent.com/36596037/226627251-14ae8377-7fca-4cfa-8768-2160783145e2.png"> 
</details>


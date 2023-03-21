# Chapter02 SoftWare Process

### SoftWare Process

```
소프트웨어공학에 대한 기본 개념을 이해한다.
◼ 소프트웨어 공학이란 무엇이며, 왜 중요한지를 이해한다.
◼ 소프트웨어 엔지니어에게 윤리적이고 직업적인 문제가 중요함을 이해한다.
◼ 교재에서 사용하는 예제, 네 가지 다른 유형의 시스템을 살펴본다
```
 <hr>

### 1. 소프트웨어 프로세스
<br>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>소프트웨어 공학 활동에 대한 비용 분포</strong></span></summary>
 <img src="https://user-images.githubusercontent.com/36596037/226615006-08623875-9f91-4a84-a991-cc42a661ba74.png"> 
  ※ 현실에서는 위의 사진대로 소프트웨어 개발이 진행되지 않는다!
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>소프트웨어 공학 : 계층적 기술</strong></span></summary>
 <img src="https://user-images.githubusercontent.com/36596037/226615519-19adc586-b070-48ca-8ca9-234f7ae8f1c4.png"> 
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>소프트웨어 프로세스</strong></span></summary>
    <ul>
     <li>고품질의 소프트웨어를 구축하는데 요구되는 작업으로 구성된 단계</li> 
     <li>좋은 품질의 소프트웨어를 얻기 위한 업무의 프레임워크</li>
    </ul>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>소프트웨어 개발의 기본적인 단계</strong></span></summary>
 <img src="https://user-images.githubusercontent.com/36596037/226615941-a024fbc0-c323-4ac3-b238-5fafc8ca4237.png"> 
</details>

 <hr>

### 2. 소프트웨어 프로세스 모델 (Software Process Model)
<br>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>소프트웨어 프로세스 모델</strong></span></summary>
    <ul>
     <li>정의(Definition)</li> 
     <ul>
      <li>소프트웨어 프로세스의 추상적인 표</li> 
     </ul>
     <li>각 프로세스 모델</li>
     <ul>
      <li>특정 관점에서의 프로세스를 나타냄</li> 
     </ul>
     <li>프로세스 모델의 종류</li>
     <ul>
      <li>폭포수(Waterfall) 모델</li>
      <li>프로토타입(Prototype, 시제품화) 모델</li>
      <li>RAD(Rapid Application Development) 모델</li>
      <li>진화적 개발</li>
      <li>진화적 모델</li>
      <ul>
        <li>나선형(Spiral) 모델</li>
        <li>점진적(Incremental) 모델</li>
        <li>동시적 개발(Concurrent Development) 모델</li>
      </ul>
      <li>형식 방법론(Formal Method) 모델</li>
      <li>컴포넌트-기반 소프트웨어 공학 (CBSE ; Component-Based Software Engineering)</li>
      <li>애자일(Agile) 프로세스</li>
      <li>RUP(Rational Unified Process)</li>
     </ul>
    </ul>
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>폭포수(Waterfall) 모델</strong></span></summary>
    <ul>
     <li>특징</li> 
     <ul>
      <li>소프트웨어 공학에서 가장 오래되고, 가장 폭넓게 사용된 전통적인 소프트웨어 생명주기 모델</li> 
      <li>소프트웨어 개발 과정의 앞 단계가 끝나야만 다음 단계로 넘어갈 수 있는 선형 순차적(Linear Sequential) 모델</li>
      <li>다음 단계를 수행하기 위해 각 단계가 끝난 후에는 결과물이 명확하게 산출되어야 함</li> 
    </ul>
   </ul>
  <img src="https://user-images.githubusercontent.com/36596037/226617931-377dc2a6-9526-4cd5-b24b-52a24c6b45cc.png">  
  <img src="https://user-images.githubusercontent.com/36596037/226617949-e32f154f-69b6-4976-8673-29996bc73e68.png">  
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>프로토타입(Prototype) 모델</strong></span></summary>
    <ul>
     <li>특징</li> 
     <ul>
       <li>사용자의 요구사항을 정확히 파악하기 위해 실제 개발될 소프트웨어에 대한 견본(시제)품(Prototype)을 들어 최종 결과물을 예측하는 모델</li> 
       <li>소프트웨어 개발이 완료된 시점에서 오류가 발견되는 폭포수 모델의 단점을 보완하기 위한 모델</li>
       <li>요구분석 단계에서 사용하며, 프로토타입의 평가가 끝나고 개발이 승인되면 다른 모형을 이용하여 개발이 이루어짐</li> 
       <li>프로토타입은 고객의 요구를 만족시킬 때까지 과정이 반복됨</li> 
       <li>고객은 동작하는 프로그램의 겉모습만을 볼 뿐이지, 그 내부의 정돈되지 못한 복잡성이나 긴 안목에서 갖추어야 할 품질이나 유지성을 인식하지 못함</li>
    </ul>
   </ul>
  <img src="https://user-images.githubusercontent.com/36596037/226618592-e8bb9fc2-1a44-4cff-95aa-20d90e22a767.png">  
  <img src="https://user-images.githubusercontent.com/36596037/226618613-68359ee9-eb64-4fab-b533-4b493132ce28.png">  
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>RAD 모델</strong></span></summary>
    <ul>
     <li>특징</li> 
     <ul>
       <li>아주 짧은 개발주기를 가지는 점진적 소프트웨어 개발 방식</li> 
       <li>RAD 모델은 컴포넌트를 사용하여 매우 빠르게 선형 순차적 모델을 적용시킬 수 있음</li>
       <li>시간의 제약은 RAD를 사용한 프로젝트가 확장 가능한 규모를 가지도록 만듬</li> 
       <li>만약 비즈니스 애플리케이션의 주요 기능들이 모듈화 될 수 있고, 각각의 기능들이 3달 안에 완성 가능하다면, RAD가 사용될 수 있음</li> 
       <li>각각의 기능들은 각각의 RAD 팀들에게 할당되어 개발된 후, 나중에 통합되어질 수 있음</li>
    </ul>
   </ul>
  <img src="https://user-images.githubusercontent.com/36596037/226619355-ff1f0416-2825-4ecd-930f-f4a2066084fb.png">  
  <img src="https://user-images.githubusercontent.com/36596037/226619371-ae5f5631-393e-4f01-a123-34cafa1421b0.png">  
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>진화적 개발</strong></span></summary>
    <ul>
     <li>특징</li> 
     <ul>
       <li>초기에 구현을 시작하고, 그것을 이용하여 사용자의 의견을 반</li> 
       <li>적당한 시스템이 개발될 때까지 계속해서 버전을 다듬어 감</li>
       <li>명세화, 개발, 검증 활동은 서로 교차하며 활동 사이에 빠른 피드백이 교환됨</li> 
    </ul>
   </ul>
  <img src="https://user-images.githubusercontent.com/36596037/226619769-b47db0d4-12a5-46e6-9cd7-6c9f37b8b189.png">  
  <img src="https://user-images.githubusercontent.com/36596037/226619784-37b5f158-2ed2-4c8c-a79d-85e41be69028.png">  
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>나선형(Spiral) 모델</strong></span></summary>
    <ul>
     <li>특징</li> 
     <ul>
      <li>Boehm이 제안</li> 
      <li>폭포수 모델과 프로토타입 모델의 장점에 위험분석 기능을 추가한 모델</li>
      <li>나선을 따라 돌듯이 여러 번의 소프트웨어 개발 과정을 거쳐 점진적으로(프로토타입을 지속적으로 발전시켜) 완벽한 최종 소프트웨어를 개발(점진적 모델 이라고도 힘)</li>
      <li>소프트웨어를 개발하면서 발생할 수 있는 위험을 관리하고, 최소화하는 것을 목적으로 함</li>
      <li>프로세스가 진행됨에 따라 소프트웨어도 진화하기 때문에, 고객과 개발자는 각 진화적 프로세스의 위험을 이해하고 해결해야 함</li>
      <li>프로토타입은 위험(risk)을 줄이는 기능을 가짐</li>
    </ul>
   </ul>
  <img src="https://user-images.githubusercontent.com/36596037/226620386-4fa2ae3f-cb54-4da2-abd3-7be776e61bf8.png">  
  <img src="https://user-images.githubusercontent.com/36596037/226620396-3b496e7a-f63f-49ea-b15b-149515fc87dc.png">  
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>점진적(Incremental) 모델</strong></span></summary>
    <ul>
     <li>특징</li> 
     <ul>
      <li>Boehm이 제안</li> 
      <li>폭포수 모델(선형 순차적 모델)에 프로토타입 모델의 반복 개념을 추가한 모델</li>
      <li>다른 모델들과 접목이 가능</li>
      <li>프로토타입과는 달리 점진적 모델은 실제로 작동하는 결과물을 만들어냄</li>
      <li>프로젝트 기간동안 한번에 모든 기능을 구현할 수 없을 때 유용하게 사용됨</li>
      <li>최초의 제품은 적은 인력으로 개발하고, 제품이 널리 쓰여지게 되면 인력을 증원하여 다른 추가 사항들을 개발함</li>
      <li>기술적인 위험을 관리할 수 있음</li>
    </ul>
   </ul>
  <img src="https://user-images.githubusercontent.com/36596037/226620881-24dfc5f9-104a-4adc-95b0-7850901a348a.png">  
  <img src="https://user-images.githubusercontent.com/36596037/226620892-ac1c1b18-76b8-49c3-9db6-077f448dad98.png">  
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>동시적(Concurrent) 개발 모델</strong></span></summary>
    <ul>
     <li>특징</li> 
     <ul>
      <li>Boehm이 제안</li> 
      <li>분석 절차는 언제나 일어날 수 있는 상태(state) 중 하나이며, 다른 절차(설계, 고객과의 의사소통) 역시 그와 비슷하게 표현함</li>
      <li>모든 절차들은 동시에 존재할 수 있지만, 모두 다른 상태(state)에 있음</li>
      <li>소프트웨어 절차에서의 각 상태마다, 한 상태에서 다른 상태로 넘어갈때 발생하는 트리거 이벤트들을 정의</li>
      <li>클라이언트/서버 애플리케이션 개발에서 자주 사용됨</li>
      <li>클라이언트/서버에 두 가지 차원으로 적용됨</li>
      <li>동시적 개발 모델은 모든 종류의 소프트웨어 개발에서 사용될 수 있음</li>
    </ul>
   </ul>
  <img src="https://user-images.githubusercontent.com/36596037/226621440-352da3bf-a28f-4c0e-abc8-b69c45dcead9.png">   
</details>

<details>
  <summary><span style="border-bottom:0.05em solid"><strong>형식 방법론(Formal Method) 모델</strong></span></summary>
    <ul>
     <li>특징</li> 
     <ul>
      <li>형식방법론(Formal Method) 모델은 컴퓨터 소프트웨어의 사양을 수학적인 식으로 표현한 것</li> 
      <li>설계 과정에서 형식방법론이 사용되면 프로그램의 검증(Verification)의 기준으로 사용되어 이전에 쉽게 감지할 수 없었던 에러들을 발견하고 수정할 수 있음</li>
      <li>모든 절차들은 동시에 존재할 수 있지만, 모두 다른 상태(state)에 있음</li>
      <li>형식방법론을 적용하기 위한 조건</li>
      <ul>
       <li>1. 형식방법론을 사용한 개발은 많은 시간과 비용이 필요</li> 
       <li>2. 개발자가 형식방법론을 사용한 개발을 수행하려면 많은 교육이 필요</li>
       <li>3. 형식방법론을 이용한 모델을 이용하면 그 내용을 잘 모르는 고객과 의사소통 하기 어려움</li>
       /ul>
      <li>형식방법론 접근방법</li>
      <ul>
       <li>고도의 안정성을 요구하는 소프트웨어를 만들려는 개발자들과 에러로 발생하는 비용 때문에 고민하는 개발자들에게 많은 도움을 줌</li> 
       <li>비행 관제 소프트웨어, 의료 기기 소프트웨어</li>
       /ul>
    </ul>
   </ul> 
</details>
    
<details>
  <summary><span style="border-bottom:0.05em solid"><strong>컴포넌트-기반 소프트웨어 공학</strong></span></summary>
    <ul>
     <li>특징</li> 
     <ul>
      <li>대부분의 소프트웨어 프로젝트는 약간의 소프트웨어를 재사용한다.</li> 
      <li>진화적 방법의 경우, 신속한 시스템 개발에 재사용이 필수적이다.</li>
      <li>비공식적인 재사용은 사용된 개발 프로세스에 관계없이 일어난다.</li>
      <li>재사용에 의존하는 컴포넌트 기반 소프트웨어 공학(CBSE; Component-based Software Engineering)</li>
      <li>재사용 지향 방법은 재사용이 가능한 많은 소프트웨어 컴포넌트가 있고 이 컴포넌트를 통합할 수 있는 틀이 있어야 함</li>
    </ul>
   </ul> 
   <img src="https://user-images.githubusercontent.com/36596037/226622540-1875cd5a-5a39-4fc8-99fd-1e148007fb10.png">  
  <img src="https://user-images.githubusercontent.com/36596037/226622541-9bacbd24-ac91-425d-95d4-e744fe6eccf6.png"> 
</details>
     
<details>
  <summary><span style="border-bottom:0.05em solid"><strong>CBSE 프로세스</strong></span></summary>
  <img src="https://user-images.githubusercontent.com/36596037/226622847-519769d4-d36f-41c8-ba2e-4928cb13667a.png"> 
</details>
     
<details>
  <summary><span style="border-bottom:0.05em solid"><strong>CBSE 프로세스</strong></span></summary>
  <img src="https://user-images.githubusercontent.com/36596037/226622847-519769d4-d36f-41c8-ba2e-4928cb13667a.png"> 
</details>

 <hr>

### 3. Agile Software Development
<br>

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

 <hr>

### 4. Rational Unified Process
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
     


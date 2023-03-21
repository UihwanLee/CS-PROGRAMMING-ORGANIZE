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

<br>


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


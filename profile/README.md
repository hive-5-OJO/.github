## 고객 데이터 기반 고객 분석 서비스, OJO 👋
LG 유플러스 유레카 SW 교육과정 3기 최종 융합 프로젝트 <br />
진행 기간: 2026.02.04 ~ 2026.03.19 (6주)

## 💡 개요
> 고객 데이터 기반 고객 분석 서비스 "OJO"는 고객에 대한 정보를 손쉽게 볼 수 있는 CRM 서비스입니다. </br>
> 상담 서비스 데이터로 고객들의 성향과 특성을 만들어 고객들에게 적합한 서비스를 제공해줄 수 있습니다. </br>
> 마케터, 상담사 등이 이 서비스를 이용하여 고객의 RFM, LTV, 코호트 분석, 상담 통계 등을 조회할 수 있습니다.

[서비스 관련 사진 - 추후 추가 예정]
<div align="center">
	
### 🔗 [OJO 바로가기 (서비스 출시 예정) ](https://github.com/hive-5-OJO)


</div>

<br/>
<br/>

## 🔧 기능 소개 
**1. 회원 관리 시스템** : 소셜 로그인 및 회원가입

**2. 고객 특성 생성 시스템** : 상담 데이터를 통해 고객의 특성을 생성

**3. 고객 관리 시스템** : 고객들의 개인정보 및 상담, 특성, 통계 자료 등을 조회 

**4. 고객 분석 시스템** : 고객 특성을 활용하여 RFM, LTV, 코호트 분석 진행

**5. 고객 필터링 시스템** : 분류된 고객을 필터링

**6. 보기 손쉬운 UI/UX** : 어떤 관리자가 와도 보기 쉬우며 통계 자료를 통해 일을 이어갈 수 있는 화면

**7. 추천 시스템** : 고객에게 맞는 새로운 상품 추천
화면

<br/>
<br/>

## ⚙️ 기술 스택
<kbd>
  <img width="391" height="550" alt="image" src="https://github.com/user-attachments/assets/803993e0-430d-4ca5-aa60-61e4b1acee7c" style="border:1px solid black;"/>
</kbd>


<br/>
<br/>
<br/>


## 🖼️ 와이어프레임
<kbd>
  <img width="794" height="722" alt="image" src="https://github.com/user-attachments/assets/26140628-0aff-4c0d-8469-53337a2a55c9" style="border:1px solid black;"/>
</kbd>

<br/>
<br/>
<br/>

## 🛠️ 시스템 아키텍쳐
<kbd>
  <img width="1198" height="566" alt="image" src="https://github.com/user-attachments/assets/662dd3c7-1933-4858-8305-77439fa02bf6" style="border:1px solid black;"/>
</kbd>


<br/>
<br/>
<br/>


## 🎯 서버 실행 방법
```
docker-compose up --build
```
### Setup
```
application.properties
docker-compose.yml
```


<br/>
<br/>


## 🏛️ 디렉토리 구조 예시
### Spring
```
java/org/backend
├── common (예외 처리, 공통 응답, 유틸리티)              
├── config (Security, Elasticsearch, Database 설정)              
├── domain               
│   ├── member           // 회원 도메인
│   │   ├── controller   
│   │   ├── service      
│   │   ├── entity       
│   │   ├── document     
│   │   ├── repository   
│   │   │   ├── MemberRepository.java     ///jpa  
│   │   │   └── MemberSearchRepository.java //엘라스틱 서치
│   │   └── dto          
│   ├── advice           // 상담 도메인
│   │   ├── ... (위와 동일 구조)
│   ├── analysis           // 분석 도메인(RFM, LTV 등)
│   │   ├── ... (위와 동일 구조)
│   │   └── batch 
│   ├── auth           // 권한 관리 도메인(로그인, 회원가입 등)
│   │   ├── ... (위와 동일 구조)
│   └── dummy           // 더미 데이터 도메인(필요시)
│       └─ ... (위와 동일 구조)
├── global  // (전역 변수 등)
└── infra (파이썬 연동을 위한 코드)
```
### FAST API
```
app
├── api
│   ├── routes.py 혹은 api.py
│   └─ ...            
├── core (설정, 보안, 환경변수)
├── crud (DB 접근 로직)
├── db (Session 관리)
├── models (DB Table 정의)
├── schemas (Pydantic DTO)             
├── services (비즈니스 로직, AI 모델 추론 logic)
├── tests (단위 테스트)
└── main.py
```
### React
```
├── src
│   ├── App.tsx
│   ├── Router.tsx
│   ├── assets (이미지, 폰트 등)
│   ├── common (공통으로 사용하는 값들)
│   │   ├── components
│   │   ├── constants
│   │   ├── hooks
│   │   ├── styles
│   │   ├── types
│   │   └── utils
│   ├── main.tsx
│   ├── pages (페이지)
│   │   ├── detail 
│   │   │   ├── components (페이지 내에서 사용할 컴포넌트)
│   │   │   ├── stores (페이지 내에서 사용할 스토어)
│   │   │   ├── hooks (페이지 내에서 사용할 커스텀 훅)
│   │   │   └── index.tsx
│   │   ├── main
│   ├── service (서버와 통신시 필요한 파일)
│   │   ├── apis
│   │   └── googleAnalytics
│   ├── stores (공통으로 사용하는 스토어)
...
```


<br/>
<br/>

## 📌 ERD
<kbd>
  <img width="1251" height="802" alt="image" src="https://github.com/user-attachments/assets/9159b7b5-0b98-4478-883a-8607c43d499a" style="border:1px solid black;"/>
</kbd>
<p>
  🔗 <a href="https://www.erdcloud.com/d/XRr2FYBQWb9c6aDbb" rel="nofollow">ERDCloud</a>  
</p>

<br/>
<br/>


## 📋 Conventions 

**1. Git 브랜치 전략**
> **Github-Flow** <br>
> 기본적으로 Github Flow를 따라 개발 프로세스를 진행한다. </br>
> 이는 기능별 브랜치를 생성하고, 코드 리뷰 후 develop 브랜치에 병합하는 방식을 의미한다.

<br>

**2. Git 컨벤션**
<details>
<summary><b>Types</b></summary>
<div markdown="1">

  - `feat`: 새로운 기능  
  - `fix`: 버그 수정  
  - `build` : 빌드 관련 수정
  - `refact`: 기능 변경 없이 코드 구조 개선
  - `docs`: 문서 수정 (README 등)
  - `style` : 코드 스타일, 포맷팅에 대한 수정
  - `test`: 테스트 코드 추가 또는 수정  
  - `ci`: 환경 설정 관련 
  - `chore`: 그 외의 작은 수정들  
  - `release`: 운영 서버 배포  

</div>
</details>

<br>

**3. 브랜치 명명 및 커밋 메시지 규칙**
- 이슈 생성 후 타입-기능명/SV-jira 티켓 넘버를 추가하여 브랜치를 생성한다.  
  예) `feat-login/SV-1`
- 브랜치를 로컬에 받아 개발한다.  
- 구현됨에 따라 자주 커밋한다. 한번에 모아서 커밋하지 않는다.  
- 커밋 메시지는 지정된 컨벤션에 따른다.
  예) `feat-login/SV-1: 버튼 컴포넌트 구현`

**4. 코드 리뷰 및 PR 관리**
- PR을 생성한다. 이때 PR없이 절대 develop 브랜치에 merge하지 않는다.  
- 지정된 template을 이용해 구현한다. 이때 PR 제목은 issue와 같은 형식으로 작성한다.
  예) `feat-login/SV-1: 버튼 컴포넌트 구현`  
- PR은 커밋 메시지와 마찬가지로 여러 업무를 모아서 보내지말고 자주 보내 conflict를 줄여야 한다.  
- 가능한 지정된 팀원이 코드 리뷰를 해주고, 1인 이상 approve하면 본인이 develop에 merge하며 2인 이상 approve해야 메인 브랜치에 푸쉬할 수 있다.

<br/>

## 🗓️ 추진 일정
  <kbd>
    <img width="392" height="237" alt="image" src="https://github.com/user-attachments/assets/57f49843-8316-4c3a-a3cd-3596250dc8f4" style="border:1px solid black;"/>
  </kbd>

<br/>
<br/>

## 🗂️ 최종 산출물
<p>
  🔗 <a href="https://docs.google.com/document/d/1IA3aemwprWEOuCamw_Dw9_QiXL1PVmh5sXY9W3w6VXE/edit?tab=t.0" rel="nofollow">기획안</a>  
</p>
<p>
  🔗 <a href="https://docs.google.com/spreadsheets/d/1zTmq07KIJewBkjpWgwM-iPLYnlfmLgdv13Dlkvx56bc/edit?gid=90508790#gid=90508790" rel="nofollow">기능 명세서</a>  
</p>

## 👥 팀원 및 역할 소개

<table>
  <tr align="center">
    <td>김영우</td>
    <td>류종현</td>
    <td>권태환</td>
    <td>박진우</td>
    <td>박현수</td>
    <td>이재혁</td>
    <td>정현서</td>
    <td>홍세민</td>
  </tr>
  <tr>
     <td align="center">
        <a href="https://github.com/0andrich">
          <img src="https://avatars.githubusercontent.com/u/139140907?v=4" width="150px" alt="김영우"/><br />
        </a>
     </td>
     <td align="center">
        <a href="https://github.com/jonghyunRyu">
          <img src="https://avatars.githubusercontent.com/u/80243566?v=4" width="150px" alt="류종현"/><br />
        </a>
     </td>
     <td align="center">
        <a href="https://github.com/hwantae">
          <img src="https://avatars.githubusercontent.com/u/73492261?v=4" width="150px" alt="권태환"/><br />
        </a>
     </td>
     <td align="center">
        <a href="https://github.com/Norang2810">
          <img src="https://avatars.githubusercontent.com/u/84859429?v=4" width="150px" alt="박진우"/><br />
        </a>
     </td>
     <td align="center">
        <a href="https://github.com/bakyunsu00">
          <img src="https://avatars.githubusercontent.com/u/68821547?v=4" width="150px" alt="박현수"/><br />
        </a>
     </td>
     <td align="center">
        <a href="https://github.com/ljh5918">
          <img src="https://avatars.githubusercontent.com/u/151804624?v=4" width="150px" alt="이재혁"/><br />
        </a>
     </td>
     <td align="center">
        <a href="https://github.com/Jung-Que">
          <img src="https://avatars.githubusercontent.com/u/108854679?v=4" width="150px" alt="정현서"/><br />
        </a>
     </td>
     <td align="center">
        <a href="https://github.com/semsemin">
          <img src="https://avatars.githubusercontent.com/u/114004065?v=4" width="150px" alt="홍세민"/><br />
        </a>
     </td>
  </tr>
  <tr>
     <td align="center">
        <p> PM, <br /> 인프라 및 <br /> RFM, LTV <br /> 로직 구현, <br /> 알림 구현</p>
     </td>
     <td align="center">
        <p> FE <br /> 로그인, <br />회원 관리, <br /> 분석 페이지 구현</p>
     </td>
     <td align="center">
        <p>분석 서버, <br /> 상담 통계, <br />코호트 분석<br /> 로직 구현, <br /> 고객 맞춤 <br />상품 추천, <br /> 이탈률 예측 구현</p>
     </td>
     <td align="center">
        <p> 더미 데이터 생성, <br /> 권한 관리 <br /> 구현</p>
     </td>
     <td align="center">
        <p> 엘라스틱<br />서치, <br /> 대시보드 및 <br />알림 구현</p>
     </td>
     <td align="center">
        <p> 배치를 통해 <br /> 고객 특성 <br />생성, <br /> 이탈률 예측 구현</p>
     </td>
     <td align="center">
        <p> 더미 데이터 생성, <br /> 권한 관리 <br /> 구현</p>
     </td>
     <td align="center">
        <p> 고객 관리 및 <br /> 프론트 구현</p>
     </td>
  </tr>
</table>

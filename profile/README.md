## 고객 데이터 기반 고객 분석 서비스, OJO 👋
LG 유플러스 유레카 SW 교육과정 3기 최종 융합 프로젝트 <br />
진행 기간: 2026.02.04 ~ 2026.03.19 (6주)

## 💡 개요
> 고객 데이터 기반 고객 분석 서비스 "OJO"는 고객에 대한 정보를 손쉽게 볼 수 있는 CRM 서비스입니다. </br>
> 상담 서비스 데이터로 고객들의 성향과 특성을 만들어 고객들에게 적합한 서비스를 제공해줄 수 있습니다. </br>
> 마케터, 상담사 등이 이 서비스를 이용하여 고객의 RFM, LTV, 코호트 분석, 상담 통계 등을 조회할 수 있습니다.

[서비스 관련 사진]
<div align="center">
<img width="2874" height="1436" alt="로그인/구글" src="https://github.com/user-attachments/assets/6efcafae-f6f4-433e-89fd-20ed2d5997a9" />
<img width="2870" height="1348" alt="대시보드" src="https://github.com/user-attachments/assets/5e86946e-6d1d-4823-a132-943ed3d8b57d" />
<img width="2859" height="1434" alt="고객 목록" src="https://github.com/user-attachments/assets/d6bebfb5-a85b-49e9-9883-0d483b660d25" />
<img width="2870" height="776" alt="채널" src="https://github.com/user-attachments/assets/2b7977fa-ad34-437d-b9db-6a6cc3dfb5b2" />

<img width="1576" height="1431" alt="기본 정보" src="https://github.com/user-attachments/assets/21dba0d6-d697-4507-b8f0-ac9288c66bf6" />
<img width="1568" height="1424" alt="특성 정보" src="https://github.com/user-attachments/assets/e223fc7a-5b5b-4632-ae5c-590e676efe84" />
<img width="1569" height="1429" alt="rfm 분석" src="https://github.com/user-attachments/assets/25f96806-1fad-4dfc-9569-40a38189197c" />
<img width="1580" height="1431" alt="ltv 분석" src="https://github.com/user-attachments/assets/57b46ec0-83cd-4070-bd95-7ea0ad6394da" />
<img width="2877" height="1450" alt="상담 이력" src="https://github.com/user-attachments/assets/dfd85043-37ce-41a7-adc1-ba0f18034450" />

<img width="2879" height="1122" alt="rfm kpi" src="https://github.com/user-attachments/assets/ec23ff25-2ca3-46cd-b2cd-105a5156041d" />
<img width="2875" height="1196" alt="코호트" src="https://github.com/user-attachments/assets/3e9a2bf8-fe62-4576-92bc-d44b68825275" />
<img width="2879" height="1432" alt="지역 기반 분석" src="https://github.com/user-attachments/assets/1f5489eb-1f06-4c86-b229-703fcf5eb3ee" />

<img width="2873" height="1093" alt="관리자 페이지" src="https://github.com/user-attachments/assets/476ac33e-67bf-4627-b0eb-a6742952d65b" />


	
### 🔗 [OJO 바로가기](http://high5-ojo.s3-website.ap-northeast-2.amazonaws.com)


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

**번외) 더미 데이터** : 10만건

<br/>
<br/>

## ⚙️ 기술 스택
<kbd>
  <img width="389" height="541" alt="image" src="https://github.com/user-attachments/assets/e936193c-f5c3-4adb-ab52-e7d377cb3f92" />
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
.env
```


<br/>
<br/>


## 🏛️ 디렉토리 구조 예시
### Spring
```
java/org/backend
├── common 							// 예외 처리, 공통 응답, 유틸리티              
├── config 							// Security 설정              
├── domain               
│   ├── admin            			// 관리자 도메인
│   │   ├── controller
│   │   ├── dto      
│   │   ├── entity    
│   │   ├── repository   
│   │   └── service
│   ├── advice           			// 상담 도메인
│   │   ├── ... (위와 동일 구조)
│   │   ├── document 	 			# Elasticsearch 관련  
│   │   ├── formatter          
│   │   └── view  
│   ├── analysis         			// 분석 도메인(RFM, LTV 등)
│   │   ├── ... (admin과 동일 구조)
│   ├── auth             			// 권한 관리 도메인(로그인, 회원가입 등)
│   │   ├── ... (위와 동일 구조)
│   │   ├── interceptor 	  
│   │   ├── oauth          
│   │   └── security
│   ├── batch
│   │   ├── ... (admin과 동일 구조)
│   │   ├── config 	  
│   │   ├── job          
│   │   └── scheduler
│   ├── channel
│   │   ├── ... (admin과 동일 구조)
│   ├── member          			// 회원 도메인
│   │   ├── ... (위와 동일 구조)
│   │   └── document 
│   ├── subscription
│   │   ├── ... (admin과 동일 구조)
└── scheduler  						// Elasticsearch 설정
```
### FAST API
```
app
├── analyzer 		// 분석 로직         
├── churn 			// 이탈률 예측 모델
├── model 			// 맞춤 추천 상품 로직
├── database.py 	// db연동
└── main.py 		// API 및 CORS 등 기본 설정
```
### React
```
src/
├── assets/           		# 정적 자원 (이미지, 아이콘, 폰트 등) 
├── components/       		# 재사용 가능한 UI 컴포넌트
│   ├── auth/         		# 권한 관리 레이아웃 (로그인, 회원가입 등)
│   └── common/       		# 공통 레이아웃 (에러 처리 등)
├── entities/           	# 도메인 모델, API, 데이터 스키마 (핵심 비즈니스 로직)
│   └── domain명/
│       ├── api/        	# 백엔드 서버와의 데이터 통신 로직 (Axios instance 등)
│       ├── model/      	# 도메인 관련 상태 정의, 데이터 페칭 훅 (Types, Query Hooks)
│       └── index.ts    	# 도메인 외부 노출을 위한 통합 엔트리 (Barrel File)
├── features/           	# 사용자 인터렉션을 통한 기능 단위 (버튼 클릭, 폼 제출 등 액션)
│   ├── admin/          	# 관리자 기능 
│   ├── auth/           	# 인증 기능 
│   └── customer/       	# 고객 관련 기능 
├── pages/              	# 각 도메인별 페이지 컴포넌트
│   ├── admin/          	# 관리자 설정 및 제어 페이지
│   ├── analysis/       	# 데이터 분석 전문 페이지 (코호트, RFM 상세 등)
│   ├── auth/           	# 로그인 및 회원가입 페이지
│   ├── channels/       	# 채널 관리 및 상세 정보 페이지
│   ├── customers/      	# 전체 고객 목록 및 검색 페이지
│   ├── dashboard/      	# 핵심 지표 요약 및 대시보드 메인 페이지
│   ├── not-found/      	# 404 에러 페이지
│   └── ui-showcase/    	# UI 컴포넌트 테스트 및 가이드 페이지
├── shared/             	# 프로젝트 전역에서 사용되는 독립적인 공통 모듈 계층
│   ├── api/            	# API 클라이언트 설정
│   ├── constants/      	# 전역 상수 관리 (경로, API 엔드포인트, 고정 메시지)
│   ├── hooks/          	# 비즈니스 로직이 없는 공통 유틸리티 훅
│   ├── lib/            	# 외부 라이브러리 설정 및 래핑 
│   ├── types/          	# 전역에서 공통으로 사용되는 타입 정의
│   ├── ui/             	# 디자인 시스템 기반의 UI 컴포넌트
│   └── utils/          	# 순수 함수 기반 공통 유틸리티 (마스킹, 날짜 포맷팅 등)
├── widgets/            	# Entity와 Feature를 조합하여 독립적으로 작동하는 큰 단위 UI
├── App.tsx           		# RouterProvider 및 Provider 설정
├── main.tsx          		# 앱 엔트리 포인트
└── routes.tsx        		# React Router를 이용한 경로 설정
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
     <td align="center" width="12.5%">
        <a href="https://github.com/0andrich">
          <img src="https://avatars.githubusercontent.com/u/139140907?v=4" alt="김영우"/><br />
        </a>
     </td>
     <td align="center" width="12.5%">
        <a href="https://github.com/jonghyunRyu">
          <img src="https://avatars.githubusercontent.com/u/80243566?v=4" alt="류종현"/><br />
        </a>
     </td>
     <td align="center" width="12.5%">
        <a href="https://github.com/hwantae">
          <img src="https://avatars.githubusercontent.com/u/73492261?v=4" alt="권태환"/><br />
        </a>
     </td>
     <td align="center" width="12.5%">
        <a href="https://github.com/Norang2810">
          <img src="https://avatars.githubusercontent.com/u/84859429?v=4" alt="박진우"/><br />
        </a>
     </td>
     <td align="center" width="12.5%">
        <a href="https://github.com/bakyunsu00">
          <img src="https://avatars.githubusercontent.com/u/68821547?v=4" alt="박현수"/><br />
        </a>
     </td>
     <td align="center" width="12.5%">
        <a href="https://github.com/ljh5918">
          <img src="https://avatars.githubusercontent.com/u/151804624?v=4" alt="이재혁"/><br />
        </a>
     </td>
     <td align="center" width="12.5%">
        <a href="https://github.com/Jung-Que">
          <img src="https://avatars.githubusercontent.com/u/108854679?v=4" alt="정현서"/><br />
        </a>
     </td>
     <td align="center" width="12.5%">
        <a href="https://github.com/semsemin">
          <img src="https://avatars.githubusercontent.com/u/114004065?v=4" alt="홍세민"/><br />
        </a>
     </td>
  </tr>
  <tr>
     <td align="center">
        <p> [PM] <br /> 인프라, <br /> RFM 배치, <br /> 상담 통계, <br /> 상품 추천</p>
     </td>
     <td align="center">
        <p> [FE] <br /> 로그인, <br />회원 관리, <br /> 분석 페이지,<br />발표</p>
     </td>
     <td align="center">
        <p>[PY/DA] <br />분석 배치, <br /> LTV 로직, <br />코호트 분석, <br /> 보고서 생성</p>
     </td>
     <td align="center">
        <p>[IAM/ML] <br /> 권한 관리, <br /> 상담 통계, <br /> 이탈률 예측</p>
     </td>
     <td align="center">
        <p>[Search] <br />엘라스틱<br />서치, <br /> 고객 필터링, <br />대시보드, <br />영상 제작</p>
     </td>
     <td align="center">
        <p>[BE/Core] <br /> 고객 특성 <br />배치, <br /> 고객 메모, <br />고객 채널</p>
     </td>
     <td align="center">
        <p>[QA] <br />더미 데이터, <br /> 정합성 검증,<br />ppt 제작 </p>
     </td>
     <td align="center">
        <p>[CX/Search]<br /> 고객 관리, <br /> 프론트 보조</p>
     </td>
  </tr>
</table>

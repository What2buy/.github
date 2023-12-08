# 뭐 찾으세요?: 온라인 가상 점원 서비스


### **🏆2023 이화여대 캡스톤 디자인과 창업프로젝트A 포스터 세션 장려상 수상**
### **🏆2023 이화여대 캡스톤디자인경진대회 융합 부문 동상 수상**


## 프로젝트 소개

사용자의 자유로운 언어적 요청을 해석해 상품을 찾아주고 상품에 대한 정보제공 질의응답을 제공하는 1:1 쇼핑 도우미 챗봇 서비스

## 프로젝트 목적
기존의 온라인 쇼핑몰은 방대한 상품 정보 및 리뷰 확인으로 인한 사용자의 많은 시간과 수고로움을 필요로 하는 문제가 발생함. 온라인 쇼핑에도 오프라인의 점원처럼 고객의 자유로운 자연어 요청을 이해하고 상품 데이터를 활용하고 다른 고객의 경험을 종합적으로 고려해 사용자 맞춤형 쇼핑 서비스 제공이 필요됨. 원하는 상품 및 스타일을 자유롭게 검색창에 입력하거나 채팅창에 상품에 대해 궁금한 점을 입력해 1:1 대화형 채팅을 통해 점원과 대화하듯 사용자에게 즉각적인 응답을 제공하는 서비스를 개발하고자 함.


## 프로젝트 기술
1. 생성형 AI + LangChain을 활용한 Prompt Engineering
* 사용자 요청에 따른 상품 목록, 구매에 결정적인 정보 요약, 사이즈 통계, 유용한 리뷰 및 불만 리뷰 요약하는 4가지 프롬프트 구성
* 사용자의 언어적 자유도를 유지하면서 모델의 효과적인 상품 검색 진행
* 다양한 데이터로부터 필요한 정보 요약 및 상품 목록 제공을 위한 포맹팅 
  
2. Text Embedding와 Vector DB을 활용한 질의응답
* 사용자 요구에 부합하는 정보만 추출해 사용자 요청에 대한 정확한 대응 및 답변 제공
  
3. Selenium과 Google Cloud Run을 활용한 실시간 브러우저 조작을 통한 실시간 데이터 수집
   
4. 기존 쇼핑몰 UI과 대화형 UI 혼합한 인터페이스 개발


## 웹사이트 
https://preeminent-fudge-566432.netlify.app/

## 시연 영상
[유투브 시연 영상](https://youtu.be/kU2kh1HcYP4?feature=shared)

## 서비스 시나리오
![Service Flow](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FXCSOD%2FbtsiOHaZXuD%2FJ2NNaPCC8urxb9AVehSeyK%2Fimg.png)

## 포스터
![포스터](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FkA6zE%2FbtsBvSr9U0S%2FqTnDHGRR7tsgFk4M6KhbRk%2Fimg.png)

## 레포지토리 구성
**1. AI : 프롬프트**
https://github.com/What2buy/what2buy-AI

**2. Front-end : 웹 클라이언트**
https://github.com/What2buy/whaat2Buy-FE

**3. Back-end : 웹 서버**
https://github.com/What2buy/whaat2Buy-BE

## 실행 환경 및 방법

**0. 실행 환경**

다음의 과정을 통해 서비스 실행에 필요한 모든 파일 빌드 가능
`node.js`, `npm`, `git` 설치가 요구됨

```
$ node -v
v20.8.0

$ npm -v
10.2.0

$ git -v
git version 2.39.2
```

**1. 프로젝트 clone**
```
git clone https://github.com/Solchall/whaat2Buy-FE.git
```

**2. 프로젝트 폴더로 이동**
```
cd whaat2Buy-FE
```
**3. 환경 변수 파일 생성**

다음의 내용이 담긴 `.env` 파일을 base directory에 추가 작성함
```
REACT_APP_AI_API=https://what2buy-o3mazxvlva-du.a.run.app
REACT_APP_SERVER_API=https://whaat2buy-be.onrender.com/api
```

**4. 실행에 필요한 패키지 설치**
```
npm i
```

**5. 프로젝트 실행**

기본 주소는 http://localhost:3000, 해당 주소로 접속
```
npm start
```

**6.테스트 계정 로그인**

다음의 테스트 계정을 통해 로그인 가능
```
email: test3@gmail.com
password: 1234567890a!
```


## 🧑‍💻 팀원
<table border="1" cellspacing="0" cellpadding="0" width="60%">
    <tr width="100%">
        <td width="33%" align="center"><a href= "https://github.com/minha62">하수민</a></td>
        <td width="33%" align="center"><a href= "https://github.com/erica00j">정유리</a></td>
        <td width="33%" align="center"><a href= "https://github.com/JangAyeon">장아연</a></td>
    </tr>
    <tr width="90%">
        <td width="33%" align="center"><img src = "https://github.com/minha62.png"></td>
        <td width="33%" align="center"><img src = "https://github.com/erica00j.png"/></td>
        <td width="33%" align="center"><img src = "https://github.com/JangAyeon.png"/></td>
    </tr>
    <tr width="100%">
        <td width="30%" align="center">
          팀장 & AI & BE
          </td>
        <td width="30%" align="center">
        AI & BE
        </td>
        <td width="30%" align="center">
        FE & BE & 웹 서비스 배포
        </td>

   </tr>
</table>


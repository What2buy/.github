# 뭐 찾으세요?: 온라인 가상 점원 서비스


### **🏆2023 이화여대 캡스톤 디자인과 창업프로젝트A 포스터 세션 장려상 수상**
### **🏆2023 이화여대 캡스톤디자인경진 대회 융합 부문 장려상 수상**
```
[제출 source code]
반드시 github.com에 upload해야 함. (기존 사용하던 repository를 제출해도 됨)
Repo가 여러 개인 경우, 해당 내용을 모두 기술 (구글 form: shift-enter 이용)
채점 기준: 여러분 과제를 git clone해서 다시 re-generate할 수 있는가?
기본 설명 (README.md)
반드시 code를 만들어 낼 수 있는 방법 or script 를 repo에 포함 + Script (예, makefile?) 포함
Proto-system을 설치할 수 있는 방법 설명 + script를 포함
데이터가 필요한 경우, sample or proto-data 포함 (DB, 파일, object등)
연구 트랙의 경우, 실험 데이터 / 실험 결과물을 반드시 포함
Open source를 가져다 사용하는 경우, 해당 내용을 반드시 README.md에 포함할 것.

[시제품]
휴대폰 app인 경우, apk / PC 혹은 외부 comput의 app인 경우, executable code + data (tar/zip 형태)
Server의 경우, executable / runtime data (필요한) 포함 / 동작 환경 관련 정보 (서버 주소/테스트 계정등)
README 혹은 README.install 파일.
실물/앱 다운로드 파일(.apk), 웹 접속주소, 테스트계정이 사전 제공해야함


[기본 설명 (README.md)]
Source code에 대한 설명
How to build
How to install
How to test
Description of sample data (if any)
Description of used open source (if any)

[참고 깃허브-강계]
https://github.com/chuckchuck-gojol/wiing-wiing
```

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
REACT_APP_OPEN_AI_KEY=아마 없어도 잘 돌아갈텐디 좀 확인 해봐
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



# 이 밑에 내용 지워야 함!!!!!
## 👗 Prototype

[프로토타입 동적 구현 영상](https://youtu.be/StQJ4zX_bko)

<br>


## 👒 Prompt Engineering and LLMs with Langchain
### 1. 상품 DB 필터링 API
소스코드: [Solchall/filtering-prompt](https://github.com/Solchall/filtering-prompt) <br>

<img width="500" alt="image" src="https://github.com/Solchall/.github/assets/71062967/69c7ef0a-5243-4163-ad1b-365e327b5de6">
<br>

- apikey: [OpenAI API KEY](https://platform.openai.com/account/api-keys)
- prompt: 찾고싶은 상품(현재는 상의 한정)에 대한 설명

<br>

[FastAPI docs](https://hidden-anchorage-81661.herokuapp.com/docs)에서 이 API를 테스트 해볼 수 있습니다. <br>
1. `/lang/` > `Try it out`을 클릭 <br>
2. `apikey`에 해당하는 `string`에 본인의 [OpenAI API key](https://platform.openai.com/account/api-keys) 넣기 <br>
3. `prompt`에 해당하는 `string`에 찾고싶은 상품(현재는 상의 한정)에 대해 적기 <br>
   - 예시1) 40,000원 이하 스프라이트 블랙 니트를 찾아줘 
   - 예시2) 4만원대 브라운 맨투맨 추천해줘. 4개월 동안 판매가 많은순으로 정렬해줘 
   - 예시3) 10만원 이하로 베이지 린넨소재 셔츠 찾아줘. 3달내 리뷰순으로 정렬해줘 

![image](https://github.com/Solchall/.github/assets/71062967/9339ce58-73c9-4427-ac94-bd2035126ecd)




<br>

### 2. 컨텐츠 DB 선정 API
소스코드: [Solchall/filtering-magazine](https://github.com/Solchall/filtering-magazine) <br>

<img width="500" alt="image" src="https://github.com/Solchall/.github/assets/71062967/50ca84cf-28a3-4ff8-828f-736761ead0a3">
<br>

- apikey: [OpenAI API KEY](https://platform.openai.com/account/api-keys)
- prompt: 찾고싶은 매거진에 대한 설명

<br>

[FastAPI docs](https://gentle-sands-05392.herokuapp.com/docs)에서 이 API를 테스트 해볼 수 있습니다. <br>
1. `/magazine/` > `Try it out`을 클릭 <br>
2. `apikey`에 해당하는 `string`에 본인의 [OpenAI API key](https://platform.openai.com/account/api-keys) 넣기 <br>
3. `prompt`에 해당하는 `string`에 찾고싶은 매거진에 대해 적기 <br>
   - 예시1) 요즘 트렌디한 상의 찾아줘
   - 예시2) 뉴진스가 입을 것 같은 옷 알려줘
   - 예시3) 바캉스 갈 때 입을 옷 추천해봐

![image](https://github.com/Solchall/.github/assets/71062967/4effd7ce-ee19-4a2d-a92f-7a45e8240fe4)


### 4. 시연 및 테스팅 영상
* [깃허브 소스 코드 레포](https://github.com/Solchall/chrome-extension/tree/main/Crawl%20Multi%20Tabs%20-%20React)
* [시연 및 테스팅 영상](https://drive.google.com/file/d/176k4IrIkyV97IYE2huRrtBUHC6b9FOly/view)

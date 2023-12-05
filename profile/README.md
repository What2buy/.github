# 뭐 찾으세요?: 온라인 가상 점원 서비스


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
## 레포지토리 구성
**1. AI : 프롬프트**
추가해줭~

**2. Front-end : 웹 클라이언트**
https://github.com/Solchall/whaat2Buy-FE

**3. Back-end : 웹 서버**
https://github.com/Solchall/whaat2Buy-BE

## 실행 방법
0. 실행 환경
node.js 설치
git 설치
```
node -v

npm -v

git -v
```

2. clone github repository
```
git clone https://github.com/Solchall/whaat2Buy-FE.git
```

2. move to project folder as base directory
```
cd whaat2Buy-FE
```

3. make `.env` file in base directory
```
REACT_APP_AI_API=https://what2buy-o3mazxvlva-du.a.run.app
REACT_APP_OPEN_AI_KEY=아마 없어도 잘 돌아갈텐디 좀 확인 해봐
REACT_APP_SERVER_API=https://whaat2buy-be.onrender.com/api
```

4. how to install package
```
npm i
```

5. how to build project
```
npm run build
```

6. how to start
```
npm start
```

7. how to login
테스트 계정 정보
```
email: 웅앵웅앵@gmail.com
password: 1234567890a!
```

## 시제품 웹사이트 
웹사이트 링크~~

## 시연 영상
유트브 링크~~~

## 👕 Service Flow
![Service Flow](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FXCSOD%2FbtsiOHaZXuD%2FJ2NNaPCC8urxb9AVehSeyK%2Fimg.png)

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

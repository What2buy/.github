# 뭐 찾으세요?: 온라인 가상 점원 서비스

## Prototype

[Figma](https://www.figma.com/proto/yS1dxiMOGnS8T1DuY0D3aB/%EC%95%84%ED%82%A4%ED%85%8D%EC%B3%90?page-id=201%3A6&type=design&node-id=308-499&viewport=106%2C618%2C0.04&scaling=scale-down&starting-point-node-id=308%3A94)

![캡스톤_동적프로토](https://github.com/Solchall/.github/assets/71062967/540e803c-e885-4967-b428-3e9083b0f4d4)

<br>


## Prompt Engineering and LLMs with Langchain
### 상품 DB 필터링 API
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

### 컨텐츠 DB 선정 API
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

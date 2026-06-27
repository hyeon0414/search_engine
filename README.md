<img src="https://capsule-render.vercel.app/api?type=Transparent&color=0A0A0A&height=100&section=header&text=search%20engine&fontSize=50" />

python - exa, dotenv

## **1. exa-py 라이브러리**
### Search
  ```
# 시카고 최고의 콜드 브루 검색 결과 중 10개
response = exa.search(
    'Best Chicago cold brew',
    num_results = 10,)
```

> * query : 검색 내용
>
> * num_results : 결과 개수 설정
>
> * startPublishedDate/endPublishedDate : 해당 기간 내에 발행된 페이지
>
> * include_domains/exclude_domains : 특정 도메인을 검색에 포함/제외
>
> * category : 특정 유형 검색

### Result
```
Title: 20 Best Iced Coffee Drinks to Try in Chicago
URL: https://www.timeout.com/chicago/restaurants/best-iced-coffee-in-chicago
ID: https://www.timeout.com/chicago/restaurants/best-iced-coffee-in-chicago
Score: None
Published Date: 2024-07-18T05:00:00.000Z
Author: None
Image: https://media.timeout.com/images/102595028/image.jpg
Favicon: https://www.timeout.com/static/root-files/favicon.ico
Extras: None
Subpages: None
Crawl Date: None
Text: 20 Best Iced Coffee Drinks to Try in Chicago
...
```




  * AI 검색 엔진으로 api 키 필요
  * 공식문서 : [https://exa.ai/docs/sdks/python-sdk](https://exa.ai/docs/reference/search-api-guide-for-coding-agents)

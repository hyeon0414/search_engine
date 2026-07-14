<img src="https://capsule-render.vercel.app/api?type=Transparent&color=0A0A0A&height=100&section=header&text=search%20engine&fontSize=50" />

python - exa, dotenv 활용해 검색 엔진 개발

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

### Search
```
# 틱톡에서 최고의 커피 음료 관련 계정을 찾기
# https://www.tiktok.com 에서 나온 검색 결과 중 상위 5개만
query = input('Search here: ') # 사용자의 입력으로 쿼리 받기

response = exa.search(
    query,
    num_results=5 ,
    type='keyword',
    include_domains=['https://www.tiktok.com'],
)
```

### Result (coffee)
```
Title: coffee
URL: https://www.tiktok.com/tag/coffee
ID: https://www.tiktok.com/tag/coffee
Score: None
Published Date: None
Author: None
Image: https://p16-sg.tiktokcdn.com/obj/tiktok-obj/24552381a53125ba59471c5cb8b75ed1.png?shp=81f88b70&shcp=-
Favicon: https://www.tiktok.com/favicon.ico
Extras: None
Subpages: None
Crawl Date: None
Text: #coffee | TikTok
[**TikTok**](https://www.tiktok.com/)
Log in**
[
**TikTok**](https://www.tiktok.com/)
Search
[
For You
](https://www.tiktok.com/)
[
Explore
](https://www.tiktok.com/explore)
[
Following
](https://www.tiktok.com/following)
[
Upload
](https://www.tiktok.com/tiktokstudio/upload)
[
LIVE
](https://www.tiktok.com/live)
[
Profile
](https://www.tiktok.com/@)
More
Log in
#### Company
#### Program
#### Terms & Policies
©2025 TikTok
![](https://p16-sg.tiktokcdn.com/obj/tiktok-obj/24552381a53125ba59471c5cb8b75ed1.png?shp=81f88b70&shcp=-)
# #coffee
## 14.1M posts
We're celebrating International Coffee Day! Share your favourite coffee hacks, recommendations and stories with us!
[
![haven’t been able to check-in with y’all in a hot minute 🥺hope you’re all well 💕#coffeewithcy #coffee #psl #pumpkinspice #cylovesfrogs #checkin created by Cy 🐸with Greg’s Fall Sounds](https://p19-pu-sign-useast8.tiktokcdn-us.com/tos-useast5-p-0068-tx/0f5886c0658e4bb28de9a204e000ab58_1649283911~tplv-dmt-logom:tos-useast5-p-0000-tx/600721f3b7464b4b88130d4b2fe44476.image?lk3s=b59d6b55&x-expires=1739638800&x-signature=Kv%2FW91CJ%2B5369SNbH7H0rSke178%3D&shp=b59d6b55&shcp=-)  
[![Cy 🐸,cylovesfrogs](https://p16-common-sign-va.tiktokcdn-us.com/tos-maliva-avt-0068/7328635617629274117~tplv-tiktokx-cropcenter:100:100.jpeg?dr=9640&nonce=74812&refresh_token=789d76afd8dd25f31ede8c0102423ef5&x-expires=1739638800&x-signature=lhnWCcNUR3Rt8LBwyhoit33Gdo0%3D&idc=useast5&ps=13740610&shcp=b59d6b55&shp=a5d48078&t=4d5b0474)](https://www.tiktok.com/@cylovesfrogs?lang=en)[#### cylovesfrogs
](https://www.tiktok.com/@cylovesfrogs?lang=en)
](https://www.tiktok.com/@cylovesfrogs/video/7083620430933970222)
[# haven’t been able to check-in with y’all in a hot minute 🥺hope you’re all well 💕[**#coffeewithcy**](https://www.tiktok.com/tag/coffeewithcy)[**#coffee**](https://www.tiktok.com/tag/coffee)[**#psl**](https://www.tiktok.com/tag/psl)[**#pumpkinspice**](https://www.tiktok.com/tag/pumpkinspice)[**#cylovesfrogs**](https://www.tiktok.com/tag/cylovesfrogs)[**#checkin**](https://www.tiktok.com/tag/checkin)
](https://www.tiktok.com/@cylovesfrogs/video/7083620430933970222)
[
![Reply to @ochaplant some Pourover coffee tips! #coffeetok #pourovercoffee #coffee created by Caitlin.Campbell with Tai Verdes’s A-O-K](https://p16-sign-va.tiktokcdn.com/tos-maliva-p-0068/c5a5a3be787348699024d3185c1bef89_1649190724~tplv-dmt-logom:tos-useast2a-v-0068/23c7d5eb899b415fac10c84c72cf4cfc.image?lk3s=b59d6b55&x-expires=1739638800&x-signature=%2B07%2FXoGKjAqT62ue0YipPI4hclk%3D&shp=b59d6b55&shcp=-)
[![Caitlin.Campbell,cc.campbell](https://p16-common-sign-va.tiktokcdn-us.com/tos-maliva-avt-0068/cfbfcf79005d73603d46e85c044c13b2~tplv-tiktokx-cropcenter:100:100.jpeg?dr=9640&nonce=43382&refresh_token=19061efab4241e7104fd919f0507a78a&x-expires=1739638800&x-signature=edVCmVPIZTv7jG%2BLGDbbm0tddVQ%3D&idc=useast5&ps=13740610&shcp=b59d6b55&shp=a5d48078&t=4d5b0474)](https://www.tiktok.com/@cc.campbell?lang=en)[#### cc.campbell
](https://www.tiktok.com/@cc.campbell?lang=en)
](https://www.tiktok.com/@cc.campbell/video/7083220201453489414)
[# Reply to[**@ochaplant**](https://www.tiktok.com/@ochaplant)some Pourover coffee tips![**#coffeetok**](https://www.tiktok.com/tag/coffeetok)[**#pourovercoffee**](https://www.tiktok.com/tag/pourovercoffee)[**#coffee**](https://www.tiktok.com/tag/coffee)
](https://www.tiktok.com/@cc.campbell/video/7083220201453489414)
[
![Latte art from @flat_white_short_film #fyp #latteart #shortfilm #flatwhite created by Annie Jordan with Saucy Santana’s Material Girl (Bass Boosted)](https://p16-sign-sg.tiktokcdn.com/obj/tos-alisg-p-0037/36b701f8c3144faab58731d02892903f?lk3s=b59d6b55&x-expires=1739638800&x-signature=tVDPeZVY6g%2F6u8Dg4hGxWAnyxOM%3D&shp=b59d6b55&shcp=-)
[![Annie Jordan,annie_jordan](https://p16-common-sign-sg.tiktokcdn-us.com/tos-alisg-avt-0068/c642ea00d247f760790f100339153ac8~tplv-tiktokx-cropcenter:100:100.jpeg?dr=9640&nonce=28217&refresh_token=3971d9fd93b720380b1ee340f0d06de8&x-expires=1739638800&x-signature=2uuGahDfX8ft4AyTz8Wmz3DYToM%3D&idc=useast5&ps=13740610&shcp=b59d6b55&shp=a5d48078&t=4d5b0474)](https://www.tiktok.com/@annie_jordan?lang=en)[#### annie\_jordan
](https://www.tiktok.com/@annie_jordan?lang=en)
](https://www.tiktok.com/@annie_jordan/video/7084896024384392449)
[# Latte art from[**@flat\_white\_short\_film**](https://www.tiktok.com/@flat_white_short_film)[**#fyp**](https://www.tiktok.com/tag/fyp)[**#latteart**](https://www.tiktok.com/tag/latteart)[**#shortfilm**](https://www.tiktok.com/tag/shortfilm)[**#flatwhite**](https://www.tiktok.com/tag/flatwhite)
](https://www.tiktok.com/@annie_jordan/video/7084896024384392449)
[
![☕️💙🏔 #coffee #mountains #alaska #asmr #peaceful #foryou created by Alisha Bair with Austin FFarwell’s New Home (Slowed)](https://p16-pu-sign-useast8.tiktokcdn-us.com/obj/tos-useast5-p-0068-tx/7e00c3290b9d410885901469cd1cd5c5_1649108428?lk3s=b59d6b55&x-expires=1739638800&x-signature=hASaV0GramhAJW5Nn4TGOHQ6Ckk%3D&shp=b59d6b55&shcp=-)
[![Alisha Bair,alirosebair](https://p16-pu-sign-useast8.tiktokcdn-us.com/tos-useast5-avt-0068-tx/f62b29b94522f8659ee424871e26681a~tplv-tiktokx-cropcenter:100:100.jpeg?dr=9640&nonce=1577&refresh_token=fa416bd38487a8ca753bdc283dfdcb9c&x-expires=1739638800&x-signature=YYsqhVujVuLBGDT6okd5i%2BefYXU%3D&idc=useast5&ps=13740610&shcp=b59d6b55&shp=a5d48078&t=4d5b0474)](https://www.tiktok.com/@alirosebair?lang=en)[#### alirosebair
](https://www.tiktok.com/@alirosebair?lang=en)
](https://www.tiktok.com/@alirosebair/video/7082866751234510122)
[# ☕️💙🏔[**#coffee**](https://www.tiktok.com/tag/coffee)[**#mountains**](https://www.tiktok.comm/tag/mountains)[**#alaska**](https://www.tiktok.com/tag/alaska)[**#asmr**](https://www.tiktok.com/tag/asmr)[**#peaceful**](https://www.tiktok.com/tag/peaceful)[**#foryou**](https://www.tiktok.com/tag/foryou)
](https://www.tiktok.com/@alirosebair/video/7082866751234510122)
[
![Afternoon pick me up #coffeetiktok #coffeeasmr #coffeeaesthetic created by Charlotte with Adrián Berenguer’s Meadow](https://p19-pu-sign-useast8.tiktokcdn-us.com/obj/tos-useast5-p-0068-tx/7cc11b66ca7e46ada960f0a2785d7c43?lk3s=b59d6b55&x-expires=1739638800&x-signature=6YCJtGYUO1nu1YCIWLXZ0pKGSYM%3D&shp=b59d6b55&shcp=-)
[![Charlotte,charlottesmythee](https://p19-pu-sign-useast8.tiktokcdn-us.com/tos-useast5-avt-0068-tx/7326548595883606058~tplv-tiktokx-cropcenter:100:100.jpeg?dr=9640&nonce=82195&refresh_token=d848585400ea0fa2a29d6faf0eaa25fa&x-expires=1739638800&x-signature=1uZo4VPNiVGnC70cntdi4jVrP8w%3D&idc=useast5&ps=13740610&shcp=b59d6b55&shp=a5d48078&t=4d5b0474)](https://www.tiktok.com/@charlottesmythee?lang=en)[#### charlottesmythee
](https://www.tiktok.com/@charlottesmythee?lang=en)
](https://www.tiktok.com/@charlottesmythee/video/7080701370407505198)
[# Afternoon pick me up[**#coffeetiktok**](https://www.tiktok.com/tag/coffeetiktok)[**#coffeeasmr**](https://www.tiktok.com/tag/coffeeasmr)[**#coffeeaesthetic**](https://www.tiktok.com/tag/coffeeaesthetic)
](https://www.tiktok.com/@charlottesmythee/video/7080701370407505198)
[
![The Aerocano #coffee #specialtycoffee #coffeetok #coffeetiktok created by Tanner Colson with moshimo sound design’s Chopin Nocturne No. 2 Piano Mono](https://p16-pu-sign-useast8.tiktokcdn-us.com/tos-useast5-p-0068-tx/45d87cd6c0244b55b078072b9b348b18_1649516474~tplv-dmt-logom:tos-useast5-p-0000-tx/1ffb49d0fbbd4fee886a644df6aa0897.image?lk3s=b59d6b55&x-expires=1739638800&x-signature=dDvFiMh%2BI19IiBlzpNYohS8GPBs%3D&shp=b59d6b55&shcp=-)
[![Tanner Colson,tannercolson](https://p16-pu-sign-useast8.tiktokcdn-us.com/tos-useast8-avt-0068-tx2/b143078755beb52d78c0d5ba5330709c~tplv-tiktokx-cropcenter:100:100.jpeg?dr=9640&nonce=39908&refresh_token=67e90794c7d9a0856fe017703d15c8c2&x-expires=1739638800&x-signature=h3wWGEUj%2F7Gvu0hv3yk9JlrQ1mQ%3D&idc=useast5&ps=13740610&shcp=b59d6b55&shp=a5d48078&t=4d5b0474)](https://www.tiktok.com/@tannercolson?lang=en)[#### tannercolson
](https://www.tiktok.com/@tannercolson?lang=en)
](https://www.tiktok.com/@tannercolson/video/7084619271766019370)
[# The Aerocano[**#coffee**](https://www.tiktok.com/tag/coffee)[**#specialtycoffee**](https://www.tiktok.com/tag/specialtycoffee)[**#coffeetok**](https://www.tiktok.com/tag/coffeetok)[**#coffeetiktok**](https://www.tiktok.com/tag/coffeetiktok)
](https://www.tiktok.com/@tannercolson/video/7084619271766019370)
[
![#coffee #fyp #asmr #newcup #trending created by annieegaangg with annieegaangg’s original sound](https://p19-pu-sign-useast8.tiktokcdn-us.com/obj/tos-useast5-p-0068-tx/19f94be4cc404b3bb581c39b1c2bec20?lk3s=b59d6b55&x-expires=1739638800&x-signature=Xy7KDdqLhbm5mD4bCHEgv%2BJDkkM%3D&shp=b59d6b55&shcp=-)
[![annieegaangg,annieegaangg3](https://p16-pu-sign-useast8.tiktokcdn-us.com/tos-useast8-avt-0068-tx2/d90c4bc04b1fa876c4fbac84a1abc312~tplv-tiktokx-cropcenter:100:100.jpeg?dr=9640&nonce=95963&refresh_token=1e48ca6a3b23225e03b2b96a542c4d53&x-expires=1739638800&x-signature=BmVN25Rsz0x9qok2rL3nQEKuQJg%3D&idc=useast5&ps=13740610&shcp=b59d6b55&shp=a5d48078&t=4d5b0474)](https://www.tiktok.com/@annieegaangg3?lang=en)[#### annieegaangg3
](https://www.tiktok.com/@annieegaangg3?lang=en)
](https://www.tiktok.com/@annieegaangg3/video/7085423009925811502)
[# [**#coffee**](https://www.tiktok.com/tag/coffee)[**#fyp**](https://www.tiktok.com/tag/fyp)[**#asmr**](https://www.tiktok.com/tag/asmr)[**#newcup**](https://www.tiktok.com/tag/newcup)[**#trending**](https://www.tiktok.com/tag/trending)
](https://www.tiktok.com/@annieegaangg3/video/7085423009925811502)
[
![POV: you just ordered 4 coffees for your coworkers 👩🏼‍💻👨🏽‍💻👩🏼‍💻#pov #coffeecarsloveni  ia #barista #latteart created by Coffeecar Slovenia with CKay’s love nwantinti (ah ah ah)](https://p16-sign-va.tiktokcdn.com/obj/tos-maliva-p-0068/773c58f45bbf456891904d9d5b6ce913?lk3s=b59d6b55&x-expires=1739638800&x-signature=FUqKDXEllbGeqSjbcSvFwH3dRLE%3D&shp=b59d6b55&shcp=-)
[![Coffeecar Slovenia,coffeecarslovenia](https://p19-common-sign-va.tiktokcdn-us.com/tos-maliva-avt-0
Summary: None
```

  * AI 검색 엔진으로 api 키 필요
  * 공식문서 : [https://exa.ai/docs/sdks/python-sdk](https://exa.ai/docs/reference/search-api-guide-for-coding-agents)

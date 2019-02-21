Btrade API
=====

&nbsp;

### API Info
---

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Btrade는 개발자를 위해 API를 제공하여 다양한 앱과 프로그램을 개발할 수 있는 환경을 제공합니다.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;이제 누구나 쉽게 비트레이드에서 제공되는 API를 통하여

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;사용자 정보, 지갑정보, 주문, 거래 내역, 거래 취소 등의 기능을 사용할 수 있습니다.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;또한 지갑 API를 제공하여 암호화폐 유관 서비스를 구축하는데 도움을 드립니다.


### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[API Key 생성하러 가기](https://www.btrade.co.kr/mypage/mypage.do) (API Key는 __Btrade 마이페이지__에서 생성할 수 있습니다.)


&nbsp;

### API 공지
---

#### Open API  변경사항 안내 (-)


$nbsp;$nbsp;$nbsp;


##### &nbsp;&nbsp;&nbsp; <Open API 변경사항>

&nbsp;&nbsp;&nbsp;해당 변경 사항은 __2018.10.10 11:00__ 부터 적용되오니, 해당 내용과 적용 시점을 반드시 확인하시고

&nbsp;&nbsp;&nbsp;적용해주시기 바랍니다.

&nbsp;

&nbsp;

### Reference
---

#### 1. Public API

#### Ticker - 거래소 마지막 거래 정보

__[GET]__ &nbsp;&nbsp;&nbsp;```https://api.btrade.co.kr/api/ticker/currency/{coin_code}```

__[Curl]__ &nbsp;&nbsp;&nbsp;```curl -X GET --header 'Accept: application/json' 'https://api.btrade.co.kr/api/ticker/currency/{coin_code}'```

__[Response Body]__

```
{
  "status": "0000",
  "data": {
    "open_price": "10000",
    "close_price": "10000",
    "low": "10000",
    "high": "10000",
    "average_price": "0.0",
    "units_traded": "0E-18",
    "volume_1day": "0E-18",
    "volume_7day": "431.699880000000000000",
    "buy_price": "0000000000.00000000",
    "sell_price": "0000000000.00000000",
    "date": 1548933680756
  }
}
```

__[Input Parameter]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|coin_code|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;코인명 (ALL, BTC, ETH, ETC, LTC, ZEC, etc.)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|

__[Output Parameters]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|status: 0000|정상|
|open_price|최근 24시간 내 시작 거래금액|
|close_price|최근 24시간 내 마지막 거래금액|
|low|최근 24시간 내 최저 거래금액|
|High|최근 24시간 내 최고 거래금액|
|average_price|최근 24시간 내 평균 거래금액|
|units_traded|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;최근 24시간 내 Currency 거래량&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|
|volume_1day|최근 1일간 Currency 거래량|
|volume_7day|최근 7일간 Currency 거래량|
|buy_price|거래 대기건 최고 구매가|
|sell_price|거래 대기건 최소 판매가|
|date|현재 시간 Timestamp|


&nbsp;

#### Orderbook - 거래소 판매 / 구매 등록 대기 또는 거래 중 내역 정보

__[GET]__ &nbsp;&nbsp;&nbsp;```https://api.btrade.co.kr/api/orderbook/currency/{coin_code}```

__[Curl]__ &nbsp;&nbsp;&nbsp;```curl -X GET --header 'Accept: application/json' 'https://api.btrade.co.kr/api/orderbook/currency/{coin_code}'```


__[Response Body]__
````
{
  "status": "0000",
  "data": {
    "timestamp": 1548934145839,
    "order_currency": "BTC",
    "payment_currency": "KRW",
    "bids": [
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      }
    ],
    "asks": [
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      }
    ]
  }
}
````


__[Input Parameter]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|coin_code|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;코인명 (BTC, ETH, ETC, LTC, ZEC, etc.)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

__[Output Parameters]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|timestamp|현재시간|
|order_currency|코인|
|payment_currency|지불 통화|
|it_action|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[bids]: buy / [asks]: sell&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|
|it_market_cost|시세|
|nResCoin|사용 가능 코인|

&nbsp;

&nbsp;

#### 2. Token
---

#### Create - 최초 토큰 생성

__[POST]__ &nbsp;&nbsp;&nbsp;```https://api.btrade.co.kr/api/v1/access_token```

```
{
  "nonce":"1548998552194",
  "hstr":"54c25b135d6e80129b71e399fecf522016ab528be7459b1c33c73730de67fad6",
  "apikey":"BTkYXt3hv5BxzieKxHiE9zovAsDSVXraNpJ",
  "grant_type":"APIKEY",
  "expires_in":60
}
```

__[Curl]__

```
curl -X POST --header 'Content-Type: application/json;charset=UTF-8' --header 'Accept: application/json' -d '{ \ 
   "nonce":"1548998552194", \ 
   "hstr":"54c25b135d6e80129b71e399fecf522016ab528be7459b1c33c73730de67fad6", \ 
   "apikey":"BTkYXt3hv5BxzieKxHiE9zovAsDSVXraNpJ", \ 
   "grant_type":"APIKEY", \ 
   "expires_in":60 \ 
 }' 'https://api.btrade.co.kr/api/v1/access_token'
```

__[Response Body]__

```
{
  "status": "0000",
  "message": "success",
  "data": {
    "access_token": "fb2050d52602edd7798efff6fd7ed289a8d743a4bdda510e0aa374c50e3b2023",
    "access_token_expire": "1549002045865",
    "refresh_token": "48f9b90cee15348744b0da1a8e995c5d3833fd985d8f9dd138c04755b18731c7",
    "refresh_token_expire": "1551590445856"
  }
}
```

__[Input Parameter]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|nonce|Request Time (Unix Time)|
|hstr|sha256( apikey + secretkey + nonce )|
|apikey|회원 API key|
|grant_type|APIKEY|
|expires_in|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Access Token 만료시간 (Minute Time, 최소30분 ~ 최대 60분)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|

__[Output Parameter]__

|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Parmeter Name&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|status| 0000: 정상 / others: error|
|message|결과 메시지|
|access_token|Btrade API 사용을 위한 Access Token|
|access_token_expire|Access Token 만료시간 (Unix Time)|
|refresh_token|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Access Token 갱신을 위한 Refresh Token&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|
|refresh_token_expire|Refresh Token 만료시간 (Unix Time)|

&nbsp;

#### Refresh - 토큰 갱신

__[POST]__

```
{
  "refresh_token":"48f9b90cee15348744b0da1a8e995c5d3833fd985d8f9dd138c04755b18731c7", 
  "expires_in":60, 
  "grant_type":"REFRESH"
}
```

__[Curl]__

```
curl -X POST --header 'Content-Type: application/json;charset=UTF-8' --header 'Accept: application/json' -d '{ \ 
   "refresh_token": "48f9b90cee15348744b0da1a8e995c5d3833fd985d8f9dd138c04755b18731c7", \ 
   "expires_in":60, \ 
   "grant_type":"REFRESH" \ 
 }' 'https://api.btrade.co.kr/api/v1/access_token'
```

__[Response Body]__

```
{
  "status": "0000",
  "message": "success",
  "data": {
    "access_token": "fb2050d52602edd7798efff6fd7ed289a8d743a4bdda510e0aa374c50e3b2023",
    "access_token_expire": "1549002045865",
    "refresh_token": "48f9b90cee15348744b0da1a8e995c5d3833fd985d8f9dd138c04755b18731c7",
    "refresh_token_expire": "1551590445856"
  }
}
```

__[Input Parameter]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|refresh_token|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Token Create API에서 생성된 Refresh Token&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|
|expires_in|Access Token 만료시간 (Minute Unit, 최소30분~최대60분)|
|grant_type|REFRESH|

__[Output Parameter]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|status|0000: 정상 / others: error|
|message| 결과 메시지|
|access_token|Btrade API 사용을 위한 Access Token|
|access_token_expire|Access Token 만료시간 (Unix Time)|
|refresh_token|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Access Token 갱신을 위한 Refresh Token&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|
|refresh_token_expire|Refresh Token 만료시간 (Unix Time)|

&nbsp;

&nbsp;

#### 3. Private API
---

#### Account - 회원 정보 조회

__[GET]__ &nbsp;&nbsp;&nbsp;```https://api.btrade.co.kr/api/private/v1/account?currency={currency}```

__[Curl]__

```
curl -X GET --header 'Accept: application/json' --header 'Authorization: Bearer 125543745d3c2712529a579d1383e89469e3cc9601cd08f22e4dd6c482b5d7b9' 'https://api.btrade.co.kr/api/private/v1/account?currency=BTC'
```

__[Response Body]__

```
{
  "status": "0000",
  "data": {
    "account_id": 3,
    "balance": 5532123.7132,
    "trade_fee": 0.005,
    "created": 1521439134000
  }
}
```

__[Input Header]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|Authorization|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Access Token&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|

__[Input Parameter]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|currency|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;코인명 (BTC, ETH, ETC, LTC, ZEC, etc.)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|



__[Output Parameter]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|status|0000: 정상 / others: error|
|account_id|유저 고유 번호|
|balance|남은 코인|
|trade_fee|적용 수수료율|
|created|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;가입시간 (Unix Time)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|

&nbsp;

#### Balance - 회원 지갑 정보

__[GET]__ &nbsp;&nbsp;&nbsp;```https://api.btrade.co.kr/api/private/v1/balance?currency={currency}```

__[Curl]__

```
curl -X GET --header 'Accept: application/json' --header 'Authorization: Bearer 7488eeb56b924e369c2d60f738e795072d3e90740339dc42205f50743619cfb4' 'https://api.btrade.co.kr/api/private/v1/balance?currency=BTC'
```

__[Response Body]__

```
{
  "status": "0000",
  "data": {
    "total_krw": 9999613666.0878,
    "in_use_krw": 7598430736.27575,
    "available_krw": 2401182929.81205,
    "total_btc": 5532121.7132,
    "in_use_btc": 8.8742,
    "available_btc": 5532112.839
  }
}
```

__[Input Header]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|Authorization|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Access Token&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|

__[Input Parameter]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|currency|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;코인명 (ALL, BTC, ETH, ETC, LTC, ZEC, etc.)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|

__[Output Parameter]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|status|0000: 정상 / others: error|
|total_{currency}|코인별 전체 Currency|
|in_use_{currency}|코인별 사용중 Currency|
|available_{currency}|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;코인별 사용가능 Curreny&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|

&nbsp;
&nbsp;

#### Transaction - 회원 거래 내역

__[GET]__ 

```
https://api.btrade.co.kr/api/private/v1/transaction?currency={currency}&deal_status={deal_status}&trd_state={trd_state}
```

__[Curl]__

```
curl -X GET --header 'Accept: application/json' --header 'Authorization: Bearer 7488eeb56b924e369c2d60f738e795072d3e90740339dc42205f50743619cfb4' 'https://api.btrade.co.kr/api/private/v1/transaction?currency=BTC&deal_status=0&trd_state=OK'
```

__[Response Body]__

```
{
  "status": "0000",
  "data": [
    {
      "search": 0,
      "orderId": "1901251726297700000003",
      "price": 3905.5,
      "trd_state": "OK",
      "fee": 0.0015,
      "trd_type": "BUY",
      "units": 0.001,
      "transfer_date": 1548404789817,
      "btc1krw": 3905500
    },
    {
      "search": 0,
      "orderId": "1901151956097700000003",
      "price": 41636.34,
      "trd_state": "OK",
      "fee": 0.005,
      "trd_type": "SELL",
      "units": 0.01019,
      "transfer_date": 1547549769770,
      "btc1krw": 4086000
    },
    {
      "search": 0,
      "orderId": "1901151956026220000003",
      "price": 44828.905,
      "trd_state": "OK",
      "fee": 0.005,
      "trd_type": "SELL",
      "units": 0.01097,
      "transfer_date": 1547549762618,
      "btc1krw": 4086500
    },
    ...
```

__[Input Header]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|Authorization|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Access Token&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|


__[Input Parameter]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|currency|코인명 (BTC, ETH, ETC, LTC, ZEC, etc.)|
|deal_status|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;상태 - 0(전체), 1(매도), 2(매수), 3(취소), 4(정정)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|
|trd_status|주문 상태 - OK, WAIT|

__[Output Parameter]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|status|0000: 정상 / others: error|
|search|0(전체), 1(매도), 2(매수), 3(입금), 4(출금) 중|
|orderId|주문번호|
|price|거래금액|
|trd_state|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;주문 상태 (OK:전체 체결 완료, WAIT:체결 대기)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|
|fee|거래 수수료|
|trd_type|상태 (BUY:매도, SELL:매수, C:취소, M:정정)|
|units|거래 Currency 수량|
|transfer_date|거래일시|
|{currency}1krw|통상적으로 말하는 시세|

&nbsp;
&nbsp;

### Cancel - 회원 판매 / 구매 거래 취소

__[POST]__

```
{
  "currency" : "BTC",
  "org_ord_no" : "190208154943577"
}
```

__[Curl]__

```
curl -X POST --header 'Content-Type: application/json;charset=UTF-8' --header 'Accept: application/json' --header 'Authorization: Bearer 7603c80ddcd596c6fffb642e44470b9cea0d79e2e67a7b9de9ff5b957d46c1c7' -d '{ \ 
   "currency" : "BTC", \ 
   "org_ord_no" : "190208154943577" \ 
 }' 'https://api.btrade.co.kr/api/private/v1/order/cancel'
``` 

__[Response Body]__

```
{
  "status": "0000",
  "data": "Success"
}
```

__[Input Header]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|Authorization|Access Token|
|Content-Type|The Content-Type entity header is used to indicate the media type of the resource.<br/>(application/json;charset=UTF-8)

__[Input Parameter]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|apikey|유저 API 고유 Key|
|currency|코인명 (BTC, ETH, ETC, LTC, ZEC, etc.)|
|org_ord_no|주문번호|
|nonce|현재날짜 (ex : 20190208)|
|hstr|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;sha-256(nonce, currency, secretKey, sheckSum)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|

__[Output Parameter]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|status|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;0000: 정상 / others: error&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|

&nbsp;
&nbsp;

### Place - 회원 판매 / 구매 거래 주문 등록 및 체결

__[POST]__

```
{
  "currency" : "BTC",
  "deal_type" : "B",
  "deal_money" : "10000",
  "amount" : "1",
  "fee_type" : "K"
}
```

__[Curl]__

```
curl -X POST --header 'Content-Type: application/json;charset=UTF-8' --header 'Accept: application/json' --header 'Authorization: Bearer 7603c80ddcd596c6fffb642e44470b9cea0d79e2e67a7b9de9ff5b957d46c1c7' -d '{ \ 
   "currency" : "BTC", \ 
   "deal_type" : "B", \ 
   "deal_money" : "10000", \ 
   "amount" : "1", \ 
   "fee_type" : "K" \ 
 }' 'https://api.btrade.co.kr/api/private/v1/order/place'
```

__[Response Body]__

```
{
  "status": "0000",
  "data": "Success",
  "order_id": "1902081549435770000003"
}
```

__[Input Header]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|Authorization|Access Token|
|Content-Type|The Content-Type entity header is used to indicate the media type of the resource.<br/>(application/json;charset=UTF-8)


__[Input Parameter]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|currency|코인명 (BTC, ETH, ETC, LTC, ZEC, etc.)|
|deal_type|판매/구매 구분 ( B-매수, S-매도)|
|deal_money|주문 금액|
|amount|주문 수량|
|fee_type|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;수수료 타입 ( K-krw수수료, C-코인수수료 )&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; *판매 시에는 krw 수수료만 가능&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|

__[Output Parameter]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|status| 0000: 정상 / others: error|
|order_id|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;주문 번호&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|

&nbsp;
&nbsp;

### Status

---

#### 1. Token Error

|&nbsp;&nbsp;&nbsp;Status Value&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|2001|Member api key is not exist.|
|2002|INCONSISTENCY HSTR|
|2003|Refresh Token is not exist.|
|2004|Access Token is not exist.|
|2005|No Access Token in Header.|
|2006|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;IP information has changed. Again create_access_token api call.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|
|2007|MEMBER_API_KEY is disabled.|
|2008|MEMBER API is not authorized.|
|2009|MEMBER API is not allow ip.|

#### 2. Exception

|&nbsp;&nbsp;&nbsp;Status Value&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|0001|코인종류 입력 에러|
|0002|존재하지 않는 주문번호입니다.|
|0003|주문가격을 확인하시기 바랍니다. / 거래가격은 1,000원 이상만 가능합니다.|
|0006|주문수량을 확인하시기 바랍니다. / 코인 최대금액을 초과하였습니다. / 코인 거래단위를 확인하시기 바랍니다. / 이미 전체취소 등록되어 있습니다.|
|1001|Invalid Parameter|
|1004|The data does not exist.|
|2000|DATA가 존재하지 않습니다.
|3000|Order State Ready|
|9999|Interval Server Error|













# Product Review

## 상품평 json

1. 상품평 등록 (/product_review/save)  
   POST

- req (Mul)

```json
{
   "productReviewSaveReqDto": {
      "userId": "lch3892",
      "productSeq": "49",
      "content": "너무 예쁘고 핏감도 좋아요!! 색깔별로 추가 구매할 의향 있어요!",
      "score": 5
   },
   "productReviewImgSaveReqDto": {
      "originalFileName": "coatPicture.png",
      "saveFilename": "7b8974f6-2d28-4ece-a311-32d9e5274dba.png"
   }
}
```

- res

```json
{
	"code": 1,
	"msg": "상품평 등록 완료",
	"data": null
}
```

- res error

```json
{
	"code": -1,
	"msg": "에러메시지",
	"data": null
}
```

---
2. 상품평 조회 (/product_review/getAll)    
   GET

- req (Mul)

```json
{
   "productSeq": 44
}
```

- res

```json
{
	"code": 1,
	"msg": "상품평 조회 완료",
	"data": {
       "reviews":[
            {
              "userId": "lch3892",
              "content": "너무 예쁘고 핏감도 좋아요!! 색깔별로 추가 구매할 의향 있어요!",
              "score": 5,
              "like": 59,
              "imgUrl": "https://img.oursite.com/review/23/05/15/18822998f3c_tackmy.jpg"
            },
            { 
             "userId": "osunai",
             "content": "최악이에요 한 번 빨았더니 바로 쪼그라드는거 무엇",
             "score": 1,
             "like": 12
            }
       ]
    }
}
```

- res error

```json
{
	"code": -1,
	"msg": "에러메시지",
	"data": null
}
```

---
3. 상품평 수정 (/product_review/update)    
   UPDATE

- req (Mul)

```json
{
   "reviewSeq": 41,
   "content": "다시 보니 그저 그런 것 같아요!",
   "score": 3,
   "productReviewImgSaveReqDto": {
      "originalFileName": "realPicture.png",
      "saveFilename": "7b83452-4ece-a311-3225274dba.png"
   }
}
```

- res

```json
{
	"code": 1,
	"msg": "상품평 수정 완료",
	"data": null
}
```

- res error

```json
{
	"code": -1,
	"msg": "에러메시지",
	"data": null
}
```
---
3. 상품평 삭제 (/product_review/delete)    
   DELETE

- req (Mul)

```json
{
   "reviewSeq": 31
}
```

- res

```json
{
	"code": 1,
	"msg": "상품평 삭제 완료",
	"data": null
}
```

- res error

```json
{
	"code": -1,
	"msg": "에러메시지",
	"data": null
}
```
---
# Product_QnA

## 상품QnA json

1. 상품 QnA 질의 (/product/qna/question)  
   POST

- req

```json
{
	"productCode": 10,
	"userId": "CUSTOMER123@hanmail.com",
	"qnaType": "배송",
	"content": "배송 기간이 얼마나 걸리나요?",
	"secretYN": true
}
```

-res

```json
{
	"code": 1,
	"msg": "상품 Question 등록 완료",
	"data": null
}
```

---

2. 상품 QnA 응답 (/product/qna/answer)  
   POST

- req

```json
{
	"QNA_SEQ": 1,
	"userId": "SELLER123@naver.com",
	"content": "배송 기간은 3~5일 정도 걸립니다."
}
```

-res

```json
{
	"code": 1,
	"msg": "상품 Answer 등록 완료",
	"data": null
}
```

---

3. 상품 QnA (/product/qna/qna?productCode=10)  
   GET

- res

```json
{
	"code": 1,
	"msg": "상품 QnA",
	"data": [
		{
			"customerId": "CUSTOMER123@hanmail.com",
			"sellerID": "SELLER123@naver.com",
			"qnaType": "배송",
			"secretYN": true,
			"question": "배송 기간이 얼마나 걸리나요?",
			"answer": "배송 기간은 3~5일 정도 걸립니다."
		},
		{
			"customerId": "CUSTOMER111@hanmail.com",
			"sellerID": "SELLER123@naver.com",
			"qnaType": "재입고",
			"secretYN": false,
			"question": "재입고 언제 되나요?",
			"answer": ""
		}
	]
}
```

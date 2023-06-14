# Product

## 상품 json

1. 상품 저장 (/product/save_product)  
   POST

- req (Mul)

```json
{
"file" : imagefile,
"productSaveReqDto":
    {
        "mainCategory": "cloths",
        "middleCategory": "outer",
        "productName" : "test3",
        "wholePrice": 1000,
        "retailPrice": 3000,
        "saleYn" : true,
        "productOptionsReqDtoList" : [
					{   "optionName" : "Blue",
					    "optionVale": "XL",
					    "currentQuantity" : 123,
					},
					{   "optionName" : "Blue",
					    "optionVale": "L",
					    "currentQuantity" : 123,
					},
				]
    }
}
```

- res

```json
{
	"code": 1,
	"msg": "상품 등록 완료",
	"data": null
}
```

- res error

```json
{
	"code": -1,
	"msg": "Category 가 존재하지 않습니다.",
	"data": null
}
```

---

2. 상품 category 페이지 (/product/category)  
   POST

- req

```json
{
	"mainCategory": "cloths",
	"middleCategory": "outer",
	"page": 0,
	"size": 8
}
```

- res

```json
{
	"code": 1,
	"msg": "상품 목록 호출 완료",
	"data": {
		"content": [
			{
				"productCode": "1417dbc4-587e-4e85-b88c-7492e6932571",
				"productName": "test3",
				"originalFileName": "springBoot.png",
				"saveFilename": "7b8974f6-2d28-4ece-a311-32d9e5274dba.png"
			},
			{
				"productCode": "82c9f5a1-fe38-45a5-9d75-ddde594c9aad",
				"productName": "test3",
				"originalFileName": "springBoot.png",
				"saveFilename": "af3e1662-21ee-4c6b-8352-bec06bcaab7f.png"
			},
			{
				"productCode": "8e59842a-7fb4-46a0-a274-b98204f03780",
				"productName": "test3",
				"originalFileName": "springBoot.png",
				"saveFilename": "704cffd9-2b00-4acd-9dfd-97c2ad2a73c6.png"
			},
			{
				"productCode": "140d95ad-c009-4e98-bd30-bf3b810ffc08",
				"productName": "test3",
				"originalFileName": "springBoot.png",
				"saveFilename": "3bfb6124-1895-4581-aadd-c8e859144087.png"
			}
		],
		"pageable": {
			"sort": {
				"empty": true,
				"sorted": false,
				"unsorted": true
			},
			"offset": 0,
			"pageNumber": 0,
			"pageSize": 8,
			"paged": true,
			"unpaged": false
		},
		"last": true,
		"totalPages": 1,
		"totalElements": 4,
		"first": true,
		"size": 8,
		"number": 0,
		"sort": {
			"empty": true,
			"sorted": false,
			"unsorted": true
		},
		"numberOfElements": 4,
		"empty": false
	}
}
```

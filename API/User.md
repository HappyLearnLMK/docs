# User

## 사용자 json

1. 사용자 저장 (/user/save)  
   POST

- req (Mul)

```json
    {
        "userId": "lch3892",
        "password": "1q2w3e4r",
        "userName": "이영수",
        "birthDate": "1981-11-07",
        "mobile" : "010-7221-3214",
        "signUpDate": "2023-01-17",
        "gender": "M",
        "type" : "ADMIN"
    }
```

- res

```json
{
	"code": 1,
	"msg": "사용자 등록 완료",
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
2. 사용자 조회 (/user/getAll)    
   GET

- req (Mul)

```json
 
```

- res

```json
{
	"code": 1,
	"msg": "사용자 조회 완료",
	"data": {
       "users": [
          {
             "userId": "lch3892",
             "userName": "이영수",
             "mobile" : "010-7221-3214",
             "gender": "M",
             "type" : "ADMIN",
             "address": {
                "addrName": "우리집",
                "addr1": "경기 성남시 분당구 판교로 35",
                "addr2": "4층 402호",
                "zipCode": 48252
             }
          },{
             "userId": "cun22qo",
             "userName": "최두팔",
             "mobile" : "010-4454-7812",
             "gender": "F",
             "type" : "USER",
             "address": {
                "addrName": "집",
                "addr1": "서울특별시 송파구 석촌호수로 15길 8",
                "addr2": "104동 1025호",
                "zipCode": 14963
             }
          },{
             "userId": "onairmanny",
             "userName": "왕곤고",
             "mobile" : "010-9264-2938",
             "gender": "M",
             "type" : "STAFF",
             "address": {
                "addrName": "회사",
                "addr1": "서울특별시 구로구 가리봉동 54-1",
                "addr2": "2층 왼쪽",
                "zipCode": 27541
             }
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
3. 사용자 수정 (/user/update)    
   PUT

- req (Mul)

```json
    {
        "userCode": "U7",
        "userName": "이영란",
        "password": "qwer!@#$",
        "mobile" : "010-7221-3214",
        "gender": "F",
        "type" : "STAFF"
    }
```

- res

```json
{
	"code": 1,
	"msg": "사용자 수정 완료",
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
4. 사용자 삭제 (/user/delete)    
   DELETE

- req (Mul)

```json
    {
   "userCode": "u7"
}
```

- res

```json
{
	"code": 1,
	"msg": "사용자 삭제 완료",
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

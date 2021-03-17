# 微信用户登录接口

⭐POST

```
{{url}}/wechat/login
```

🚀初次获取请求：

请求body：

```
code:微信获取到的code
```

🔥成功登录Json：

```json
{
    "code": 200,
    "data": {
        "role": [
            "Consumer"
        ],
        "token": "8|0HnjbcYgEB0zIbtYKATJCBze66zrcM78IeMpNuUQ",
        "head": "https://thirdwx.qlogo.cn/mmopen/vi_32/DYAIOgq83eo2Pc3pVuWXuoKykkGuh1ZiaJgS0iaZicIFiaK5kWHljMEDcHj3K42Qdm7Jg3x9fg0JSuzgR13A22GfPA/132",
        "nickname": "world"
    },
    "msg": "success"
}
```

🔥用户不存在(code存在):

```json
{
    "code": 400,
    "msg": {
        "session_key": "FmGFUp08onTAzFG88mHADQ==",
        "openid": "oR5Pk5BL-oyyABpNl13TGtLaIrlA"
    }
}
```

🐙本情况下前端应存储secret

🐙随后调起注册接口



🔥请求的code不存在

```json
{
    "code": 400,
    "msg": {
        "errcode": 40029,
        "errmsg": "invalid code, hints: [ req_id: LJHf7aMre-sA0aRA ]"
    }
}
```

🔥请求的code已过期

```json
{
    "code": 400,
    "msg": {
        "errcode": 40163,
        "errmsg": "code been used, hints: [ req_id: mJHfAa0gE-1p900a ]"
    }
}
```




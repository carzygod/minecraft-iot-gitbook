# 用户注册接口

⭐POST

```
{{url}}/wechat/info
```

🚀流程

🔥用户成功注册并登录：

样例请求body：

```
//密文向量IV
iv:K1Vfv8WcXnduDj+vPgrGcQ==

//加密数据ED
ed:2hynYH/OJ/R57J0+8cSsYymXjO1RHh3dx/3l7cu81JbZl0DaaFdejkTIiBBIxuEydsW5ew265PY4rNlD732cWuOEtjGuc0KSHXsDG3m05xYCWos64IaqLOvsoaOMhE3cJcaFJMc/6hyZZE7l02UO1Lb4Ly9hxapIyfSGd20KmXneECx8SNovtsqNKmoWqKUyXccVN2DeMz/JD0zyilU68r05u3uVw4dd4oElFE1BBHNlK+02NtZrdpGUCcWSUHDmFAiAEVlaNdDhZOZdQRlsna1mOtpeXerxH7s7CXMPP2ioVUy1SmU4xETYZ1o5DMHZL4u8mHuqkGZsROo+62Ksb4FXs5axhi8zD9NQJu95mcSep7ZHp0RgTSuehZMnskNgeFoy+r5svFEeojHEvcnhtMaDe3fI+3sVXo0tJ4B4/9bjHvKRlAqgG0frJ1/B+25q2bDSga3laapQfndfrJMxew==↵

//用户密钥secret
se:ITVJzDzVCbWWAjBW4Ga4bQ==
```

样例返回Json

```json
{
    "code": 200,
    "data": {
        "role": [
            "Consumer"
        ],
        "token": "10|lcfVbeTU2sZKJRfWsrZO7vlokazahMmddLOANKZm",
        "head": "https://thirdwx.qlogo.cn/mmopen/vi_32/DYAIOgq83eo2Pc3pVuWXuoKykkGuh1ZiaJgS0iaZicIFiaK5kWHljMEDcHj3K42Qdm7Jg3x9fg0JSuzgR13A22GfPA/132",
        "nickname": "world"
    },
    "msg": "success"
}
```

返回用户token与用户信息如头像、昵称登



🔥密文解密失败：

* 🐙直接出错满屏红
* 🐙别怪我，他这个包没有办法预先介入错误，而是会直接返回一个568.18kb的报错文件/页面
# 获取用户数据接口

⭐GET

```
{{url}}/consumer/getInfo
```

🚀请求body：

```
无
```

🚀成功获取JSON:

```json
{
    "code": 200,
    "data": {
        "nickName": "一只🍋J",
        "head": "https://thirdwx.qlogo.cn/mmopen/vi_32/Q0j4TwGTfTKoA2dW3XwcjGJq4XKLfHcHibOrQEV6JXZDE5fZ67dpHM08ldFic0YgyicnWj9A78GgpibcqRjJnh0kMw/132",
        "like": 5,
        "order": {
            "unpay": 1,
            "unrecive": 1,
            "refound": 0,
            "msg": 0,
            "confirm": 0
        }
    },
    "msg": "success"
}
```

🚀示例说明：

```json
{
    "code": 200,
    "data": {
        "nickName": "一只🍋J",//用户名
        "head": "https://thirdwx.qlogo.cn/mmopen/vi_32/Q0j4TwGTfTKoA2dW3XwcjGJq4XKLfHcHibOrQEV6JXZDE5fZ67dpHM08ldFic0YgyicnWj9A78GgpibcqRjJnh0kMw/132",//头像
        "like": 5,//收藏数量
        "order": {//订单相关
            "unpay": 1,//未支付订单数量
            "unrecive": 1,//未收货订单数量
            "refound": 0,//退款中订单数量
            "msg": 0,//待留言订单数量
            "confirm": 0//已收货订单数量
        }
    },
    "msg": "success"
}
```




# 用户连接鉴权逻辑

⭐websocket

```
{{url}}/websocket
```

🚀流程

🔥用户验证成功：

样例请求body：

```
//🚀登录token
$2y$10$1im.z/V7cqu0oX4V1wk5v.TsnSvsrIbeIltfrxCXsrmAAZ3Xyi9V6
```

样例返回Json

```json
{
    "type":1,//🚀消息类型。1：服务器消息，2：用户消息
    "data":"success" //认证成功
}
```

🔥用户验证失败：

```json
{
    "type":1,
    "data":"failed"//认证错误
}
```
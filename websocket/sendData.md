# 数据发送规范

⭐websocket

🚀流程

🔥发送数据：

样例请求body：

```json
{
    "target":"wph004", //🚀目标用户 可以为目标用户 也可以为 default。default则为关联消息群发
    "msg":"cnmb"//🚀发送内容 可以为字符串 也可以发json
}
```

样例返回Json

```json
空
```

🔥用户发送失败：

```json
{
无权限
还没写
}
```
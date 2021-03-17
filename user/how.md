# 鉴权登录说明

🚀声明：

🔥统一优先访问微信登录接口：

若存在该用户，则返回token

否之，返回openid与secret

🔥若获取到openid与secret则：

调起wx.getuserinfo获取用户数据

将iv、密文、secret发送至注册接口以进行二次鉴定

存在UnionId:登录用户并新增openid记录；

存在UnionId:创建用户


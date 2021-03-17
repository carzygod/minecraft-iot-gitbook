# 用户接口

🚀声明：

🔥由于伯乐购商城有多个子商城，为了保证不同子商城的用户能够进行账户互通，目前采用的方案为采用unionID作为用户唯一标识方案。

🔥若该方案后续存在问题，则改采用使用手机号作为唯一标识的方案（配合openid数据分散）

🚀逻辑方案：

注册登录：

①获取用户openid，比对数据库

②若openid存在，则根据openid指向的用户name进行登录

③若openid不存在，则返回获取unionID、手机号的请求

④获取用户unionid、手机号，比对数据库

⑤若uninoid、手机号存在，则创建记录，openid指向用户，openid的fid指向uninoID、手机对应的ID

⑥若uninoid、手机号都不存在，则创造两条新记录：uninoID、手机指向，fid为0；openid指向，fid为uninoid对应的ID


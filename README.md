## Gv 比价助手

### 简介

GV 比价助手是一个支持跨平台的基于第三方机器人协议封装而成的框架,支持**主流电商平台商品的比价查券转链等功能**,支持自定义关键词回复,支持所有群聊好友监听。我们拒绝繁琐的配置 提供在线生成配置文件的功能,帮助您更加快速上手改软件,是您使用返利平台进行推广 赚取佣金的不二选择。

![](https://i.loli.net/2021/11/01/1Mntpv3rlGOZNKE.png)

目前支持的平台有

- 京东 京喜 京东极速版
- 淘宝 天猫

京系支持 卡片消息、链接

淘宝系支持 链接、淘口令

### 特性

- [x] liunx 支持 QQ 可拓展 windows 微信 | Windows 支持 QQ WX
- [x] 支持定时发送自定义消息淘系京系 转链 查询优惠券
- [x] 比价支持自定义显示时间 图片 商品名称等
- [x] 支持自动同意好友请求 自动同意邀请入群 被加后回复
- [x] 支持监听 所有群聊 私聊
- [ ] 支持在线生成 校验 修改配置文件
- [ ] 支持定时发送自定义消息
- [ ] 支持自定义关键字回复

### 配置文件

#### 比价助手配置文件

程序启动第一次会创建配置文件
以下为配置文件列子 请修改为自己的配置文件

```yaml
vlwConfig:
  addres: http://127.0.0.1:5000/ #VLW http服务监听地址
  token: FengG1.. #VLW API调用全局Token 必填
  whetherAgreeFriend: false # 是否自动同意好友请求
cQConfig:
  whetherAgreeFriend: true #是否自动同意好友请求
  whetherAgreeGroup: true #是否自动同意加群请求
  whetherInviteGroup: true #是否自动同意邀请入群请求
jDRebate:
  jpkId: 2110213838 #京品库 appid
  jpkKey: RSoetRkPBrWTYLIXFUbeadT6EZ #京品库 appkey
  jpkUnionId: 20144680 #京东联盟id 京粉app查看
tBRebate:
  ztkKey: a4ed78c13bad55ddf0579a #折淘客 appkey
  ztkSid: 653 #折淘客 sid
  ztkPid: mm_297075_24750311_731092 #折淘客 淘宝授权 pid
froogleConfig:
  whetherShopImage: false #比价文案是否发送主图照片
  whetherShopName: true #比价文案是否发送商品名称
  whetherDate: true #比价文案是否发送所有日期
otherConfig:
  replyAfterBeingAdded: 您好,我是Gv比价助手,您可以从京东、拼多多、淘宝 APP中 使用右上角的分享按钮分享给我,我会自动帮您查询历史价格以及是否有隐藏优惠,当您身边的朋友也想使用比价功能时,您可以把我拉进群聊,本助手不会收集使用者任何信息。 #添加好友后回复
```

## 教程

### 折淘客

注册网址:http://www.zhetaoke.com/user/user_register.html

找到个人信息 授权管理 Appkey 查看 对应配置文件 `ztkKey`

找到个人信息 授权管理 添加你的淘宝账户授权 对应配置文件 `ztkSid`

找到推广中心 PID 管理 添加你淘宝授权 pid 对应配置文件 `ztkPid`

### 京品库

申请京品库开发者应用，https://member.jingpinku.com/develop/index.do，审核一天，获取appid和appkey。申请通过后，

京品库 appid 对应配置文件 `jpkId`

京品库 appkey 对应配置文件 `jpkKey`

手机下载京粉 APP 我 正上方 联盟 ID 对应配置文件 `jpkUnionId`

### windows 支持微信 QQ

**教程太过小白和啰嗦 不够简单 其实配置起来很方便**
群里下载独立版的 GvAide 压缩包

1. 到群里下载 Windows 版本的压缩包 解压 找到 GvAide.exe 打开一下关闭 目录下找到`config.yaml` 文件
2. https://github.com/Mrs4s/go-cqhttp/releases 默认下载 386 结尾的 用不了再下载你电脑架构的版本 (**下载错误会导致你 cqhttp 打不开**)
   <img src="https://i.loli.net/2021/11/01/NxwobECI76fGtTO.png" width = "800" height = "400"  />
   cqhttp![]() 下载压缩包或者安装包都可以 群里有个配置文件 名称为`config.yml`
   拉到 cqhttp 的目录下 ![](https://i.loli.net/2021/11/01/mbn64rCdOKIfwzs.png)
   启动主程序 扫码登录 登录过后不要关闭 (**无视 WARING**)
3. windows 支持微信 到群里下载 VLW 框架 打开之后会提示你安装指定版本的微信 安装过后启动 VLW
   **为了防止微信版本更新 请使用压缩包内一个名称为`改host地址指向本地防更新.exe`点开 闪一下就可以了**
   之后点击插件管理 找到插件 xYo_httpApi_WeChat-->启用-->设置 启用自动开启服务 设置 API 调用 token 设置完毕点击启动服务 之后就可以使用 VLW 启动微信了 登录一下
   ![](https://i.loli.net/2021/11/01/8fSg6FMarVT4Xj5.png)
4. 找到你解压过后 GvAide 的目录 找到`config.yaml`文件(**没有就先运行一下**) 填写好配置文件 打开`GvAide.exe` 就可以了

## 打赏 购买

请联系 Q:2628791395

<img src="https://i.loli.net/2021/11/01/vCFNikThqdYlaKz.jpg" width = "300" height = "300"  />

## Gv 比价助手

### 简介

GV 比价助手是一个支持跨平台的基于第三方机器人协议封装而成的框架,支持**主流电商平台商品的比价查券转链等功能**,支持自定义关键词回复,支持所有群聊好友监听。我们拒绝繁琐的配置 提供在线生成配置文件的功能,帮助您更加快速上手改软件,是您使用返利平台进行推广 赚取佣金的不二选择。

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

如果您使用了傻妞 请在傻妞 cqhttp 配置文件 `config.yml` 连接服务列表--> HTTP 通信设置-->反向 HTTP POST 地址列表
添加一行 ` - url: "http://localhost:7270/api/qqCQ" # 地址 如果是本机请填写为localhost 如果是其他服务器地址请修改为IP或者域名`

```yaml
vlwConfig:
  addres: http://127.0.0.1:5000/ #VLW http服务监听地址
  token: FengG1.. #VLW API调用全局Token
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

1. 下载.Net 运行时 https://dotnet.microsoft.com/download/dotnet/5.0 ![](https://i.loli.net/2021/11/01/ZMBpcJjl7nwQxEd.png) 一般 windows 系统都是 x64 或者 x86 如果你是 32 位就选择 x86 64 就选择 x64 arm 就选 Arm64 下载过后安装
2. 到群里下载 Windows 版本的压缩包 解压 找到 GvAide 打开打开之后 目录下找到`config.yaml` 文件
3. 配置 CQhttp 前往https://github.com/Mrs4s/go-cqhttp/releases 下载你电脑版本的 cqhttp![](https://i.loli.net/2021/11/01/NxwobECI76fGtTO.png) 下载压缩包或者安装包都可以 群里有个 cqhtto 的配置文件 名称为`config.yml` 拉到 cqhttp 的目录下 ![](https://i.loli.net/2021/11/01/mbn64rCdOKIfwzs.png) 启动主程序 扫码登录
4. windows 支持微信 到群里下载 VLW 框架 打开之后会提示你安装指定版本的微信 安装过后重新启动 VLW 为了防止微信版本更新 请使用压缩包内一个名称为`改host地址指向本地防更新`点开 闪一下就可以了 之后点击插件管理 找到插件 xYo_httpApi_WeChat-->启用-->设置 ![](https://i.loli.net/2021/11/01/8fSg6FMarVT4Xj5.png) 启用自动开启服务 设置全局调用 token 设置完毕点击启动服务
5. 找到你解压过后比价助手的目录 找到`config.yaml`文件 填写好配置文件 启动 cqhttp（登录过的） vlw 启动微信（xYo_httpApi_WeChat 要开启服务） 就可以使用了

## 打赏 购买
请联系Q:2628791395
![](https://i.loli.net/2021/11/01/vCFNikThqdYlaKz.jpg)

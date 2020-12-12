1：速度不怎样，应个急没问题。脚本默认情况下仅支持IBM伦敦.

   | Secrets变量 | 形式 |
  | --------------------- | ----------- |
  | `IBM_CF_USERNAME`       | IBM Cloud 邮箱地址 |
  | `IBM_CF_PASSWORD` | IBM Cloud 邮箱密码 |
  | `IBM_CF_APP_NAME` | IBM Cloud 应用程序名 |
  | `V2_UUID` | 自定义UUID码 |
  | `V2_WS_PATH_VMESS` </br> `V2_WS_PATH_VLESS` | 协议选择一个，填入自定义PATH路径 |
  
注：VMESS默认的alterId为64

2：每周自动登录IBM服务器一次
利用Github的Actions 每周重启 IBM Cloud Fonudray
IBM Cloud 10天不操作就会关机，所以我们需要 十天内对其重启一次，避免关机。

首先登录IBM Cloud

点击又上角的命令行

在这一步我们主要是记录4个值

IBM_ACCOUNT // IBM Cloud的登录邮箱和密码
IBM_APP_NAME // 应用的名称
REGION_NUM // 区域编码
RESOURSE_ID // 资源组ID
具体后面会一步一步完成

image-20200615175949804

进入命令行先执行

ibmcloud login
输入邮箱和密码。

之后记录下区域(Region)

image-20200615180817619


这里需要记下和区域对应的编号也就是REGION_NUM，比如我这里是eu-gb,那么我的区域编号是7

接下来获取资源组idRESOURSE_ID

ibmcloud resource groups
image-20200615183425453

图中所指向便是RESOURSE_ID

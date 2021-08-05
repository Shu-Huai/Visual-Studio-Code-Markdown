# Office Tool Plus使用教程

## 关于本文档

本文档是Office Tool Plus软件的使用教程。本文档将以Office 365 企业应用版及Project 专业版 2019和Visio 专业版 2019为例，从启动程序、卸载、安装、激活等步骤，介绍Office Tool Plus的使用方法。本文档编写于2021年8月5日，使用的Office Tool Plus软件版本为8.2.4.1，发布日期为2021年7月28日，官方提供的下载链接为[https://otp.landian.vip/redirect/download.html?type=runtime](https://otp.landian.vip/redirect/download.html?type=runtime)。理论上使用版本号不同的软件在操作上并无太大差距。

## 关于启动程序

### 如果电脑中已经装有.NET 5 Desktop Runtime x86

在这种情况下，可以直接运行文件夹根目录下的“Office Tool Plus.exe”以启动程序。需要注意的是，电脑中必须安装有x86版本的框架而非x64版本。

### 如果电脑中未装有.NET 5 Desktop Runtime x86

在这种情况下，运行文件夹根目录下的“RunMe.bat”以启动程序，脚本会自动加载.NET 5 Desktop Runtime x86，随后会自动运行“Office Tool Plus.exe”。如果你想要下载.NET 5 Desktop Runtime x86框架，请访问[https://dotnet.microsoft.com/download/dotnet/current/runtime](https://dotnet.microsoft.com/download/dotnet/current/runtime)。

启动后，会提示需要阅读并接受使用条款。
接下来会出现一个以“微软 CDN 出现比较严重的问题。”为开头的消息提示，点击确定即可。

## 关于卸载

点击主页面中的部署按钮，进入部署界面。

在基础设置下的产品栏目中，可以看到电脑中原有的Office应用程序，点击卸载按钮，卸载全部产品，点击开始部署。

随后程序将唤起微软的产品卸载程序，点击卸载按钮，等待程序执行完毕。

## 关于安装

点击主页面中的部署按钮，进入部署界面。

在基础设置下的产品栏目中，点击添加产品按钮，选择“Microsoft 365 企业应用版”。

再次点击添加产品，选择“Project 专业版 2019”。

再次点击添加产品，选择“Visio 专业版 2019”。

在应用程序栏目中，建议全选，如果了解每个软件的用处可以进行自定义。

在语言栏目中，点击添加语言，会出现简体中文语言包。

在右边的部署设置中，体系结构选择64位。

点击查看XML代码按钮，看到的代码应该一致于或至少相似于下面的代码。

```XML
<Configuration>
  <Add OfficeClientEdition="64" Channel="Current" AllowCdnFallback="True">
    <Product ID="O365ProPlusRetail">
      <Language ID="zh-cn" />
    </Product>
    <Product ID="ProjectPro2019Retail">
      <Language ID="zh-cn" />
    </Product>
    <Product ID="VisioPro2019Retail">
      <Language ID="zh-cn" />
    </Product>
  </Add>
</Configuration>
```

随后点击开始部署按钮，提示确认信息，点击确认，开始进行安装。

安装完成后，界面如图。
![安装完成](Pictures/安装完成.png "安装完成")

## 关于激活

点击主页面中的激活按钮，进入激活界面。

首先需要清除原先的许可证。在许可证管理栏目中的安装许可证按钮旁边的下拉菜单中选择清除所有许可证，弹出警告，点击是。等待程序运行完毕，在操作结果栏目下的文本区域会显示形如：

> Found 97 licenses to install.
> Number of Licenses Uninstalled = 97

这样的文本，表示操作成功。

接下来安装新的许可证。在许可证管理栏目中的选择产品选框中选择“Office Mondo 2016 - 批量版 - [MondoVolume]”，点击安装许可证，弹出注意信息，点击是即可。等待程序运行完毕，在操作结果栏目下的文本区域会显示如下信息：

> <产品密钥安装成功>

表示操作成功。

然后输入KMS信息。在KMS管理栏目中的KMS主机字段填写“kms.loli.beer”，点击保存设置，在操作结果栏目下的文本区域会显示：

> 成功应用设置

表示操作成功。

最后，点击左上角的激活按钮，等待程序执行完毕，在操作结果栏目下的文本区域会显示形如：

> Office 16, Office16MondoVL_KMS_Client edition
> 许可证说明: Office 16, VOLUME_KMSCLIENT channel
> 产品密钥的最后五个字符: XQBR2
> <产品激活成功>

这样的文本信息，表示操作成功。

激活完成后，激活界面的显示如下：
![激活完成](Pictures/激活完成.png "激活完成")

打开Word或其他应用程序，依次点击文件、账户，可以看到产品已激活。
![产品已激活](Pictures/产品已激活.png "产品已激活")

至此，Office 365 企业应用版及Project 专业版 2019和Visio 专业版 2019安装激活完毕。

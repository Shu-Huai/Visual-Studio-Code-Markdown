# Office Tool Plus使用教程

## 关于本文档

本文档是我自己编写的，Office Tool Plus软件的使用教程。本文档将以Office 365 企业应用版为例，从启动程序、安装、卸载、激活等步骤，介绍Office Tool Plus的使用方法。

## 关于启动程序

### 如果电脑中已经装有.NET 5 Desktop Runtime x86

在这种情况下，可以直接运行文件夹根目录下的“Office Tool Plus.exe”已启动程序。需要注意的是，电脑中必须安装有x86版本的框架而非x64版本。

### 如果电脑中未装有.NET 5 Desktop Runtime x86

在这种情况下，运行文件夹根目录下的“RunMe.bat”以启动程序，脚本会自动加载.NET 5 Desktop Runtime x86，随后会自动运行“Office Tool Plus.exe”。如果你想要下载.NET 5 Desktop Runtime x86框架，请访问[https://dotnet.microsoft.com/download/dotnet/current/runtime](https://dotnet.microsoft.com/download/dotnet/current/runtime)。

## 关于激活

点击主页面中的激活按钮

![激活按钮](Pictures\激活按钮.png)

首先需要清除原先的许可证。在许可证管理栏目中的安装许可证按钮旁边的下拉菜单中选择清除所有许可证，等待程序运行完毕，在操作结果文本区域会显示相应的成功信息。

接下来安装新的许可证。在许可证管理栏目中的选择产品选框中选择“Office Mondo 2016 - 批量版 - [MondoVolume]”，点击安装许可证，等待程序运行完毕，在操作结果文本区域会显示相应的成功信息。

然后输入KMS信息。在KMS管理栏目中的KMS主机字段填写“kms.loli.beer”，点击保存设置。

最后，点击左上角的激活按钮。

至此，Office 365 企业应用版激活完毕。

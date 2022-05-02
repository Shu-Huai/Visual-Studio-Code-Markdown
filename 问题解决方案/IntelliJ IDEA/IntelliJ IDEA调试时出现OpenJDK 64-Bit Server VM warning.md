# IntelliJ IDEA调试时出现OpenJDK 64-Bit Server VM warning

## 错误信息

OpenJDK 64-Bit Server VM warning: Sharing is only supported for boot loader classes because bootstrap classpath has been appended

## 错误图示

![错误图示](http://shu-huai.cn:13127/public/图床/IntelliJ%20IDEA调试时出现OpenJDK%2064-Bit%20Server%20VM%20warning错误图示.png "错误图示")

## 错误原因

由于启用了系统代理，同时在IntelliJ IDEA中开启了检测代理，造成异步堆栈跟踪warning。

## 解决方法

文件(F)→设置(T)→构建执行部署→调试器→异步堆栈跟踪→取消勾选检测代理→确定。
![解决方法](http://shu-huai.cn:13127/public/图床/IntelliJ%20IDEA调试时出现OpenJDK%2064-Bit%20Server%20VM%20warning解决方法.png "解决方法")

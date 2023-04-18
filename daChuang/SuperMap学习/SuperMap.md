---
tags : [ 大创 , SuperMap , 汇总 ]
---
## SuperMap iObject Java下载和安装

访问[SuperMap技术资源中心|为您提供全面的在线技术服务](http://support.supermap.com.cn/DownloadCenter/ProductPlatform.aspx)下载，下载完成后解压运行 `install.bat` 即可完成安装

## SuperMap iObject Java许可配置

两种方法，在线许可和离线许可

- 在线许可
  - 在SuperMap Online上申请在线许可[申请试用许可 (supermapol.com)](https://www.supermapol.com/web/pricing/triallicense)，在程序内使用代码登录即可

```java
// 传入SuperMap Online帐号，登录自动检索可用许可
CloudLicense.login(username, password);
// 连接云许可中的许可模块，验证是否云许可获取是否成功，成功返回0
License lic = new License();
int code = lic.connect(65400);    //试用许可模块ID 65400
System.out.println("code = " + code);
```

- 离线许可
  - 离线许可在安装iObject JAVA时会自行安装

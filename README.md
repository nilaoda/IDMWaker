# IDMWaker
调用IDM的[API](http://www.internetdownloadmanager.com/support/idm_api.html)添加任务

## 功能描述
将链接批量发送给IDM进行下载，并提供正则表达式匹配，自动增加序号等功能  
  
![截图](https://i.loli.net/2019/05/13/5cd9165d3800a64404.png)


## 实现方式
1.[下载API](http://www.internetdownloadmanager.com/support/download/IDMCOMAPI.zip)  
2.使用`TlbImp.exe`将`IDManTypeInfo.tlb`文件转换为dll类库  
3.在项目中引入该类库并调用，C#核心代码如下
```
new IDManLib.CIDMLinkTransmitterClass().SendLinkToIDM2(
    URL, //URL
    Referer, //Referer
    Cookies, //Cookies
    Data, //Data
    Username, //Username
    Userpassword, //Userpassword
    LocalPath, //LocalPath
    LocalFileName,  //LocalFileName
    Flag, //Flag
    UserAgent,
    null
    );
```

## 下载
https://github.com/nilaoda/IDMWaker/releases/latest

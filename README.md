#微信Web-App几分钟变身“原生App”

微信最近推出了 微信JS-SDK， 使微信公共号可以直接调用微信原生的接口，具备部分原生应用的能力。微信JS-SDK 的推出，将大大提高微信公共号的用户体验，但是如果存在一种方式，可以使微信公共号各种已有的服务，直接变为一款真正的原生应用，岂不是会更好？借助APICloud 平台，可以做到：零修改，微信公共号 变 iOS  + Android双平台原生应用！

**两种实现方式：**
* 方式一： 网站控制台新建 native 应用； 用我们提供的  jweixin-1.0.0.js 文件替换 微信官方的  jweixin-1.0.0.js 文件，并按特定目录组织；网站勾选必须的 weiXin  sinaWeiBo qq baiduMap imageBrowser speechRecognizer baiduLocation scanner 模块；网站云编译，扫码即可安装。 
* 方式二： 网站新建 webapp ，输入自己的 微信 webapp 地址；把我们的 jweixin-1.0.0.js放到您自己的服务器，并在页面内正确引入；勾选必须的 weiXin  sinaWeiBo qq baiduMap imageBrowser speechRecognizer baiduLocation scanner模块；网站云编译，扫码即可安装。

下面以微信 JS-SDK 的 demo 页面对方式做一具体介绍：

1.http://demo.open.weixin.qq.com/jssdk/ 把此页面保存到本地 wiget 文件夹中。
建议使用 Google 浏览器，这样可以保存页面用到的 js css 文件。如图1.

<img src="http://community.apicloud.com/bbs/data/attachment/forum/201501/13/200332oky0a0ap9x9axr87.png" />

2.修改中文文件（夹）名，因为 android 开发不允许存在中文文件名。这里我们把 “微信JS-SDK Demo_files”文件夹，更名为 “script” 文件夹; 把 “微信JS-SDK Demo.html” 文件，重命名为 index.html。

**注意：**

a. index.html 中的 “微信JS-SDK Demo_files” 相关路径也要同步修改为 “script”。

b. index.html 用作倒档的几个按钮，如“基础接口”，“分享接口”等，点击会跳出应用，需要删去 Google 智（无）能（脑）添加的路径信息：http://demo.open.weixin.qq.com/jssdk/，如
“http://demo.open.weixin.qq.com/jssdk/#menu-basic”改为 “#menu-basic”。

c. 以上需要修改的地方，都是因为使用了 Google 浏览器保存网页，浏览器智（无）能（脑）添加了无关信息；实际开发中，是不会遇到这个问题的。

3.在 wiget 文件目录下添加一个 config.xml 文件，并适当修改，并适当配置。如果2：
关于配置的更多信息，参见：http://docs.apicloud.com/APICloud/技术专题/3rd-party-integration-manual。
当然， 您可以直接复制附件中的 config.xml 文件到您自己的 wiget 文件夹中，来快速体验。

<img src="http://community.apicloud.com/bbs/data/attachment/forum/201501/13/200332gym5vo5q35vi5vbo.png" />

4.使用我们提供的 jweixin-1.0.0.js 文件替换 wiget/script/jweixin-1.0.0.js文件.（jweixin-1.0.0.js 文件见下方链接）
      
5.网站控制台新建 native 应用；widget 文件夹压缩为 widget.zip ，并上传到 网站控制台-->代码；
上传成功，云编译即可生成原生iOS + Android应用。见图3，图4.图5.

<img src="http://community.apicloud.com/bbs/data/attachment/forum/201501/13/200333zsak6c121cg0xagz.png" />

6.扫描生成的二维码，安装应用；安装成功后，打开即可体验。详见效果图。
      
**注意：**

1. 微信 JS-SDK 接口文档，参见： http://mp.weixin.qq.com/wiki/7/aaa137b55fb2e0456bf8dd9148dd613f.html

2. 示例中使用的是 APPloader 的相关 SDK 信息，微信分享后，可能会跳转到 APPLoader 应用。把您的应用配置更改为自己的，即可解决此问题。

<img src="http://community.apicloud.com/bbs/data/attachment/forum/201501/13/200333vqq5rr7vlrpzrr3q.png" />

<img src="http://community.apicloud.com/bbs/data/attachment/forum/201501/13/200333g4u12uwz6ebx16bu.png">

<img src="http://community.apicloud.com/bbs/data/attachment/forum/201501/13/200333mm8pzar1iccacmm1.png">

<img src="http://community.apicloud.com/bbs/data/attachment/forum/201501/13/200334uzzszcztkmvn9xi9.png">

<img src="http://community.apicloud.com/bbs/data/attachment/forum/201501/13/200335l9qqnwunqy3caqu8.png">

<img src="http://community.apicloud.com/bbs/data/attachment/forum/201501/13/200336tnqcuhlndl7ymhn8.png">

<img src="http://community.apicloud.com/bbs/data/attachment/forum/201501/13/200336fxn899w8i9e8z4en.png">

<img src="http://community.apicloud.com/bbs/data/attachment/forum/201501/13/200336ehoxznin9meix66i.png">

<img src="http://community.apicloud.com/bbs/data/attachment/forum/201501/13/200337xo9takebukeomeek.png">

**下载链接:**
      
1. iOS 安装包地址：http://resource.apicloud.com/weixinjssdk/weChat.ipa
      
2. 安卓安装包地址：http://resource.apicloud.com/weixinjssdk/weChat.apk
      
3. jweixin-1.0.0.js APICloud 版 地址；http://resource.apicloud.com/weixinjssdk/jweixin-1.0.0.js
      
4. widet.zip 压缩包，源文件地址：http://resource.apicloud.com/weixinjssdk/widget.zip
      
二维码扫描快速体验：
-----------------------
<img src="http://community.apicloud.com/bbs/data/attachment/forum/201501/13/200333xe5qx6vo3wx6w6vm.png">

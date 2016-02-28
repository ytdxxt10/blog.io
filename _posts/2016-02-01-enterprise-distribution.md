---
layout: post
title: iOS企业应用发布
date: 2016-02-02
tags:[iOS技术]
description: iOS应用发布

comments: true
---

#iOS企业级发布

当然你首先得有一个企业账号😊，像下面这种
![](https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/two.png)

###创建企业发布证书
这里不在详细赘述所有步骤，上一篇[](http://ytdxxt10.github.io/Terry_Blog/%E6%8A%80%E6%9C%AF/2016/02/02/distribution.html)已经做了详细介绍，
这里主要比较他们的区别。
首先创建证书应该点击如下图中的 In-House and Ad Hoc，由于我已经创建过，因此是不可点击的状态。

![](https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/enterprise2.png)

###创建Provisioning Profiles
如上，只讲区别。
创建时，点击下图中的In House选项

![](https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/enterprise3.png)

注意：**不管是证书还是provisioning创建完成后都需要下载下来双击安装一下，包括怎样确定证书是否安装成功，上一篇也已经介绍过**

###创建IPA文件和manifest（plist文件）
首先你得到工程中点击general,填好你的bundleID，然后下面的Team选上你的**企业级开发者账号**(记住是企业级，而不是公司或个人账号)，然后再点击上面的build Setting ,在Code Signing中选为发布模式，如下图:

![](https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/enterprise7.png)

点击general 如果Team底下没有出现警告，就说明到目前为止没有任何问题😂，不然的话，出现的原因可能是
-Team上的账号选择错误。
-bundle ID 填写错误
-证书没有正确安装
-provisioning profiles不在该证书底下。

假如你没有出现警告的话，那么下面我们来打包。
点击上方的Product底下的Archive进行打包,完成后点击右侧的**Export**(注意是Export，而不是upload to APP Store),当然你也传不上去😊。
此时出现下面的情形，选择Save for Enterprise Deployment，然后Next

![](https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/enterprise8.png)

选择你的企业证书，出现：

![]()

选择第一个**Export one app for all compatible devices**
点击Next，开始打包。此时出现：

![](https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/enterprise9.png)

这里如果你只是想要把你的APP放在第三方托管，你就不需要选择*include manifest for over-the-air installation*
第三方平台可以参考[这个](fir.im)

否则你打算在你自己的服务器上进行无线分发，你就需要选上，点击Next：

![](https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/enterprise11.png)
填入你的APP URL 和 Display Image URL和 Full Size Image URL
必须是Https开头奥。
至此前端的工作就做完了。
后面就是你需要后台和web人员协助你，弄成这种形式,进行无线分发

```
<a href="itms-services://?action=download-manifest&url=https://mydomain.com/apps/MyInHouseApp.plist" id="text">Install the In-House App</a>

```

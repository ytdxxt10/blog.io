---
layout: post
title: iOS应用发布
category: 技术
comments: true
---

#iOS应用发布

当然首先你得有一个开发者账号。
像这种

![](https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/three.jpg)


##创建发布证书
+首先先到上面那个界面点击

![distribution2](https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/4.png)

+后点击Certificates

+到达

![distribution3](https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/5.png)

+点击右上角的+按钮

+点击

![distribution4](https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/7.png)

+继续点击continue，这里会要求你上传一个CSR文件。

!(distribution5)(https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/8.png)

+这里打开钥匙串访问，点击左上角的钥匙串访问，证书处理，从证书颁发机构请求证书到达这里，然后填上上面的邮箱，下面选择存储到磁盘。点击继续，保存到一个路径中。

![distribution6](https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/9.png)

然后我们回到刚才的界面，点击下面的chooseFile，上传你的CSR文件。点击下面的Generate按钮，下载下来证书点击Done。双击下载的证书

![distribution7](https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/10.png)

如何判断证书是否有效？
去你的钥匙串中，如果存在你的证书。并且点击下面有个钥匙的东西，说明你的证书是有效，可以使用的，反之不可。当然你也可以把其导成.p12文件，给别人使用。

![distribution8](https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/11.png)

##创建一个Provisioning Profiles
点击provisioning Profiles下面的Distribution，后点击右上角的+号按钮。

点击下面的Distribution下面的AppStore按钮。点击继续，选择一个APPID(如果你未创建APPID，请到APPID界面下创建一个)，然后把这个文件下载下来并双击。

![distribution9](https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/12.png)
![distribution10](https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/13.png)

##上传项目至APPStore
回到你的工程，在General下面的BundleID，填入你自己创建的APPID
然后在BuildSetting下面的Code Signing中选择成如下

![distribution11](https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/14.png)
![distribution12](https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/15.png)

按command+shift+k,清除下缓存。
后选择product下面的Archive

完成后，点击右侧的Upload to App Store选择你们公司或者个人账号。点击choose，如下，、
![distribution12](https://github.com/ytdxxt10/Terry_Blog/raw/gh-pages/blogImages/enterprise1.png)

点击upload即可上传。
时间依网速而定，快则5min，满则失败重传n次。

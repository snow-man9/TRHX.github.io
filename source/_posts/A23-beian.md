---
title: 网站ICP备案和公安备案流程
tags: 
  - ICP备案
  - 公安备案
categories:
  - [WEB前端]
  - [Hexo]
description: 为了规范互联网信息服务活动，促进互联网信息服务健康有序发展，国家相关部门要求在国内的所有网站都必须备案(使用海外服务器则不需要备案)，未备案的域名不能使用国内服务器。部分推广平台也需要备案才可以开通。
thumbnail: https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/thumbnail/NationalEmblem.png
avatar: https://cdn.jsdelivr.net/gh/TRHX/CDN-for-itrhx.com@2.1.9/images/trhx.png
icons: [fas fa-heading]
---

![Website-Approve](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/Website-Approve.png)

网站备案分为ICP备案和公安备案
- ICP备案：ICP备案的目的就是为了防止在网上从事非法的网站经营活动，打击不良互联网信息的传播，如果网站不备案的话，很有可能被查处以后关停。根据中华人民共和国信息产业部第十二次部务会议审议通过的《非经营性互联网信息服务备案管理办法》条例，在中华人民共和国境内提供非经营性互联网信息服务，应当办理备案。未经备案，不得在中华人民共和国境内从事非经营性互联网信息服务。而对于没有备案的网站将予以罚款或关闭。

- 公安备案：网站备案是根据国家法律法规需要网站的所有者向国家有关部门申请的备案，公安局备案是其中一种。公安局备案一般按照各地公安机关指定的地点和方式进行，操作流程会比ICP备案流程简单，主要是已登记为主。

以百度官网为例，其中`京公安网备11000002000001`就是公安备案，`京ICP证030173号 `就是ICP备案
![01](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/01.png)
# <font color=#FF0000> -- ICP备案 </font>
一般在域名服务商那里都会有代备案系统，下面以阿里云为例，进入备案系统：
![02](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/02.jpg)

### <font color=#FF0000>1、填写信息验证备案类型</font>
备案主办单位填写，个人就选个人，企业就选企业，按照实际信息填写：
![03](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/03.jpg)
### <font color=#FF0000>2、产品验证</font>
对搭建备案网站的云服务器进行验证，如果你在阿里云购买了相关产品，就选择相应的产品类型和实例进行验证，也可以勾选`已有备案服务号`，填写服务号进行验证，备案服务号可以通过备案控制台进行申请，具体操作可以参考官方文档[《申请备案服务号》](https://help.aliyun.com/knowledge_detail/36938.html)，也有的小伙伴没有在任何地方购买过服务器等相关产品，比如单纯搭建一个 [Github Pages + Hexo](https://blog.csdn.net/qq_36759224/article/details/82121420) 轻量级的个人博客，这种博客没有后端，不需要服务器，但是要备案怎么办？这种情况也好解决，去某宝买一个服务号就行了。
![04](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/04.jpg)
![05](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/05.jpg)
### <font color=#FF0000>3、填写网站信息</font>
填写网站信息以及办理备案的个人或者单位的真实信息，在填写网站名称的时候要<font color=#FF0000>特别注意！特别注意！特别注意！不满足要求的话是会被打回的！</font>不能使用姓名、地名、成语、不能包含公司、组织等企业性质的词语......具体要求可以参考官方文档[《填写主体信息和网站信息》](https://help.aliyun.com/knowledge_detail/36948.html?spm=a2c4g.11186623.6.573.6e1369a5ZNlC0v)。
![06](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/06.jpg)
![07](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/07.png)
### <font color=#FF0000>4、上传资料</font>
根据要求，上传证件照片或证件彩色扫描件。身份证好说，拍好了上传就行了，注意《网站备案信息真实性核验单》需要你<font color=#FF0000>下载并打印在一张A4纸上，使用黑色签字笔填写，不能涂改</font>，具体可参照所给的示例进行填写，填写完成后再拍照上传。企业网站类似，提交备案后会在一个工作日内进行初审。
![08](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/08.jpg)
![09.jpg](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/09.jpg)
![10](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/10.jpg)
### <font color=#FF0000>5、人脸核验或幕布拍照核验</font>
根据不同地域管局要求及核验平台的支持情况，使用人脸识别进行核验，或者申请专用幕布进行幕布拍照核验

| 地区 | 核验要求 |
|:--:|:--|
| 上海、福建地区用户 | 需使用阿里云APP进行人脸核验。如果使用PC端发起的备案申请，请根据界面提示下载阿里云APP进行人脸核验。 |
| 广东、辽宁、安徽、重庆地区用户 | 首次备案、新增网站：支持使用阿里云APP进行人脸核验或通过阿里云备案平台（PC端）进行幕布拍照核验。<br>其他备案类型：需通过阿里云备案平台（PC端）进行幕布拍照核验。|
| 其他地区用户 | 通过阿里云备案平台（PC端）进行幕布拍照核验。 |


以幕布拍照核验为例，如果你没有阿里云的幕布，就需要申请幕布（免费的），邮寄很快，大约两三天就到了，等收到幕布后，按照要求进行拍照，<font color=#FF0000>一定要仔细阅读拍照说明！一定要仔细阅读拍照说明！一定要仔细阅读拍照说明！不合格依旧会被打回！</font>拍照完成后上传即可。
![11](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/11.jpg)
![12](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/12.jpg)
![13](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/13.png)
### <font color=#FF0000>6、提交管局、短信核验</font>
当照片审核通过后，就会提交到管局，工信部要求部分省市成为手机号码短信核验试点省市，相应省市的用户在阿里云备案平台提交备案申请且初审完成后，会收到工信部发送的核验短信，短信包含验证码和验证地址，需要在收到短信的24小时内完成短信核验，备案申请才能进入管局审核。
需短信核验省份：

 - 2017年12月18日起：天津、甘肃、西藏、宁夏、海南、新疆、青海被列为试点省份。
 - 2018年9月10日起：浙江、四川、福建、陕西、重庆、广西、云南被列为试点省份。
 - 2018年9月24日起：山东、河南、安徽、湖南、山西、黑龙江、内蒙古、湖北被列为试点省份。

![14](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/14.jpg)
### <font color=#FF0000>7、ICP备案完成</font>
整个备案过程中会有阿里云的客服打电话给你，进行信息确认，备案申请信息成功提交管局系统后，管局审核一般为 3 - 20 个工作日（亲测很快，不到一个周就通过了），审核通过后会收到阿里云的邮件通知。
![15](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/15.jpg)
# <font color=#FF0000> -- 公安备案 </font>
公安备案个人觉得比ICP备案还要麻烦，自己在公安备案的时候，最开始申请了一个月也没给我处理（大概是地方原因，所在的市比较小，估计都没几个人办过网站，网警也不太负责），与ICP备案最大的不同，如果你是交互式网站的话，公安备案是需要你去公安机关当面审核的，这也是比较麻烦的一点。
### <font color=#FF0000>1、用户注册、登录</font>
登录[全国互联网安全管理服务平台](http://www.beian.gov.cn)，选择联网备案登录，注册账号并登录
![16](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/16.jpg)
### <font color=#FF0000>2、新办网站备案申请</font>
点击新办网站申请，按实填写网站开办主体，上传身份证正反照和手持身份证件照。
![17](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/17.jpg)
![18](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/18.jpg)
### <font color=#FF0000>3、填写网站基本信息</font>
按实填写网站基本信息，需要注意的地方：

<font color=#FF0000>IP：</font>IP地址为阿里云/腾讯云的公网IP地址，请不要填写内网IP。

<font color=#FF0000>域名证书：</font>以阿里云为例，进入【域名控制台】，点击域名后面的【管理】，选择【域名证书下载】即可，其它服务商类似。

<font color=#FF0000>网络接入/域名注册服务商：</font>若办理公安备案的域名是通过[阿里云](https://www.aliyun.com/)完成的工信部备案，则按照以下填写：
网络接入服务商：
- 接入商所属地区管辖：境内
- 接入商所属区域 ：浙江省 杭州市 滨江区
- 名称：阿里云计算有限公司
- 网站接入方式：租赁虚拟空间

域名注册服务商：
- 域名商所属地区管辖：境内
- 域名服务商所属区域：浙江省 杭州市 余杭区 
- 名称：阿里云计算有限公司（原万网）

也可以通过点击后面的`查询网络接入\域名注册服务商`直接选择相应服务商，其他服务商类似

<font color=#FF0000>服务类型：</font>交互式服务指：为互联网用户提供信息发布、交流互动等服务，包括但不限于论坛、博客、微博、网络购物、网上支付等服务类型，此项选择是否提供互联网交互服务将会直接影响到后面是否需要去公安局当面核验，若选择`是`，当地网警会打电话叫你去公安局当面核验，还需要填写《交互式服务安全检查表》等各种文件，总之是比较麻烦的，个人小网站，博客什么的建议选择`否`，选择`www服务`，这样的话不用去当面核验，审核下来也比较快，企业单位用户建议选择交互式。

其他信息如实填写即可！
![19](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/19.png)
### <font color=#FF0000>4、填写网站负责人信息</font>
填写网站安全负责人和网站应急联络人相关信息，网站应急联络人直接勾选同主体负责人后会自动填入。
![20](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/20.jpg)
### <font color=#FF0000>5、同意责任书并提交审核</font>
《互联网信息服务单位网络安全责任告知书》有30秒的强制阅读时间，建议认真阅读一下告知书的内容。然后勾选我已阅读，点击提交即可。随后可以看到审核状态，不同地区政策有所不同，会有当地的网警联系网站负责人的，审核通过后记得在网站首页底部张贴公安机关核发的备案图标！
![21](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/21.png)
![22](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A23/22.png)
# easy_chatgpt

**写在最前：**

计划采用国内能调用的接口来重写一个最简单能部署的代码
接口采用：https://github.com/xing61/xiaoyi-robot

# 优质稳定的OpenAI的API接口-For开发者

#### 介绍
为开发者提供优质稳定的OpenAI相关的API调用接口。  
小一机器人，提供ChatGPT的API调用，支持openai的API接口，支持：gpt-4，gpt-3.5。      
要买openai的账号？  
要科学上网？  
要美元的银行卡？  
通通不用的，直接调用就行，简单粗暴，关键稳定，超级好用！！  
openai的国内代理，国内接口请求转发，api proxy  
各种示例代码：https://github.com/xing61/xiaoyi-robot/blob/main/example.md

- **项目主要优势**  
  * 不限制国内使用，可以用微信充值，没有封号风险。
  * 不用买openai的账号，不用美元的银行卡。 
  * 无需代理即可访问，没有墙的阻拦。  
  * 支持GPT4，并且没有每3小时25条消息的限制。  
  * 兼容OpenAI接口格式，可以做到平替。支持vscode插件，支持autoGPT，agentGPT。API用法也可参考官方文档  
  * 新增对Embeddings支持，可以用接口运行AutoGPT等应用。
  * 新增对stream模式的支持，可以支持原生的各种应用
  * 更多特性支持，敬请期待。也可直接向我们提交需求哦

- **项目地址**   
1、微信公众号：小一机器人，开发者单独的Secret Key、余额查询、示例代码等请从微信公众号“小一机器人”，点击菜单“Chat的API”查看。     
账号信息管理：http://flag.smarttrot.com/#/my,  （暂时充值只能微信充值，所以充值要从微信公众号”小一机器人“中进行）      
 ![小一机器人-公众号二维码-small](https://github.com/xing61/xiaoyi-robot/assets/38256442/c3a00169-d51b-48f7-b969-2303e9916886)  
2、微信交流群（如果你也对本项目感兴趣，欢迎加入群聊参与讨论交流）：    
![微信截图_20230723120823](https://github.com/xing61/xiaoyi-robot/assets/38256442/2d2ad0af-a3ba-4d7f-9ddb-ef0204efc0ac)  
3、QQ群（彩蛋：群里有qq机器人：小一机器人，@他即可像访问chatgpt一样。另外现在加入邀请内测还能赠送免费token）  
![qq群-微信截图_20230723120926](https://github.com/xing61/xiaoyi-robot/assets/38256442/7805499d-e0e5-41fb-b5a3-a90237b76730)  

**首次使用配置：**

请访问 http://你的域名/key.php 配置您的API_KEY列表，程序将全局自动循环调用。默认用户名：admin，默认密码：admin@2023。默认用户名密码可以在key.php文件中修改。

**本项目完全开源，是PHP版调用OpenAI的API接口进行问答的Demo，有以下特性和功能：**

1. 对PHP版本无要求，不需要数据库。核心代码只有几个文件，没用任何框架，修改调试很方便。
2. 采用stream流模式通信，一边生成一边输出，响应速度全网最快。
3. 支持GPT-3.5-Turbo和GPT-4等各种模型（后者需要修改下默认model名称）。
4. 支持Markdown格式文本显示，如表格、代码块。对代码进行了着色，提供了代码复制按钮，支持公式显示。
5. 支持多行输入，文本框高度自动调节，手机和PC端显示都已做适配。
6. 支持一些预设话术，支持上下文连续对话，AI回答途中可以随时打断。
7. 支持错误处理，OpenAI接口返回错误时可以看到具体原因。
8. 可以实现区分内外网IP，内网直接访问，外网通过BASIC认证后可访问。
9. 可以实现页面输入自定义API_KEY使用，方便分享给网友或朋友使用。
10. 服务器自动记录所有访问者的对话日志和IP地址，方便管理员查询。
11. 支持API_KEY自动轮询，解决5美元账户每分钟限制查询3次的问题。
12. 支持调用OpenAI官方接口画图，提问的第一个字是“画”即可生成图片。

**本项目定位是个人或朋友之间分享使用，轻量设计，不计划引入数据库等复杂功能。有需要的用户可以自行拿去修改，版权没有，改动不究。对于项目UI或其他功能有改进想法的朋友欢迎提交PR，或者在Issues或Discussions进行讨论。**

------
# 测试网址：http://mm1.ltd
![t1](https://user-images.githubusercontent.com/5563148/232330560-1b6a45f3-fcc1-4d3e-a2f7-b1c9878fe9cd.jpg)
![t2](https://user-images.githubusercontent.com/5563148/232330566-c6ea7fb3-474f-45e4-adda-37f3db27b92a.jpg)
![t3](https://github.com/dirk1983/chatgpt/assets/5563148/732b5bed-7e9c-4c07-9865-9b97957781a7)


------
**本项目常见问题：**

1. 在国内环境使用提示OpenAI连接超时

是的，OpenAI官方不支持中国（含港澳台地区）IP访问接口。有以下几种解决方案：

a. 使用境外服务器部署本项目，如美国、韩国、日本等，比如腾讯云日本就可以。

b. 如果本项目部署在电脑上，可以用电脑上的HTTP-PROXY代理，把stream.php里面注释掉的“curl_setopt($ch, CURLOPT_PROXY, " http://127.0.0.1:1081 ");”修改一下即可。

c. 使用反向代理服务，将OpenAI接口地址反代到某个网址，把“curl_setopt($ch, CURLOPT_URL, ' https://api.openai.com/v1/chat/completions ');”这行里面的网址改成反代后的网址即可。

使用后两种解决方案的时候可能会因为代理的缓存机制造成stream模式的实时性受影响，另外可能也增加了额外的访问延迟。

2. 关于反向代理的配置方式

如果你有海外服务器，使用nginx反代最简单，修改配置文件，增加一两行代码即可实现，具体方式自行搜索。如果没有海外服务器，可以用cf worker免费建一个，前提是你要有一个域名，几块钱就能注册一个。搭建自己的cf worker教程在这里：https://github.com/noobnooc/noobnooc/discussions/9 。如果你连域名也不想注册，也可以用别人现成的反代地址，比如下面这个：https://openai.1rmb.tk/v1/chat/completions 。地址是群友提供的，不确定什么时候失效，用的人比较多时可能会有点卡，大家也可以进群求一个。

3. 关于Stream流模式的原理，为什么你部署的不像我的那么快

本项目前端使用的是Javascript的EventSource方式与后端进行通信，可以实现数据的流模式即时传输，而OpenAI接口也是支持数据实时生成实时传输的，因此才能实现问答的秒回。EventSource模式的缺点是不支持POST方式传递数据，GET方式对数据长度有限制，cookie也有限制，所以选择了分两步请求后端，采用SESSION传递数据。至于为什么你用我的代码部署的网站速度比较慢，主要原因除了服务器的问题，可能还有PHP环境的问题。PHP如果想实现流式输出需要关闭输出缓存，可能需要修改apache或nginx及php.ini的配置，具体修改方式可以自行搜索或者到群里问群友。

4. 如果想实现像Demo站一样输入API_KEY才能使用的功能，怎么修改代码

在index.php文件中取消掉相关的注释就行了，为了美观建议把上面的“连续对话”部分注释掉，要不然手机访问不是很友好。注释“连续对话”不影响网站运行，默认就是包含上下文的连续对话。

5. 是否支持docker？

有网友提出想使用docker方式运行本项目，其实随便找一个nginx+php环境的docker，把path指向本项目所在的目录就行了。这里提供热心网友提供的docker镜像：gindex/nginx-php。使用方式如下：

```
docker pull gindex/nginx-php
docker run -itd -v /root/chatgpt(本地目录):/usr/share/nginx/html --name nginx-php -p 8080(主机端口):80 --restart=always gindex/nginx-php
```

还有另一位热心网友基于本项目在github上的docker版chatgpt，网址：https://github.com/hsmbs/chatgpt-php ，也可以用。

6. 是否支持Windows客户端？

喜欢使用独立Windows桌面应用的朋友可以下载Release里面的exe文件运行，其实就是一个指向我演示网站的浏览器套个壳。

------

附OpenAI官网的模型和接口调用介绍：

https://platform.openai.com/docs/models/moderation

https://platform.openai.com/docs/api-reference/chat/create

https://platform.openai.com/docs/guides/chat/introduction

https://platform.openai.com/docs/api-reference/models/list

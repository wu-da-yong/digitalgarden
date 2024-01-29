---
{"dg-publish":true,"permalink":"/Zettelkasten/14a9a1 potplayer百度翻译插件的使用方法/","dgPassFrontmatter":true}
---

编号:: 14a9a1
标题:: potplayer百度翻译插件的使用方法
创建时间:: 2023-03-11 14:26
up:: [[Zettelkasten/14a9a 硬字幕提取工具9.0教学\|14a9a 硬字幕提取工具9.0教学]]
来源:: 

---
必备工具：
![[SubtitleTranslate - baidu.as]]

## 第一步：必须开通百度翻译的开发者，并注册一个应用
> 1、前往网址：[http://api.fanyi.baidu.com/api/trans/product/prodinfo](http://api.fanyi.baidu.com/api/trans/product/prodinfo)
> 2、登录你自己的百度账号
> 3、第1的网址打开后点“产品服务”，拉到下面，有个“立即使用”
> 4、填写百度翻译要求的必要信息，并完成应用注册，不要填写IP地址，其他的填写啥看你个人喜好咯！

## 第二步：安装翻译插件
> 1、将SubtitleTranslate - [baidu.as](http://baidu.as)、SubtitleTranslate - baidu.ico这两个文件选中，Ctrl+C复制
> 2、打开PotPlayer播放器的安装路径（方法不会的请百度、谷歌等等方式搜索）
> 3、再进入Extention文件夹，接着又进入Subtitle文件夹、最后进入Translate文件夹
> 4、Ctrl+V，把刚才选择的两个文件粘贴到这个文件夹

## 第三步：获取和配置翻译插件的 appId 与 密钥
> 1、第一步中的1，网址，点击“管理控制台”
> 2、我的服务下面一点，如果有“此服务已停用 开启（这两个字蓝色）”的提示，点击“开启”
> 3、拉到底部，会有“申请信息”，里面包含 “APP ID” 和 “密钥”
> 4、随便打开一个带外挂字幕的视频，例如外挂ass字幕文件的视频！
> 字幕->在线字幕翻译->实时字幕翻译设置->选中百度翻译-> 点右边的 “账户设置”，会弹出一个对话框。
> 6、将上面第 3 步得到的“APP ID” 和 “密钥”分别填写进去，然后点确定，会再次弹出对话框，点击关闭就行了。

## 第四步：测试
> 1、随便打开一个带中文字幕的视频（如果上方打开的视频没关闭，不必重新打开）
> 字幕->在线字幕翻译->Bai Du translate
> 字幕->在线字幕翻译->总是使用(注：这个看个人需求)
> 字幕->在线字幕翻译->下面显示翻译(注：这个看个人需求)
> 字幕->在线字幕翻译->目标语言->之后在语言列表选择你要的，例如英语，日语、汉语等等任意一个，看个人需求。
> 6、畅玩吧

## 可选的配置 - 翻译请求的频率
> 1、这个配置是可选的，一般不用配置的
> 2、原因：百度翻译有默认翻译冷却时间，短时间内多次传输翻译请求，那么很可能会被拦截，如果翻译结果会提示 error:54003……那么就是被拦截了。如果出现这个，那么才有必要做这个配置，否则就不需要这个配置的！
> 3、用记事本等文本编辑器打开刚才安装后的SubtitleTranslate - baidu.as这个文件（不是当前这个文本的同一个文件夹里的文件哦，是配置到PolPlayer里面的那个文件！）
> 4、修改大概23行位置的 int coolTime = 1000; 数字1000，将它加大一些，然后保存好文件再试试，如果不够就再加大一些，1000是指1秒钟，1000毫秒=1秒，是指一条字幕翻译后，下一条字幕最少需要等多久才开始翻译的意思。请注意不要删除掉这行的最后一个英文的分号
> 5、保存文件
> 6、如果开着PotPlayer则关闭再重新打开，没开的直接打开就行了，然后就可以试试效果了。

## 常见错误
如果集成后，翻译结果出现：error: 数字，error_msg:英语，那么根据数字，在下方截图查找原因

## 最后：参与扩展
> github发布地址：[https://github.com/fjqingyou/PotPlayer_Subtitle_Translate_Baidu](https://github.com/fjqingyou/PotPlayer_Subtitle_Translate_Baidu)
![](https://secure2.wostatic.cn/static/ezGgZGoB5JGKoWCMW8FPRa/ioWcSxHy1qQyYcBVbzTMSc.png?auth_key=1647372837-3oYyvFn6yeBCqsg3tayJso-0-f4a108a219b52c5b77a7a878d1e31c7c)
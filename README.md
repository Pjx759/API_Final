# 项目名称：药记住


|  发布日期 | 2020-06-18 |
 | -- | -- |
 |  app名称 | 药记住 |
 |  文件现状 | 进行中 |
 |  文件的主人 | 彭靖茜|
 |  领头的设计师 | 彭靖茜 |
 |  领头的开发者 | 彭靖茜 |
 |  领头的测试者 | 彭靖茜 |
 
 > [20×20演示PPT](https://github.com/Pjx759/API_Final/blob/master/%E8%8D%AF%E8%AE%B0%E4%BD%8F20%C3%9720%E6%BC%94%E7%A4%BA.pptx)
## PRD设计
### 一、价值宣言：
> 药记住产品是基于目前医疗环境下，亚健康人群不断壮大的情况下，设计更加贴近用户日常保证身体健康提醒、记录的产品；药记住产品对于用户的帮助是根据用户提供给我们的数据，我们使用通用票据识别、语音识别和关键词提取识别对数据进行处理，帮助用户在繁重、忙碌的日常生活中也可以保证及时记录药物使用方式、剂量和保证按时服用药物，帮助用户记录并完成每一次药物的服用
面对对象为当下的药物使用需求用户
1. 本产品在帮助用户更方便的了解自己的药品数据情况，使用通用票据识别可以帮助用户获得准确的药品剂量、频次信息，而不被混淆
2. 通过用户即时的语音输入，使用语音识别api和关键词提取api，帮助用户获得当下药品使用等其他需求信息，产生即时提醒帮助用户完善用药
### 二、产品概述
* 整体描述：目前市场中能够关于医疗的产品数不胜数，但是大部分都是以医疗治疗为主，能够为用户提供专属服务，药品使用记录的软件在市场中比较少，对于用户日常的使用的医疗软件缺少人性化功能；基于现状，需要一个药品使用记录产品兼顾用户**开药单识别**和**语音识别功能**，并加**关键词提取功能**，帮助用户快速的获取药品使用信息，提高用户日常使用效率
* 产品分析：

|产品概述|需求概述|
 | -- | -- |
 |产品背景|目前医疗行业发展迅速，而目前亚健康群体数量任然庞大，且近年来流感等疾病都存在传播高速的问题，用药人群数量逐步上升，说明本产品市场发展有潜在能力|
 |产品市场|产品针对用药人群进行以用户为中心的设计，可以发掘更多的潜在长期用户市场中相关针对用户的产品存在较少，基本都以用户医疗为主，缺少用户自身服务的产品|
 |市场描述|市场中相关针对用户的产品存在较少，基本都以用户医疗为主，缺少用户自身服务的产品|

### 三、PRD-1加值宣言
- **通用票据识别API的价值**：可以将票据图片上的信息识别并输出为文字信息  
- **语音识别API的价值**：将语音信息转化为文字方便记录，节省文字输入时间  
* **关键词提取API的价值**：提取出用户输入的关键信息
### 四、PRD-2核心价值
- 产品核心价值（最小可行性产品）：提供票据识别帮助用户对于药单数据过多的困恼，也可以快捷的记录用药剂量和频次
### 五、PRD-3核心价值与用户痛点</h3>
* 解决用户对于服用药物的不熟悉可以通过APP进行识别提取重点信息，如服用剂量和频次等信息
* 语音输入可以帮助用户更加快捷的补充信息，并形成一个提醒系统  
* 关键词提取可以帮助用户在大量药物信息中提取出关键的、有利于用户痛点的数据
### 六、PRD-4人工智能概率性与用户痛点
* 目前百度开放平台的票据文字识别正确率需针对各类票据特定的字体、打印样式而准，目前综合场景下字段准确率高达98%，其中增值税发票、出租车票四要素准确率高达99.9%  
* **错误现象的解决方法：**
  * 当图像/语音识别出现偏差时，向用户提供简单编辑修改的功能。可以通过手动修改信息不准确或者错误的地方  
  * 剂量输入时，会设置再次确认，防止错误影响用户  
> 相关链接：[概率性机器学习与人工智能](https://blog.csdn.net/yeler082/article/details/78265086)
### 七、PRD-5需求列表与人工智能API加值  
| 优先级	| 用户需求	| 功能实现 | API价值 | 原因 |
| :--: | :--: | :--: | :--: | :--: |
| 重要	|药品使用方式很多、药品类型量过大时可能会记不清楚每个药品的具体使用的剂量和频次|[通用票据识别](https://ai.baidu.com/tech/ocr_receipts/receipt) 	| 将票据图片转化为文字信息，可以快捷输出数据 | 开药单的数据繁多而用户需要的数据只是其中的一小部分 |
| 次重要	|药品单词使用后可能会混淆不同药品间隔时间，给予用户即时语音输入|[短语音识别](https://ai.baidu.com/tech/speech/asr)| 实现用户输入语音可以输出文字信息，并且提取信息给用户 | 用户在任何时间都可以输入提醒数据 |  
| 一般重要	|提取用户输入的数据，显示用户需要的重点|[关键词提取](https://www.xfyun.cn/services/keyword-extraction)| 通过用户输入语音输出文字的信息，提取关键信息给用户 | 用户输入的信息并不是全部都很重要 |
### 八、产品文档
* **产品介绍**：针对现在药物使用人群，群体是十分庞大的，对于记录药物使用的产品并不是特别多，因此，‘药记住’APP就是对于用户使用药物的数据整合并给予用户一个更加便捷的输出，辅助用户完成日常的药物使用。产品主要使用**通用票据识别**识别用户所得到的开药单，输出药品剂量使用的详细数据，语音识别和关键词提取是辅助用户在使用时，更加便捷的操作
### 九、问题描述与需求列表
#### 9.1用户画像
* 长期服用条理身体药物人群
* 短期内需要持续服用药物人群

| 信息 | 画像1 |
| -- | -- |
| 姓名 | 云芳 |
| 年龄 | 23 |
| 职业 | 白领 |
| 人物简介 | 长期坐在办公室，身体容易出现一些长期潜在不适 |
| 用户痛点 | 票据信息多，无法明白开药单中重要的说明 |
| 使用场景 | 就诊结束后药品很分散，不容易整齐收录和记录使用方法、剂量 |

|信息|画像2|
| -- | -- |
| 姓名 | 一一|
|年龄|21|
|职业|学生|
|人物简介|容易丢三落四，不注意细节问题|
|用户痛点|记不清楚不同药物如何使用|
| 使用场景 | 药品在一定数量时并不容易记得使用方法和剂量 |


### 十、解决方案及表述
> 对于要记住不同药物使用时间和剂量的问题，许多用户对于这种繁琐的事件记忆起来相当困难，甚至会记混淆不同药物的使用方式及剂量
* 用户可欲性
目前市场中能够关于医疗的产品数不胜数，但是大部分都是以医疗治疗为主，能够为用户提供专属服务，药品使用记录的软件在市场中比较少，对于用户日常的使用的医疗软件缺少人性化功能
* 技术可行性
  * 有一定地技术难度的开发
  * 界面设计尽量简单清晰，方便用户有更好地操作体验，减少不必要的按钮和不必要的设计
  * api的调用与整合需要有一定的技术能力，可行度高，api开放平台大多有调用文档帮助使用
  * 作为一款适用于用药记录app，需要设身处地地为用户着想，以用户需求为主，从用户的角度去设计交互
* 商业可行性
通过完善app的内容交互，形成初期的完整的软件，借助用户不断发展，帮助产品推广，对用户提出的痛点进行修改反馈，后期得到数量庞大的用户群后与医疗等相关行业进行合作，从中提高商业价值。
### 十一、利益关系者图
![利益关系者图](https://github.com/Pjx759/API_Final/blob/master/photos/%E5%88%A9%E7%9B%8A%E5%85%B3%E7%B3%BB%E5%9B%BE.jpg)
## 原型设计
### 一、产品流程图
* 智能加值部分流程图
![产品流程图](https://github.com/Pjx759/API_2020/blob/master/Finall/photos/%E4%BA%A7%E5%93%81%E6%B5%81%E7%A8%8B%E5%9B%BE.jpg)  
### 二、框架流程图
![框架图](https://github.com/Pjx759/API_2020/blob/master/Finall/photos/%E4%BA%A7%E5%93%81%E6%A1%86%E6%9E%B6%E6%B5%81%E7%A8%8B%E5%9B%BE%20(1).jpg)
### 三、数据流程图
![原型数据流程图](https://github.com/Pjx759/API_2020/blob/master/Finall/photos/%E6%95%B0%E6%8D%AE%E6%B5%81%E7%A8%8B%E5%9B%BE.png)
### 四、交互界面设计
* [原型交互展示](https://modao.cc/app/c0f063708635bcbed0bde59d2c79ef82f11b0232?simulator_type=device&sticky)
### 五、界面流程图
* 主页功能选择
![主页流程说明](https://github.com/Pjx759/API_Final/blob/master/photos/%E4%B8%BB%E9%A1%B5%E5%88%86%E6%9E%901.png)
* 票据识别交互界面流程
![票据识别界面流程图说明](https://github.com/Pjx759/API_Final/blob/master/photos/%E9%80%9A%E7%94%A8%E7%A5%A8%E6%8D%AE%E8%AF%86%E5%88%AB%E6%B5%81%E7%A8%8B%E5%9B%BE.png)
* 语音输入识别交互界面流程
![语音识别界面流程图说明](https://github.com/Pjx759/API_Final/blob/master/photos/%E8%AF%AD%E9%9F%B3%E8%AF%86%E5%88%AB%E6%B5%81%E7%A8%8B.png)
* 关键词提取交互界面流程
![关键词识别界面流程图说明](https://github.com/Pjx759/API_Final/blob/master/photos/%E5%85%B3%E9%94%AE%E8%AF%8D%E8%AF%86%E5%88%AB1.png)
## API输出、入展示
### 一、API数据输入输出
1. 通用票据识别
  * 识别用户输入的开药单中的是药品信息：[票据识别api说明](https://github.com/Pjx759/API_Final/blob/master/codes/%E9%80%9A%E7%94%A8%E7%A5%A8%E6%8D%AE%E8%AF%86%E5%88%ABapi.md)
> [票据示例](https://github.com/Pjx759/API_Final/blob/master/photos/piaoju1.jpg)
2. 语音识别
  * 识别用户即时输入的语音信息：[语音识别api说明](https://github.com/Pjx759/API_Final/blob/master/codes/%E8%AF%AD%E9%9F%B3%E8%AF%86%E5%88%ABapi.md)
3. 关键词提取
  * 提取出用户输入信息中的重要部分：[关键词提取api说明](https://github.com/Pjx759/API_Final/blob/master/codes/%E5%85%B3%E9%94%AE%E8%AF%8D%E6%8F%90%E5%8F%96api.md)

### 二、API使用水平
* 通用票据识别
  * 输入：票据图片； 输出：票据中的文字信息
* 语音识别
  * 输入：语音信息； 输出：文字信息
* 关键词提取识别
  * 输入：文字信息； 输出：关键词文字信息
> 所选的几个api调用都是技术性很强的平台，并且提供调用文档帮助调用api，文档中输入输出都有清楚的指出数据类型，避免了调用出错
### 三、API风险说明
* 百度语音识别：不同文件输出结果存在一定差异，经过对比，m4a文件的准确度更高
  * 输入其他格式文件
  ![其他格式图片](https://github.com/Pjx759/API_2020/blob/master/Finall/photos/%E5%85%B6%E4%BB%96%E6%96%87%E4%BB%B6.png)
  * 输出错误结果
  ![错误结果展示](https://github.com/Pjx759/API_2020/blob/master/Finall/photos/%E8%BE%93%E5%87%BA%E9%94%99%E8%AF%AF%E6%95%B0%E6%8D%AE.png)
* 关键词提取：过于简单的句子可能无法提取更关键的信息点
  * 关键词过于简单举例![关键词错误举例图片](https://github.com/Pjx759/API_Final/blob/master/photos/%E5%85%B3%E9%94%AE%E8%AF%8D%E8%BF%87%E4%BA%8E%E7%AE%80%E5%8D%95.png)
  * 输出结果会提示错误，经过官网的错误码查询发现是句子过于简单api可能无法提取![关键词输出错误码](https://github.com/Pjx759/API_Final/blob/master/photos/%E5%85%B3%E9%94%AE%E8%AF%8D%E9%94%99%E8%AF%AF%E7%A0%81.png)
### 四、API调用价格说明
1. 语音识别api

| 品牌 |调用说明|
| -- | -- |
| 百度语音识别标准版 |200万次免费调用|
| 百度语音识别急速版 |5万次免费调用|
| 讯飞语音识别 | 最高50万次 |
| 腾讯语音识别 | 录音文件识别免费额度为每月10小时；一句话识别免费额度为每月5000次；实时语音识别免费额度为每月5小时。 |

> 相关链接：[百度语音识别标准版](https://ai.baidu.com/tech/speech/asr)；[百度语音识别急速版](https://ai.baidu.com/tech/speech/asrpro)；[讯飞语音听写](https://www.xfyun.cn/services/voicedictation)；[腾讯语音识别](https://cloud.tencent.com/product/asr)
2. 票据识别api

| 品牌 |调用说明|
| -- | -- |
|百度通用票据识别|免费版：200次/天；定制化：30w+|
|腾讯云票据单据识别|免费调用1000次/月|

> 相关链接：[百度通用票据识别](https://ai.baidu.com/tech/ocr_receipts/receipt)；[腾讯云票据单据识别](https://cloud.tencent.com/product/invoiceocr)

* 总结：选择百度语音api和百度通用票据识别api具有较高的商业可行性，提供的服务在一定程度上可以满足产品的需求
## 心得与感谢
### 心得体会
* 对于一个产品的价值方向，可以明确到每个运用关键点，本次课程中最注重的就是智能加值部分，是产品核心价值；而一个产品如何做好以用户为中心就需要从用户角度出发，当然不能因为使用加值而使用加值给用户，这并不是以用户为中心的设计
* 药记住这个产品的设置跟药品有关，就应该更贴近用户的实际生活，并给予正确的引导
### 感谢
  * 感谢在整个项目中帮助过我的全体老师和同学
  * 感谢整个项目给我在学习上有很多不同的提示与启发
  * 感谢更大品牌人工智能服务文档的对我项目的帮助，让我学会了很多技术上的知识


> PRD文档中图片若不能正常显示，麻烦多刷新几次
> 或[gitee仓库PRD文档](https://gitee.com/pjx759/API_Fianl/blob/master/README.md)

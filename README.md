# 项目名称：药记住


|  发布日期 | 2020-06-18 |
 | -- | -- |
 |  app名称 | 药记住 |
 |  文件现状 | 进行中 |
 |  文件的主人 | 彭靖茜|
 |  领头的设计师 | 彭靖茜 |
 |  领头的开发者 | 彭靖茜 |
 |  领头的测试者 | 彭靖茜 |
## PRD设计
### 价值宣言：
面对对象为当下的药物使用需求用户
1. 本产品在帮助用户更方便的了解自己的药品数据情况，使用通用票据识别可以帮助用户获得准确的药品剂量、频次信息，而不被混淆
2. 通过用户即时的语音输入，使用语音识别api和关键词提取api，帮助用户获得当下药品使用等其他需求信息，产生即时提醒帮助用户完善用药
### PRD-1、加值宣言
- **通用票据识别API的价值**：可以将票据图片上的信息识别并输出为文字信息  
- **语音识别API的价值**：将语音信息转化为文字方便记录，节省文字输入时间  
* **关键词提取API的价值**：提取出用户输入的关键信息
### PRD-2、核心价值
- 产品核心价值（最小可行性产品）：提供票据识别帮助用户对于药单数据过多的困恼，也可以快捷的记录用药剂量和频次
### PRD-3、核心价值与用户痛点</h3>
* 解决用户对于服用药物的不熟悉可以通过APP进行识别提取重点信息，如服用剂量和频次等信息
* 语音输入可以帮助用户更加快捷的补充信息，并形成一个提醒系统  
* 关键词提取可以帮助用户在大量药物信息中提取出关键的、有利于用户痛点的数据
### PRD-4、人工智能概率性与用户痛点
* 目前百度开放平台的票据文字识别正确率需针对各类票据特定的字体、打印样式而准，目前综合场景下字段准确率高达98%，其中增值税发票、出租车票四要素准确率高达99.9%  
* **错误现象的解决方法：**
  * 当图像/语音识别出现偏差时，向用户提供简单编辑修改的功能。可以通过手动修改信息不准确或者错误的地方  
  * 剂量输入时，会设置再次确认，防止错误影响用户  
### PRD-5、需求列表与人工智能API加值  
| 优先级	| 用户需求	| 功能实现 | API价值 | 原因 |
| :--: | :--: | :--: | :--: | :--: |
| 重要	|药品使用方式很多、药品类型量过大时可能会记不清楚每个药品的具体使用的剂量和频次|[通用票据识别](https://ai.baidu.com/tech/ocr_receipts/receipt) 	| 将票据图片转化为文字信息，可以快捷输出数据 | 开药单的数据繁多而用户需要的数据只是其中的一小部分 |
| 次重要	|药品单词使用后可能会混淆不同药品间隔时间，给予用户即时语音输入|[短语音识别](https://ai.baidu.com/tech/speech/asr)| 实现用户输入语音可以输出文字信息，并且提取信息给用户 | 用户在任何时间都可以输入提醒数据 |  
| 一般重要	|提取用户输入的数据，显示用户需要的重点|[关键词提取](https://www.xfyun.cn/services/keyword-extraction)| 通过用户输入语音输出文字的信息，提取关键信息给用户 | 用户输入的信息并不是全部都很重要 |
### 产品文档
* **产品介绍**：针对现在药物使用人群，群体是十分庞大的，对于记录药物使用的产品并不是特别多，因此，‘药记住’APP就是对于用户使用药物的数据整合并给予用户一个更加便捷的输出，辅助用户完成日常的药物使用。产品主要使用**通用票据识别**识别用户所得到的开药单，输出药品剂量使用的详细数据，语音识别和关键词提取是辅助用户在使用时，更加便捷的操作
### 问题描述与需求列表
#### 用户画像
* 长期服用条理身体药物人群
* 短期内需要持续服用药物人群

| 信息 | 画像1 |
| -- | -- |
| 姓名 | 云芳 |
| 年龄 | 23 |
| 职业 | 白领 |
| 人物简介 | 长期坐在办公室，身体容易出现一些长期潜在不适 |
| 用户痛点 | 票据信息多，无法明白开药单中重要的说明 |

|信息|画像2|
| -- | -- |
| 姓名 | 一一|
|年龄|21|
|职业|学生|
|人物简介||
|用户痛点||

## 原型设计
### 原型-1、产品流程图
* 智能加值部分流程图
![产品流程图](https://github.com/Pjx759/API_2020/blob/master/Finall/photos/%E4%BA%A7%E5%93%81%E6%B5%81%E7%A8%8B%E5%9B%BE.jpg)
### 原型-2、数据流程图
![原型数据流程图](https://github.com/Pjx759/API_2020/blob/master/Finall/photos/%E6%95%B0%E6%8D%AE%E6%B5%81%E7%A8%8B%E5%9B%BE.png)
### 原型-3、交互界面设计
* [原型交互展示](https://modao.cc/app/c0f063708635bcbed0bde59d2c79ef82f11b0232?simulator_type=device&sticky)


## API输出、入展示
### 一、API数据输入输出
1. 通用票据识别
  * 识别用户输入的开药单中的是药品信息：[票据识别api说明](https://github.com/Pjx759/API_Final/blob/master/codes/%E9%80%9A%E7%94%A8%E7%A5%A8%E6%8D%AE%E8%AF%86%E5%88%ABapi.md)
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



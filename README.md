# nlp-demo
自然语言处理在线示例
A interface demo for show some nlp tasks
<h3>
这里部署了几个自然语言处理例子，可以通过简单的页面操作来进行实验。（由于使用cpu推断，调用可能会花费一些时间）
请访问：http://zfcjelr4.dongtaiyuming.net:80
</h3>

<br/>

<h2>
问答系统工具
</h2>

<br/>

<h3>
这个问答系统工具包含一些生成问答系统数据及进行各类问答问题样本强化的实用小工具。
包括 抽取式问答、实体问句生成器、问答数据生成器、问答搜索引擎 四部分。
</h3>

<br/>

<h3>
1 抽取式问答，是一个自训练squad形式的问答抽取模型，输入一个问题及对应的上下文，可以得到答案。
</h3>

![FireShot Capture 003 - Gradio - localhost](https://user-images.githubusercontent.com/27874014/176256050-13aa6538-f8c7-44f7-89a5-80c7457e4b83.png)

<br/>

<h3>
2 实体问句生成器，是一个自训练的根据上下文中锁定一个实体，来生成该实体相关的问句。（请保证实体位于上下文中）
输入上下文和其中的一个实体子字符串，可以得到一个实体相关的问句。
</h3>

![FireShot Capture 004 - Gradio - localhost](https://user-images.githubusercontent.com/27874014/176256080-06685064-a251-4ddd-a831-3e8e513f3c16.png)

<br/>

<h3>
3 问答数据生成器，是一个自训练的问答对生成器，输入上下文，这个生成器会生成若干与上下文相关的问答对。
 其中question为生成的问题、entity为对应上下文中的答案、statement为问题对应的陈述句、top_chip为上下文中与陈述句最相似的子句。
</h3>

![FireShot Capture 005 - Gradio - localhost](https://user-images.githubusercontent.com/27874014/176256127-494a5abd-d1e3-4e37-8da3-32c9baeae8c3.png)

<br/>

<h3>
4 问答搜索引擎，是一个自构建的问答对搜索引擎，通过输入问答对，可以搜索语料库中与输入问答对相似的问答对。
 其中question为生成的问题、entity为对应上下文中的答案、statement为问题对应的陈述句、top_chip为上下文中与陈述句最相似的子句、
  score为该搜索问答对与输入问答对的得分。
</h3>

![FireShot Capture 006 - Gradio - localhost](https://user-images.githubusercontent.com/27874014/176256160-37038219-08dc-4512-93e6-5b38dc57d329.png)

<br/>

<h2>
维基百科信息工具
</h2>

<br/>

<h3>
这个自构建的问答系统工具包含一些知识图谱问答系统常用数据接口及最终架构的一个维基百科知识图谱问答接口。
包括 实体查询、实体信息查询、属性查询、实体链接、维基百科知识图谱问答。
</h3>

<br/>
<h3>
1 实体查询、实体信息查询、属性查询这三部分围绕的是定位与搜索感兴趣的实体信息，给出其在知识库中的
 一些表征和一些简单的三元组关联关系，是知识库的基本数据描述。
 这里支持通过中文字符串定位实体在知识库中的ID的搜索映射，并锁定单个实体的属性信息。
  其中通过实体id及属性id进行实体搜索可以精确锁定具有相似属性的实体，以实体字符串
  查询实体是这个功能的一个字符串包装。
  这些搜索功能有助于锁定具有感兴趣的相似属性的实体，可用于实体替换、实体样本增强、知识搜索等功能。
</h3>
<h3>
2 实体链接可以识别上下文中被知识库包含的实体及其基本信息（如实体ID、实体属性、实体类型），可以用于
  根据知识库进行预料标注、模型数据准备等基本功能，是一个有效的辅助工具。
</h3>
<h3>
3 维基百科知识图谱问答系统，包括自训练构建的实体识别、问句分类、知识库引擎搜索、结果排序等各个部分。
可以通过输入一个被知识库涵盖的问题来得到结果。（排序靠上的结果为答案）
</h3>

![FireShot Capture 007 - Gradio - localhost](https://user-images.githubusercontent.com/27874014/176256323-a71b13c7-ad1e-4e68-96ab-1147176a2c64.png)

<br/>

<h2>
数据表问答（TableQA）
</h2>

<br/>

<h3>
自训练构建的 TableQA 数据表问答，可在线编辑数据或上传csv数据，之后通过输入问题得到答案。
一些数据和问句 可以参考：
https://github.com/svjack/tableQA-Chinese/blob/main/notebook/fine-tune-on-finance.ipynb
</h3>

![FireShot Capture 008 - Gradio - localhost](https://user-images.githubusercontent.com/27874014/176256415-1e67957b-2293-47f1-bf64-ca0ced8a6f34.png)

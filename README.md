# nlp-demo
自然语言处理在线示例
A interface demo for show some nlp tasks
<h3>
这里部署了几个自然语言处理例子，可以通过简单的页面操作来进行实验。（由于使用cpu推断，调用可能会花费一些时间）
请访问：http://zfcjelr4.dongtaiyuming.net:80
</h3>
There are some models deplay in a server, that can be test by call some http requests:
(Because use cpu to infer, you many wait some seconds, when call them.)

You can visit http://zfcjelr4.dongtaiyuming.net:80 to try them

<br/>


<h2>
Squad中文抽取式问答：Squad style chinese question answer interface:
</h2>


<img width="543" alt="截屏2022-06-26 13 58 14" src="https://user-images.githubusercontent.com/27874014/175802745-500137eb-6535-4982-af43-3d900b966261.png">


<h3>
这是一个自训练squad形式的问答抽取模型，输入一个问题及对应的上下文，可以得到答案。
</h3>
This is a self trained squad style extractive question answer model

You can try to input a question and realtive context to see the answer.

<br/>


<h2>
实体问句生成器：Generate a question on entity that located in context:
</h2>


<img width="559" alt="截屏2022-06-26 13 59 52" src="https://user-images.githubusercontent.com/27874014/175802752-cf07c30f-9bf9-43bc-bf06-0de30afa601e.png">

<h3>
这是一个自训练的根据上下文中锁定一个实体，来生成该实体相关的问句。（请保证实体位于上下文中）
输入上下文和其中的一个实体子字符串，可以得到一个实体相关的问句。
 </h3>
This is a self trained generator that generate a entity related queston on context.
(Guarantee the entity is located in context)

You can try to input a context and one entity in context to see the question.

<br/>

<h2>
问答数据生成器：Generate question and answer on context:
</h2>

<img width="537" alt="截屏2022-06-26 14 01 14" src="https://user-images.githubusercontent.com/27874014/175802761-ecbc315f-4af7-4948-a4ac-c1d9f3e28825.png">


<h3>
这是一个自训练的问答对生成器，输入上下文，这个生成器会生成若干与上下文相关的问答对。
</h3>
  <br/>
This is a self trained generator that generate question and its answer on context.

You can try to input a context to see relative questions and answers.

<br/>

<h2>
英文对维基百科SparqlQuery生成器：English question to Wikidata style Sparql Query interface:
</h2>

<img width="537" alt="截屏2022-06-26 14 02 10" src="https://user-images.githubusercontent.com/27874014/175802773-12329757-c312-4ff3-a240-a5c66736b54a.png">


<h3>
这是一个自训练的通过英文问句生成对应的 Sparql Query 的生成器，有助于构建问答系统及知识图谱。
可以通过输入英文问句来生成对应的 Sparql Query
</h3>
  <br/>
This is a self trained encoder-decoder on english quetion to wikidata sparql query dataset (with some data augumentation)

This may be useful in some Knowledge Base construction problem or Question Answer task on Knowledge Base.

You can try to input a english question and get the sparql query of this question. 

<br/>

<h2>
维基百科知识图谱问答：Knowledge Graph Question Answer on Wikidata:
</h2>


<img width="537" alt="截屏2022-06-26 14 03 54" src="https://user-images.githubusercontent.com/27874014/175802783-fd1b2760-c253-4f32-b4d6-6264b0689739.png">

<h3>
这是一个自构建的维基百科知识图谱问答系统，包括实体识别、问句分类、知识库引擎搜索、结果排序等各个部分。
可以通过输入一个被知识库涵盖的问题来得到结果。（排序靠上的结果为答案）
</h3
  <br/>
This is a self construct Knowledge Graph Question Answer project demo, with some self trained slot-filling and ranking

model for answer question over wikidata.

You can try to input a question and get the answer in wikidata. (May require some time to infer by cpu)

The output is a ordering list, that answers are located in top.

<br/>


<h2>
数据表问答：Answer question by tableau data:
</h2>
<h3>
自构建的 TableQA 数据表问答，可在线编辑数据或上传csv数据，之后通过输入问题得到答案。
一些数据和问句 可以参考：
https://github.com/svjack/tableQA-Chinese/blob/main/notebook/fine-tune-on-finance.ipynb
</h3>
  <br/>
This is the demo of project:
https://github.com/svjack/tableQA-Chinese 
Which is a chinese tableqa project

You can edit tableau data sheet and the question you want to ask online, and get the answer by click "Get Answer" button

<img width="535" alt="截屏2022-06-26 14 05 00" src="https://user-images.githubusercontent.com/27874014/175802786-c0363747-0d19-4ea0-8f77-05fde4ce70ce.png">


And if you want to try your data and relative question, you can switch the top tab to [数据表问答（上传数据）：Answer question by upload tableau data:]

<img width="535" alt="截屏2022-06-26 14 05 26" src="https://user-images.githubusercontent.com/27874014/175802796-a8f76ebc-d815-4782-b140-249f62d68bbf.png">

Upload a csv file and ask the question.(The default data used in that is same with previous tab)

Some data and question can be seen in: https://github.com/svjack/tableQA-Chinese/blob/main/notebook/fine-tune-on-finance.ipynb

<br/>

<h2>
文本搜索与向量搜索：Text Search on Text or Embedding:
</h2>
<h3>
自搭建搜索引擎，基于Lucene及Milvus，二者分别负责基于中文文本特征的搜索与跨语言向量特征的搜索。
（可通过选定搜索方式为Text和Embedding进行切换）
其中向量搜索支持跨语言搜索，可以通过输入英文或其他大多数语言（包括中文）来进行向量搜索。
支持上传少量csv数据，但生成向量索引需要花费一些时间。
</h3>
  <br/>


<img width="535" alt="截屏2022-06-26 14 08 14" src="https://user-images.githubusercontent.com/27874014/175802801-94d28760-1687-4635-93bb-7162c6215f0b.png">

<img width="535" alt="截屏2022-06-26 14 11 34" src="https://user-images.githubusercontent.com/27874014/175802808-d60ecc39-2fad-460d-8b90-c80ccdff2917.png">

This is a self deploy search engine interface, that support search query by bm25 similarity
or by cos similarity (embed by a cross-language embedding model)

You can try to input a chinese query when search by text or input query in any language (chinese or english for example)
and see the output.

<!-- Because use cpu to infer, may consume some time to build index when search by cos.-->
And you can also upload some text by csv (which has only one column named by "context" and row count limit by 300)
and try to search (consume some time to build text index or embedding index)
<br/>

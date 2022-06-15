# nlp-demo
A interface demo for show some nlp tasks

There are four models deplay in a server, that can be test by call some http requests:
(Because use cpu to infer, you many wait some seconds, when call them.)

You can visit http://zfcjelr4.dongtaiyuming.net:80 to try them

<br/>


<h2>
Squad中文抽取式问答：Squad style chinese question answer interface:
</h2>

<img width="1292" alt="4" src="https://user-images.githubusercontent.com/27874014/172537608-7e4a8f0b-2a88-4878-a5fe-a021a2db95a4.png">


This is a self trained squad style extractive question answer model

You can try to input a question and realtive context to see the answer.

<br/>


<h2>
实体问句生成器：Generate a question on entity that located in context:
</h2>

<img width="1292" alt="5" src="https://user-images.githubusercontent.com/27874014/172537627-9f5d4c75-94bf-480f-afbf-b692a0a4dcac.png">


This is a self trained generator that generate a entity related queston on context.
(Guarantee the entity is located in context)

You can try to input a context and one entity in context to see the question.

<br/>

<h2>
问答数据生成器：Generate question and answer on context:
</h2>

<img width="1292" alt="6" src="https://user-images.githubusercontent.com/27874014/172558081-3d166855-056b-4754-b1ff-da59cdf02a91.png">

This is a self trained generator that generate question and its answer on context.

You can try to input a context to see relative questions and answers.

<br/>

<h2>
英文对维基百科SparqlQuery生成器：English question to Wikidata style Sparql Query interface:
</h2>

![3](https://user-images.githubusercontent.com/27874014/172563175-977df544-fdac-4a9a-a218-d352ccb95092.png)

This is a self trained encoder-decoder on english quetion to wikidata sparql query dataset (with some data augumentation)

This may be useful in some Knowledge Base construction problem or Question Answer task on Knowledge Base.

You can try to input a english question and get the sparql query of this question. 

<br/>

<h2>
维基百科知识图谱问答：Knowledge Graph Question Answer on Wikidata:
</h2>

![Screenshot 2022-06-13 042434](https://user-images.githubusercontent.com/27874014/173252258-6bd181d1-7da8-409d-9447-26c6ae1441c2.png)

This is a self construct Knowledge Graph Question Answer project demo, with some self trained slot-filling and ranking

model for answer question over wikidata.

You can try to input a question and get the answer in wikidata. (May require some time to infer by cpu)

The output is a ordering list, that answers are located in top.

<br/>


<h2>
数据表问答：Answer question by tableau data:
</h2>

This is the demo of project:
https://github.com/svjack/tableQA-Chinese 
Which is a chinese tableqa project

You can edit tableau data sheet and the question you want to ask online, and get the answer by click "Get Answer" button

<img width="1292" alt="截屏2022-06-08 下午9 55 26" src="https://user-images.githubusercontent.com/27874014/172634785-f3b91019-218a-4896-89f1-a5e4c1a42317.png">

And if you want to try your data and relative question, you can switch the top tab to [数据表问答（上传数据）：Answer question by upload tableau data:]

<img width="1291" alt="截屏2022-06-08 下午9 56 42" src="https://user-images.githubusercontent.com/27874014/172634994-2c05af9d-ca32-405f-9ca4-a3960039c0de.png">

Upload a csv file and ask the question.(The default data used in that is same with previous tab)

Some data and question can be seen in: https://github.com/svjack/tableQA-Chinese/blob/main/notebook/fine-tune-on-finance.ipynb

<br/>

<h2>
文本搜索与向量搜索：Text Search on Text or Embedding:
</h2>

<img width="1003" alt="截屏2022-06-09 下午8 05 03" src="https://user-images.githubusercontent.com/27874014/172842848-c4536fa6-3701-4429-a870-dbc910908f56.png">

<img width="1028" alt="截屏2022-06-09 下午7 47 05" src="https://user-images.githubusercontent.com/27874014/172840857-25d045a1-e830-4e23-b628-0eb9de88d079.png">


This is a self deploy search engine interface, that support search query by bm25 similarity
or by cos similarity (embed by a cross-language embedding model)

You can try to input a chinese query when search by text or input query in any language (chinese or english for example)
and see the output.

<!-- Because use cpu to infer, may consume some time to build index when search by cos.-->
And you can also upload some text by csv (which has only one column named by "context" and row count limit by 300)
and try to search (consume some time to build text index or embedding index)
<br/>

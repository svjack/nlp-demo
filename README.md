# nlp-demo
A interface demo for show some nlp tasks

There are four models deplay in a server, that can be test by call some http requests:
(Because use cpu to infer, you many wait some seconds, when call them.)

You can visit http://zfcjelr4.dongtaiyuming.net:80 to try them

<br/>

<h2>
Answer question by tableau data:
</h2>

This is the demo of project:
https://github.com/svjack/tableQA-Chinese 
Which is a chinese tableqa project

You can edit tableau data sheet and the question you want to ask online, and get the answer by click "Get Answer" button

<img width="1292" alt="1" src="https://user-images.githubusercontent.com/27874014/172537468-019ea82b-aefc-47f3-975f-6112f6269d0c.png">


And if you want to try your data and relative question, you can switch the top tab to [2 Answer question by upload tableau data]

<img width="1292" alt="2" src="https://user-images.githubusercontent.com/27874014/172537546-4c912626-0101-47ad-ad6c-d39241d2f259.png">


Upload a csv file and ask the question.(The default data used in that is same with previous tab)

<br/>

<h2>
English question to Wikidata style Sparql Query interface:
</h2>

<img width="1292" alt="3" src="https://user-images.githubusercontent.com/27874014/172537586-cab98f29-0c99-43c3-8121-6d039919de35.png">


This is a self trained encoder-decoder on english quetion to wikidata sparql query dataset (with some data augumentation)

This may be useful in some Knowledge Base construction problem or Question Answer task on Knowledge Base.

You can try to input a english question and get the sparql query of this question. 

<br/>

<h2>
Squad style chinese question answer interface:  
</h2>

<img width="1292" alt="4" src="https://user-images.githubusercontent.com/27874014/172537608-7e4a8f0b-2a88-4878-a5fe-a021a2db95a4.png">


This is a self trained squad style extractive question answer model

You can try to input a question and realtive context to see the answer.

<br/>

<h2>
Generate a question on entity that located in context:  
</h2>

<img width="1292" alt="5" src="https://user-images.githubusercontent.com/27874014/172537627-9f5d4c75-94bf-480f-afbf-b692a0a4dcac.png">


This is a self trained generator that ca generate a entity related queston on context.
(Guarantee the entity is located in context)

You can try to input a context and one entity in context to see the question.

<br/>

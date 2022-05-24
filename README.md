# nlp-demo
A interface demo for show some nlp tasks

There are three models deplay in a server, that can be test by call some http requests:
(Because use cpu to infer, you many wait some seconds, when call them.)

1 English question to Wikidata style Sparql Query interface:

```py
http://zfcjelr4.dongtaiyuming.net:80/eng_sent_to_query?sent=Where is the city that XiHu located in ?
```
OR
```py
port = 80
url_format = "http://zfcjelr4.dongtaiyuming.net:{}/{}"
resp = requests.post(
    url = url_format.format(port, s2q_task),
    data = {
        "sent": "Where is the city that XiHu located in ?"
    }
).content
resp.decode()
```

this will produce
```py
{'query': 'select distinct?obj where  wd:XiHu wdt:located_in?obj.?obj wdt:not_a_type_but_is_instance_of wd:administrative_division_of_the_South_Asia '}
```

2 Squad style chinese question answer interface:

```py
http://zfcjelr4.dongtaiyuming.net:80/squad?question=特朗普什么时候出生？&context=美国总统特朗普生于上世纪,他在56岁时获得这个奖项。
```
OR
```py
squad_task = "squad"
resp = requests.post(
    url = url_format.format(port, squad_task),
    data = {
        "question": "特朗普什么时候出生？",
        "context": "美国总统特朗普生于上世纪" + ",他在56岁时获得这个奖项。"
    }
).content
resp.decode()
```

this will produce
```py
{'answers': [{'answer': '上世纪', 'type': 'extractive', 'score': 0.5670798122882843, 'context': '美国总统特朗普生于上世纪,他在56岁时获得这个奖项。', 'offsets_in_document': [{'start': 9, 'end': 12}], 'offsets_in_context': [{'start': 9, 'end': 12}], 'document_id': 'f3633225ec0d3e98b834cecf565d5df3', 'meta': {}}], 'query': '特朗普什么时候出生？', 'no_ans_gap': 0.5969600677490234}
```

3 Generate a question on entity that located in context:

```py
http://zfcjelr4.dongtaiyuming.net:80/gen_question?span=特朗普&context=美国总统特朗普生于上世纪,他在56岁时获得这个奖项。
```
OR 
```py
qst_gen_task = "gen_question"
resp = requests.post(
    url = url_format.format(port, qst_gen_task),
    data = {
        "span": "特朗普",
        "context": "美国总统特朗普生于上世纪" + "他在56岁时获得这个奖项。"
    }
).content
resp.decode()
```

this will produce
```py
{'question': ['哪个总统赢得了奖项?']}
```

You can change the parameters in requests to see the output.

# Overview - News API

## Table of Contents
1. [HOST](#HOST)
2. [ENDPOINT-list](#ENDPOINT-list)
3. [ENDPOINT-detail](#ENDPOINT-detail)

---
## HOST

https://test-miniprogram.com

---
## ENDPOINT-list

__GET /api/news/list__

__Request__

| parameter | type      | description                                                           |
|:--        |:--        |:--                                                                    |
| type      | String    | categories of news，value is one of gn, gj, cj, yl, js, ty and other  |

__Response__

```json
{
    "code": 200,
    "message": "success",
    "result": [
        {
            "id": 1519631218506,
            "title": "外媒称香港回归15年打破“经济将死”预言",
            "date": "2012-07-01T09:34:12.000Z",
            "source": "中国新闻网",
            "firstImage": "http://img1.gtimg.com/news/pics/hv1/38/85/1076/69988613.jpg"
        },
        {
            "id": 1519631218591,
            "title": "实德指媒体窃公司机密 已向某媒体递律师函",
            "date": "2012-04-21T11:32:04.000Z",
            "source": "腾讯财经",
            "firstImage": "http://img1.gtimg.com/finance/pics/hv1/33/207/1023/66573393.jpg"
        },
        {
            "id": 1519631218595,
            "title": "公务员医疗费用成迷 学者呼吁管理应公开透明",
            "date": "2012-02-26T08:13:00.000Z",
            "source": "财新网",
            "firstImage": "http://img1.gtimg.com/finance/pics/hv1/241/102/983/63945826.jpg"
        }
    ]
}
```
---
## ENDPOINT-detail

__GET /api/news/detail__

__Request__

| parameter | type      | description   |
|:--        |:--        |:--            |
| id        | Number    | news id       |

__Response__

```json
{
    "code": 200,
    "message": "success",
    "result": {
        "id": 1519631218693,
        "title": "外媒称香港回归15年打破“经济将死”预言",
        "date": "2012-07-01T09:34:12.000Z",
        "source": "中国新闻网",
        "firstImage": "http://img1.gtimg.com/news/pics/hv1/38/85/1076/69988613.jpg",
        "content": [
            {
                "type": "p",
                "text": "报道特别强调金融合作方面，中央支持第三方利用香港办理人民币贸易投资结算，进一步丰富香港人民币离岸产品”。自1997年7月1日回归之后，香港与内地的经济关系日益紧密，“北京方面迫切希望利用这个全球金融中心来进行重大改革试验，比如将人民币国际化的努力。”"
            },
            {
                "type": "p",
                "text": "一些香港居民在接受美国CNN采访时表达了对香港特区以及新任特首的看法。多数香港居民认为，回归以来，“一国两制”实行得不错，相信“一国两制”将进展良好，相信香港的前途会更光明。希望新任特首上台后，能进一步改善包括住房在内的民生条件。"
            }
        ],
        "readCount": 471
    }
}
```

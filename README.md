# OpenGEO

中文 AI 搜索观测记录。同一个问题，问几家国产 AI，抓包看它们怎么改写搜索词、搜了什么、最后挑了哪些来源。

网站：<https://opengeo.page/> · English: <https://opengeo.page/en/>

## 观测记录

| 编号 | 题目 | 数据 |
| --- | --- | --- |
| 001 | [AI 搜索是怎么推荐的？抓包实测 5 家国产 AI 的搜索词改写与引用来源](https://opengeo.page/observations/001-suzhou-yimei/)（[English](https://opengeo.page/en/observations/001-suzhou-yimei/)） | [Hugging Face](https://huggingface.co/datasets/Maodian/opengeo-observation-001) |

001 的问题是「苏州当地有哪些医美？」，测了豆包、千问、腾讯元宝、Kimi、DeepSeek。主要发现：

- 同一句话，千问改写出 1 条搜索词，Kimi 3 条，豆包 5 条。
- 豆包把上一轮对话里的企业名带进了下一轮搜索词。
- 千问检索到 20 条结果，只把 5 条交给模型。

这是单次测试，结论的边界写在文章的「测试方法与局限」一节。

## 怎么做的

- 在平台的正常对话里提问，同时抓取网络请求。
- 从抓包里提取搜索词、来源、工具调用和埋点字段，脱敏后公开。
- 每篇文章写明测试时间、平台、轮次和局限；数字都能在数据集里找到对应记录。

## 原则

- 只观测，不教铺稿，非商业。
- 不公开任何客户或个人信息。
- 数据和方法公开，欢迎复现和指错。

## 授权

- 文章与数据：[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh-hans)，注明「来源：OpenGEO 项目」并附原文链接即可。
- 代码：MIT。

详见 [转载与引用](https://opengeo.page/reuse/)。

## 引用

```
何瑜. AI 搜索是怎么推荐的？抓包实测 5 家国产 AI 的搜索词改写与引用来源. OpenGEO, 2026-11-05. https://opengeo.page/observations/001-suzhou-yimei/
```

也可以用仓库里的 `CITATION.cff`。

## 联系

作者：何瑜（He Yu）· [help@opengeo.page](mailto:help@opengeo.page) · 发现错误请直接开 issue。

---

**English.** OpenGEO is a small, non-commercial log of how Chinese AI assistants search: we ask several of them the same question, capture the traffic, and compare how each rewrites the query and filters sources. Articles and data are CC BY 4.0. Start with [observation 001](https://opengeo.page/en/observations/001-suzhou-yimei/).

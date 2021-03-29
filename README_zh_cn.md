[![Build Status](https://travis-ci.com/hankcs/gohanlp.svg?branch=main)](https://travis-ci.com/hankcs/gohanlp)
[![Go Report Card](https://goreportcard.com/badge/github.com/hankcs/gohanlp)](https://goreportcard.com/report/github.com/hankcs/gohanlp)
[![GoDoc](https://godoc.org/github.com/hankcs/gohanlp?status.svg)](https://godoc.org/github.com/hankcs/gohanlp)

# gohanlp
中文分词 词性标注 命名实体识别 依存句法分析 语义依存分析 新词发现 关键词短语提取 自动摘要 文本分类聚类 拼音简繁转换 自然语言处理

## [HanLP](https://github.com/hankcs/HanLP) 的golang 接口
- 在线轻量级RESTful API
- 仅数KB，适合敏捷开发、移动APP等场景。服务器算力有限，匿名用户配额较少
- 支持基于等宽字体的[可视化](https://hanlp.hankcs.com/docs/tutorial.html#visualization)，能够直接将语言学结构在控制台内可视化出来
  
## 使用方式

### 安装
```
go get -u github.com/hankcs/gohanlp@main

```
#### 使用

#### 申请auth认证

https://bbs.hanlp.com/t/hanlp2-1-restful-api/53

#### 文本形式

```
client := hanlp.HanLPClient(hanlp.WithAuth("你申请到的auth")) // auth不填则匿名
s, _ := client.Parse("2021年HanLPv2.1为生产环境带来次世代最先进的多语种NLP技术。阿婆主来到北京立方庭参观自然语义科技公司。",hanlp.WithLanguage("zh"))
fmt.Println(s)
```

#### 对象形式

```
client := hanlp.HanLPClient(hanlp.WithAuth("你申请到的auth")) // auth不填则匿名
resp, _ := client.ParseObj("2021年HanLPv2.1为生产环境带来次世代最先进的多语种NLP技术。阿婆主来到北京立方庭参观自然语义科技公司。",hanlp.WithLanguage("zh"))
fmt.Println(resp)
```



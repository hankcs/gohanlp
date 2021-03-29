
[![Build Status](https://travis-ci.com/hankcs/gohanlp.svg?branch=main)](https://travis-ci.com/hankcs/gohanlp)
[![Go Report Card](https://goreportcard.com/badge/github.com/hankcs/gohanlp)](https://goreportcard.com/report/github.com/hankcs/gohanlp)
[![GoDoc](https://godoc.org/github.com/hankcs/gohanlp?status.svg)](https://godoc.org/github.com/hankcs/gohanlp)

## [中文文档](README_zh_cn.md)

# gohanlp
[HanLP](https://github.com/hankcs/HanLP) The multilingual NLP library for researchers and companies, built on PyTorch and TensorFlow 2.x, for advancing state-of-the-art deep learning techniques in both academia and industry. HanLP was designed from day one to be efficient, user friendly and extendable. It comes with pretrained models for various human languages including English, Chinese and many others.



## Usage

### install

```
go get -u github.com/hankcs/gohanlp@main

```

#### Apply for auth certification

https://bbs.hanlp.com/t/hanlp2-1-restful-api/53

#### text model

```go
package main

import (
	"fmt"
	"github.com/hankcs/gohanlp/hanlp"
)

func main() {
    client := hanlp.HanLPClient(hanlp.WithAuth("The auth you applied for")) // If not, anonymity
    s, _ := client.Parse("In 2021, HanLPv2.1 delivers state-of-the-art multilingual NLP techniques to production environments.",hanlp.WithLanguage("mul"))
    fmt.Println(s)
}
```

#### object model

```go
package main

import (
	"fmt"
	"github.com/hankcs/gohanlp/hanlp"
)

func main() {
    client := hanlp.HanLPClient(hanlp.WithAuth("The auth you applied for")) // If not, anonymity
    resp, _ := client.ParseObj("In 2021, HanLPv2.1 delivers state-of-the-art multilingual NLP techniques to production environments.",hanlp.WithLanguage("mul"))
    fmt.Println(resp)
}
```



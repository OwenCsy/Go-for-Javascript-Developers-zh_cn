# 介绍

现如今，一位编程者经常会使用多种编程语言。在不同的语言间切换会伴随额外的开销。同时，这些环境的变动往往也会导致bug的出现。例如，如果你在Python和Javascript间切换，可能的情况是，你会混淆关于空数组和布尔值的转换规则<sup>1</sup>。同样的，当你在Go和Javascript间切换时，你可能会模糊switch关键字在break/fallthrough上的默认行为<sup>2</sup>。为语言的不同提纲挈领能够减少这些潜在错误发生的可能，同时让它们能够更加容易的进行切换。

这篇文档比较了两种不同的语言，Golang('Go')以及ECMAScript('Javascript'/'JS')。这个搭配的优点是由于这两种语言的流行。这是关键。他们其实并不相似，实际上，他们存在巨大的差异。Javascript是一种事件驱动的，动态类型的解释性语言。然而Go是一种静态的编译型语言。

如果你正在读这篇文章，那么很大几率，你已经非常了解Javascript但是并不怎么了解Go。要是这样，确保你先完成[A tour of go](https://go.dev/tour/)以及[Effective go](https://golang.org/doc/effective_go.html)


# 我应该选择哪种语言？
你应该为工作选择正确的语言。不幸的是，这里不存在一种简单方案来指示你选择哪种语言来解决现有的问题。
![image1](http://www.pazams.com/Go-for-Javascript-Developers/images/science_art.png)
除了技术上的考量以外，其他的方面，例如社区接受度也是非常重要的。据[报道](http://highscalability.com/blog/2014/2/26/the-whatsapp-architecture-facebook-bought-for-19-billion.html)，Facebook将因为缺少合适的开发者而从Erlang语言进行迁移。

话虽如此，值得指出的是，Javascript适合于IO密集型的应用，但在CPU密集型的实践中并不那么得心应手。

# 语义
每一个子章节/主题均使用(D),(S)或(B)，来比较两种语言，是（大致不同 mostly <b>D</b>ifferent）或（大体相似 mostly <b>S</b>imilar）抑或（二者兼备 mostly <b>B</b>oth）的。

这篇文档使用ECMAScript 2015(ES6)，同时，一些主题会指出使用的是运行时环境“NodeJS”。

# 贡献
本书非常欢迎大家的建议，指正以及贡献。对于这些事项，请访问本书的源码[https://github.com/pazams/go-for-javascript-developers](https://github.com/pazams/go-for-javascript-developers)以及创建issue或pull-request

# 注
1. 在Python中，空数组在判断时等同于false，而在Javascript中，空数组等同于true
2. 在Javascript中，不存在break时，语句会贯穿执行，而在Go中，当某一个case语句执行完后，不存在贯穿行为
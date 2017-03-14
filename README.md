# 笔试题型总结
- 马上就要过年了，而过完年，马上便是各大公司的校招，各个还在学校的童鞋也都要出来找实习单位了，那么如何让我们在面试以及笔试中脱颖而出呢？答案之一便是：多刷题，刷好题。下面我分别总结了（html/css进阶篇 ） （javascript进阶篇）相信可以作为大家升职加薪提供筹码。
- 注：在笔试中很多知识点还请深刻记忆，哪怕是你本身觉得自己已经懂得，但是如果要像面试官解释清楚，也许还不一定做得到，以及某些算法题型，日常不加以练习，可能临场发挥不一定写的出来，或者会花比较长的时间来进行解答，这些都是面试中的减分项。

1. [html/css篇面试题](https://github.com/Kelichao/work.expressive/issues/11)
2. [javascript篇面试题](https://github.com/Kelichao/work.expressive/issues/12)

# 实用的前端工具站点


- [查询可以使用的css/js属性的网站caniuse](http://caniuse.com/)
- [画svg矢量图](http://editor.method.ac/)
- [自动添加前缀网站](http://autoprefixer.github.io/)
- [JavaScript 标准参考教程（alpha）阮一峰](http://javascript.ruanyifeng.com/)
- [ECMAScript 6 入门 阮一峰](http://es6.ruanyifeng.com/)
- [在线画流程图的页面](https://www.draw.io/)
- [思维导图工具](http://www.xmindchina.net/)
- [码农头条](http://hao.caibaojian.com/)
- [css命名规范](http://www.zhangxinxu.com/wordpress/2010/09/%E7%B2%BE%E7%AE%80%E9%AB%98%E6%95%88%E7%9A%84css%E5%91%BD%E5%90%8D%E5%87%86%E5%88%99%E6%96%B9%E6%B3%95/)
- [在线格式化代码](http://tool.oschina.net/codeformat/js)
- [在线babel转换](http://babeljs.io/repl/)


# 编写可维护的Javascript代码

# 一、基本的格式化
## 1.1缩进
> 推荐的是一个tab，优点是比较便捷，而且层级明显，缺点是不同的编辑器对tab Size的理解不一样。

```js
if (1) {
    if (2) {
        if (3) {
            // some code
        }
    }
}
``` 
## 1.2语句结尾
> 推荐在非条件语句结束时统一加上分号“;”

```js
// 推荐
var name = "Bob";
// 不推荐
var age = 100
```

## 1.3 行的长度
> 推荐将行的长度限制在80个字符

## 1.4 换行
> 换行后需要两个tab，并且逗号需要留在上一行

```js
// 换行后需要两个tab，并且逗号需要留在上一行
doit(element, window, document, "some code", true, 
        "abc", "def");
```
## 1.5空行
1. 在方法之间。
2. 在方法中的局部变量和第一条语句之间。
3. 在多行或单行注释之前。
4. 在方法内的逻辑片段之间插入空行，提高可读性。

## 1.6命名
> 驼峰法用于普通变量，功能函数

`var anotherNames`

> 首字符大写用于构造函数

`function Model(){// somecode}`

> 全大写字母用于常量

`var PERSON_COUNT = 10;`
## 1.6.1变量和函数
> 变量名前缀应当为名词

```js
var count = 10;
var myName = "Bob";
```

> 方法函数名应该以动词开头

```js
function getName() {
    // some code
}
```

<table>
    <tr>
        <td>动词</td>
        <td>含义</td>
    </tr>
    <tr>
        <td>can</td>
        <td>返回布尔值</td>
    </tr>
    <tr>
        <td>has</td>
        <td>返回布尔值</td>
    </tr>
    <tr>
        <td>is</td>
        <td>返回布尔值</td>
    </tr>
    <tr>
        <td>get</td>
        <td>返回一个非布尔值</td>
    </tr>
    <tr>
        <td>set</td>
        <td>用于保存值</td>
    </tr>
</table>

## 1.7直接量
> 换行

```js
//合法，但不推荐
var str = "asdfghjklzxc\
vbnbm";

// 推荐 "+" 分割
var str = "asdfghjklzxc" + 
          "vbnbm";
```

# 二、注释
> 单行注释

```js

// 我是单行注释
fn();
```

> 多行注释

```js

/*
 * 这是一个多行注释
 * 星号后面要留空格
 */
fn();
```

> 特殊注释

```js
/*
 * TODO: 说明代码还未完成，应当包含下一步要做的事。
 * HACK: 该问题可能有更好的解决办法
 * XXX：说明代码是有问题的，应当尽快修复
 * FIXME: 有问题，要紧程度比XXX低
 * REVIEW: 说明代码任何可能的改动都需要评审
 */
```

# 三、语句和表达式
## 3.1
> 注意空格，对齐花括号

```js
if (condiction) {

}
```

## 3.2循环语句中的变量提前
```js
var i;
for (i = 0; i < 10; i++) {
    // some code
}
```

## 3.3运算符间距
```js
var fond = (value1 === value2);
```

## 3.4三元运算符的处理
```js
 var instanceData = typeof childVal === 'function'
 ? childVal.call(vm)
 : childVal;
```
# 四、变量声明
## 4.1
```js
// 推荐多var方式声明变量
// 且统一放在函数体顶部
var a = 1;
var b = 2;
var c = 3;
```

## 4.2

>推荐用全等(===)代替双等
```js
if (1 === "1") {
    // some code
}
```



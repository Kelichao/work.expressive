# Chrome技巧
一、选择器
> 不管有無引入jQuery，都可以通过$(selector)选取元素

二、查找DOM中元素关联的事件
> 可以查看普通绑定事件，对jq等库不奏效。getEventListeners($(‘firstName’)).click[0].listener

三. 查询代码块执行时间
> console.time('myTime'); //Starts the timer with label - myTime
> console.timeEnd('myTime'); //Ends the timer with Label - myTime

四、将数据生成表格

> console.table([{a:1, b:2, c:4}]) 

![image](https://cloud.githubusercontent.com/assets/18028533/25693756/a9b84606-30dd-11e7-8514-72895c8a47c2.png)

五、定位到对应元素
> inspect($('selector')) 

六、选中之前检查过的元素
> $0    $1     $2.......

七、列举出元素所有属性

> dir($('selector')) 

八、获取最近一个结果值

> $_

九、清空控制台和内存
> clear()

十、带格式的输出
```js
console.group("%c ws通讯消息","color:#296ab4;");
console.log(112233);
console.end();
```


# 妙味课堂-CSS3

标签（空格分隔）： CSS

---
#### 学习CSS3之前先讲几个问题：
- 浏览器支持问题
- 厂商前缀问题
- 在JS中的写法：-webkit-transition => WebkitTransition; -o-transition  => OTransition; -moz-transition => MozTransition

## CSS3选择器 - 属性选择器
- E[attr]只使用属性名，但没有确定任何属性值
- E[attr="value"]指定属性名，并指定了该属性的属性值
- E[attr~="value"]指定属性名，并且具有属性值，此属性值是一个词列表，并且以空格隔开，其中词列表中包含- 了一个value词，而且等号前面的“~”不能不写
- E[attr^="value"]指定了属性名，并且有属性值，属性值是以value开头的
- E[attr$="value"]指定了属性名，并且有属性值，而且属性值是以value结束的
- E[attr*="value"]指定了属性名，并且有属性值，而且属值中包含了value
- E[attr|="value"]指定了属性名，并且属性值是value或者以“value-”开头的值（比如说zh-cn）
- 实例：百度文库;
- 备注：IE7以上支持

### 属性选择器

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS3选择器</title>
    <style>
        p {height: 30px; border: 1px solid #000;}
        /*p[miaov] {background: red;} */ /*所有四个*/
        /*p[miaov=g-xM] {background: red;}*/ /*第四个小美*/
        /*p[miaov~=old] {background: red;}*/ /*第一个leo*/
        /*p[miaov^=g] {background: pink;}*/ /*第四个小美*/
        /*p[miaov$=M] {background: #cc0;}*/ /*第三、四个：子鼠和小美*/
        /*p[miaov*=d] {background: purple;}*/ /*第一、二个：leo和杜鹏*/
        /*p[miaov|=b] {background: purple;}*/ /*第一、二、三和最后一个：leo、杜鹏和子鼠、无名氏*/
    </style>
</head>
<body>
    <p miaov="b-leo old">leo</p>
    <p miaov="b-dp">杜鹏</p>
    <p miaov="b-zM">子鼠</p>
    <p miaov="g-xM">小美</p>
    <p miaov="b">无名氏</p>
</body>
</html>
```

### 实例：百度文库
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>百度文库</title>
    <style>
        p {height: 30px; line-height: 30px; font-size: 12px; border: 1px solid #000;}
        p a {background: url(img/w.gif) no-repeat 3px center; padding-left: 20px; display: block;}
        p a[href*=text]{background: url(img/text.gif) no-repeat 3px center;}
        p a[href*=pdf]{background: url(img/swf.gif) no-repeat 3px center;}
        p a[href*=exl]{background: url(img/x.gif) no-repeat 3px center;}
    </style>
</head>
<body>
    <p><a href="http://www.miaov.com/doc/javascript.html">妙味课堂</a></p>
    <p><a href="http://www.miaov.com/text/javascript.html">妙味课堂</a></p>
    <p><a href="http://www.miaov.com/pdf/javascript.html">妙味课堂</a></p>
    <p><a href="http://www.miaov.com/doc/javascript.html">妙味课堂</a></p>
    <p><a href="http://www.miaov.com/exl/javascript.html">妙味课堂</a></p>
</body>
</html>
```


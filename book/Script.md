# 常用JS代码
#### 1. Jquery 获取除自己之外的兄弟标签
```js
obj.siblings(); 
```
#### 2. 求数组里的最小数
```js
Math.min.apply(null, arr);
```
#### 3. 转换成json字符串
```js
JSON.stringify(arrlist);
```
#### 4. 禁用移动端滚动条滚动
```js
//禁用
$('body').bind("touchmove", function (e) {
    e.preventDefault();
});
//解除
$('body').unbind("touchmove");
```
#### 5. 获取范围内随机数
```js
function random(min, max) {
    return Math.floor(min + Math.random() * (max - min));
}
```
#### 6. js截取URL字段值
```js
//getQueryString("id");
function getQueryString(name) {
    var reg = new RegExp("(^|&)" + name + "=([^&]*)(&|$)", "i");
    var r = window.location.search.substr(1).match(reg);
    if (r != null) return unescape(r[2]); return "";
}
```
#### 7. 基本语法
##### 7. 1
```js
$.ajax({
    type: "post",
    contentType: "application/x-www-form-urlencoded; charset=utf-8",
    url: "url",
    data: {},
    dataType: "text",
    cache:false,
    async: false,
    beforeSend:function () {
        console.log("处理中...");
    },
    success: function (data) {
        console.log("成功!");
    },
    err: function (xhr, textStatus,error) {
        console.log("失败:"+xhr.status+"|"+xhr.readyState+"|"+textStatus);
    }
});
```

|参数名| 描述 |
|-|-|
|type|提交方式|
|contentType|声明|
|url|提交处理URL|
|data|提交参数|
|dataType|返回值类型|
|cache|是否缓存|
|async|同/异步加载|
|beforeSend|提交前处理函数|
|success|处理成功函数|
|error|处理失败函数|

#### iframe 高度自适应
``` js
var iframeHeight = 62;
        function changeFrameHeight() {
            var ifm = document.getElementById("iframepage");
            ifm.height = document.documentElement.clientHeight - iframeHeight;
        }
        window.onresize = function () { changeFrameHeight(); }
        $(function () { changeFrameHeight(); });
```


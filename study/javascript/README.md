# javascript

javascript负责告示浏览器你的页面怎么用

例如你需要用户输入两个数，显示相加结果  
一个简单的加法例子
```html
<div>
  <input id="value1" type="number" />
  +
  <input id="value2" type="number" />
  <input id="result" readonly />
</div>
<script>
  /**获取三个输入框的操作对象（dom元素）用这些对象来获取和修改输入框的内容 */
  const value1 = document.getElementById("value1"),
        value2 = document.getElementById("value2"),
        result = document.getElementById("result");
  value1.onchange = value2.onchange = () =>
    (result.value = value1.value + value2.value)
</script>
```
例子看不懂？请继续往下看
>### 引入javascript的两种方法
>```html
><!--外部引入,通常javascript文件以js作为后缀-->
><script src="index.js"></script>
><!--直接在script标签中写-->
><!--或许你的第一个js代码应该长这样-->
><script>
>  alert("hello world")
></script>
>```

>### javascript注释  
>注释不参与程序运行，但能给你的代码加上说明，既能方便别人理解你的代码，又能在修改代码时更快的从大量代码中找到你要改的内容
>```javascript
>//我是单行注释
>/** 
> * 我的多行注释
> */
>```

>### javascript变量，常量等声明
>```javascript
>/**用var字段声明变量 */
>var a = "hello world"
>/**用const 声明常量，常量值无法被改变 */
>const b = "hello world"
>/**let声明局部变量 */
>let c = "hello world"
>/**啥字段也不要也能声明个变量，但是不推荐这种方法 */
> d = "hello world"
>```
>mdn文档 => [var](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Statements/var)，[const](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Statements/const)，[let](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Statements/let)

>### javascript获取html元素的操作对象（dom） 
>关于dom? ... 瞅这 =>[![mdn%E4%BC%A0%E9%80%81%E9%97%A8](../../icon/mdn传送门.svg)](https://developer.mozilla.org/zh-CN/docs/Glossary/DOM)  
>
>先给元素个id
>```html
><div id="demo1"></div>
>```
>根据id获取元素
>```javascript
>/**传统方法根据id获取dom*/
>const dom = document.getElementById("demo1")
>/**document.querySelector里面的参数就一css选择器 */
>const dom = document.querySelector("#demo1")
>/**document.querySelectors可以选多个，返回的数组 */
>const doms = document.querySelector("div")
>```
>啥，你问啥是css选择器？瞅这 [css选择器](../css/css%E9%80%89%E6%8B%A9%E5%99%A8.md)
>
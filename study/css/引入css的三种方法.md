# 引入css的三种方法
>### 方法一  
>&ensp;html标签中使用style属性，设置的css样式只针对与该标签  
示例：
>>```html
>><div style="width:100px;height:100px;background-color: red;"></div>
>>```  
设置这个div标签的宽、高为100px,背景颜色为红色

>### 方法二
>&ensp;使用`<style>`标签，它通常和文字内容无关，所以通常放到`<head>`标签中  
示例
>>##### 注：代码以html[基础页面](../html/%E5%9F%BA%E7%A1%80%E9%A1%B5%E9%9D%A2.md)为前提，注释为添加内容的说明
>>```html
>><!DOCTYPE html>
>><html>
>><head>
>>  <meta charset="UTF-8">
>>  <title>新建文档</title>
>>  <style>
>>    /**将class为block的元素宽高设置成100px,背景颜色为红色 */
>>    .block {
>>      width: 100px;
>>      height: 100px;
>>      background-color: red;
>>    }
>>  </style>
>></head>
>><body>
>>  <!-- 添加一个div元素，设置该元素属于block类 -->
>>  <div class="block"></div>
>></body>
>></html>
>>```
>### 方法三
>&ensp;使用`<link>`标签引入外部css
>>示例  
>>##### 文件index.html
>>```html
>><!DOCTYPE html>
>><html>
>><head>
>>  <meta charset="UTF-8">
>>  <title>新建文档</title>
>>  <!--引入一个外部资源,rel="stylesheet"说明这个引入的资源是stylesheet(样式表) href="index.css"指资源的url地址，此处指同文件夹下的index.css文件-->
>>  <link rel="stylesheet" href="index.css"/>
>></head>
>><body>
>>  <!-- 添加一个div元素，设置该元素属于block类 -->
>>  <div class="block"></div>
>></body>
>></html>
>>```
>>##### 文件index.css
>>```css
>>/**将class为block的元素宽高设置成100px,背景颜色为红色 */
>>.block{
>>   width:100px;
>>   height:100px;
>>   background-color: red;
>>}
>>```
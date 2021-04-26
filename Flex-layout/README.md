### 实现Flex布局（display:flex）  
  
网页布局（layout）是 CSS 的一个重点应用。  
![Image](https://github.com/srqAndwr/CSS-Skill/blob/main/Flex-layout/img/layout.gif)   
  
布局的传统解决方案，基于盒状模型，依赖 display 属性 + position属性 + float属性。它对于那些特殊布局非常不方便，比如，垂直居中就不容易实现。  
![Image](https://github.com/srqAndwr/CSS-Skill/blob/main/css-chargingWave/img/charging-wave.gif)  
2009年，W3C 提出了一种新的方案----Flex 布局，可以简便、完整、响应式地实现各种页面布局。目前，它已经得到了所有浏览器的支持，这意味着，现在就能很安全地使用这项功能。
![Image](https://github.com/srqAndwr/CSS-Skill/blob/main/Flex-layout/img/brower.jpg)   
  
    
## 一、Flex 布局是什么？  
Flex 是 Flexible Box 的缩写，意为"弹性布局"，用来为盒状模型提供最大的灵活性。  
任何一个容器都可以指定为 Flex 布局。  
```pug
.box{
  display: flex;
}
```
行内元素也可以使用 Flex 布局。  
```pug
  .box{
     display: inline-flex;
  }
```
Webkit 内核的浏览器，必须加上-webkit前缀。  
```pug
.box{
   display: -webkit-flex; /* Safari */
   display: flex;
}
```

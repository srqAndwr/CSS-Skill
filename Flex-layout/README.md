### 实现Flex布局（display:flex）  
  
网页布局（layout）是 CSS 的一个重点应用。  
![Image](https://github.com/srqAndwr/CSS-Skill/blob/main/Flex-layout/img/layout.gif)   
  
布局的传统解决方案，基于盒状模型，依赖 display 属性 + position属性 + float属性。它对于那些特殊布局非常不方便，比如，垂直居中就不容易实现。  
![Image](https://github.com/srqAndwr/CSS-Skill/blob/main/Flex-layout/img/css-flex.png)  
2009年，W3C 提出了一种新的方案----Flex 布局，可以简便、完整、响应式地实现各种页面布局。目前，它已经得到了所有浏览器的支持，这意味着，现在就能很安全地使用这项功能。
![Image](https://github.com/srqAndwr/CSS-Skill/blob/main/Flex-layout/img/brower.jpg)   
  
    
## 一、Flex 布局是什么？  
Flex 是 Flexible Box 的缩写，意为"弹性布局"，用来为盒状模型提供最大的灵活性。  
任何一个容器都可以指定为 Flex 布局。  
```javascript
  .box{
      display: flex;
  }
```
行内元素也可以使用 Flex 布局。  
```javascript
  .box{
     display: inline-flex;
  }
```
Webkit 内核的浏览器，必须加上-webkit前缀。  
```javascript
  .box{
     display: -webkit-flex; /* Safari */
     display: flex;
  }
```
注意，设为 Flex 布局以后，子元素的float、clear和vertical-align属性将失效。  
  
  
## 二、基本概念
采用 Flex 布局的元素，称为 Flex 容器（flex container），简称"容器"。它的所有子元素自动成为容器成员，称为 Flex 项目（flex item），简称"项目"。  
![Image](https://github.com/srqAndwr/CSS-Skill/blob/main/Flex-layout/img/container.png)  
容器默认存在两根轴：水平的主轴（main axis）和垂直的交叉轴（cross axis）。主轴的开始位置（与边框的交叉点）叫做main start，结束位置叫做main end；交叉轴的开始位置叫做cross start，结束位置叫做cross end。  
项目默认沿主轴排列。单个项目占据的主轴空间叫做main size，占据的交叉轴空间叫做cross size。  
  
  
## 三、容器的属性  
以下6个属性设置在容器上。  
```javascript
  *flex-direction
  *flex-wrap
  *flex-flow
  *justify-content
  *align-items
  *align-content
```
### 3.1 flex-direction属性  
`flex-direction'属性决定主轴的方向（即项目的排列方向）。  


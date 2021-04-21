## 先上效果图  
[!Image](https://github.com/srqAndwr/CSS-Skill/blob/main/css-chargingWave/img/charging-wave.gif)  

### 今天的任务就是运用css样式来实现一个波浪式动画。  
## 原理  
原理十分简单，我们都知道，一个正方形，给它添加 border-radius: 50%，将会得到一个圆形。  
[!Image](https://github.com/srqAndwr/CSS-Skill/blob/main/css-chargingWave/img/circle.png)  
+ border-radius：用来设置边框圆角，当使用一个半径时确定一个圆形。
好的，如果 border-radius 没到 50%，但是接近 50% ，我们会得到一个这样的图形：  
[!Image](https://github.com/srqAndwr/CSS-Skill/blob/main/css-chargingWave/img/45%25circle.png)   
注意边角，整个图形给人的感觉是有点圆，却不是很圆。  
 我们让上面这个图形滚动起来(rotate) ，看看效果：  
 [!Image](https://github.com/srqAndwr/CSS-Skill/blob/main/css-chargingWave/img/45%25translate.gif)  
可能很多人看到这里还没懂旋转起来的意图，仔细盯着一边看，是会有类似波浪的起伏效果的。  
而我们的目的，就是要借助这个动态变换的起伏动画，模拟制造出类似波浪的效果。  

## 实现  
我们通过一个例子来看看具体实现起来能达到什么样的效果  
我们利用上面原理可以做到的一种波浪运动背景效果图：  
[!Image](https://github.com/srqAndwr/CSS-Skill/blob/main/css-chargingWave/img/wave.gif)   
+ 注意，这里背景是蓝色静止的，运动是白色的椭圆形。  


## 技巧  
单纯的让一个 border-radius 接近 50 的椭圆形旋转，动画效果可能不是那么好，我们可以适当的添加一些其他变换因素，让动画效果看上去更真实：

在动画过程中，动态的改变 border-radius 的值；
在动画过程中，利用 transform 对旋转椭圆进行轻微的位移、变形；
上面也演示到了，多个椭圆同时转动，赋予不同时长的动画，并且添加轻微的透明度，让整个效果更佳逼真。  

喜欢的点歌star吧。

## 一、 实现过程
1. 传统布局

参考[css+js实现banner图片轮播](https://frogfans.github.io/blog.html?blogId=17)，其中banner实现过程即为传统布局，按照左-中-右顺序渲染。

2. 圣杯布局

参考[【聊一聊】css中的经典布局——圣杯布局](http://www.cnblogs.com/hl-520/p/5753075.html)，按照博主教程逐步尝试，并加以理解。

3. 双飞翼布局

参考[【聊一聊】css中的经典布局——双飞翼布局](https://www.cnblogs.com/hl-520/p/5754111.html)，在圣杯布局基础上改造。

---
## 二、 实际体验

[固比固三栏式布局对比](https://frogfans.github.io/blog.html?blogId=18)

对整个浏览器窗口进行缩放即可。

---
## 三、 对比总结
- 总宽度：

Left 250px + Main + Right 300px。

![](https://github.com/frogfans/ThreeColumnLayout/blob/master/img/001.png?raw=true)

** **
- 第一个临界值：700px，即 Main = Left 时：

**圣杯布局** 被挤乱。

![](https://github.com/frogfans/ThreeColumnLayout/blob/master/img/002.png?raw=true)

** **
- 第二个临界值：550px + Main容纳文字的最小宽度：

**传统布局** 中Left和Right被压缩，Main固定为最小宽度；

**圣杯布局** 中Main被压缩，整个布局混乱；

**双飞翼布局** 中Main被压缩，整个布局保持秩序。

![](https://github.com/frogfans/ThreeColumnLayout/blob/master/img/003.png?raw=true)

** **
- 第三个临界值：550px，即 Main = 0 时：

**圣杯布局** 整个布局混乱；

**双飞翼布局** 中Main消失，Left和Right相互遮挡。

![](https://github.com/frogfans/ThreeColumnLayout/blob/master/img/004.png?raw=true)

** **
- 对比：

**传统布局** 能很好地保持整个三栏式布局的格式，在无需将Main优先渲染的情况下可以使用；

**圣杯布局** 在将整个布局最小宽度设置为第一个临界值的情况下和双飞翼布局没有区别；

**双飞翼布局** 至少需要将整个布局最小宽度设置为第三个临界值，即Main完全消失时，保证左右栏布局完整。

** **
- 总结：

**传统布局** 保证了Main内容完整，牺牲了左右栏布局；

**圣杯布局** 保证了左右栏布局完整，牺牲了整个布局；

**双飞翼布局** 保证了左右栏相对位置完整，牺牲了Main内容。
#此topo插件是基于Jtopo改编的，感谢原作者：http://www.jtopo.com/

#但是作者已经停止更新了，所以我拉了包自己维护。

#以下是vue/react里的用法，具体api请访问原作者官网

npm i cztp --save

import cztp from 'cztp'

-------------------------

#以下是更新日志：

##1.0.2

date@2020-05-25

name@金角大王

change:

1、更改背景图为空序列化报错

-------------------------

##1.0.3

date@2020-05-25

name@金角大王

change:

1、给每个节点配备deviceId

-------------------------

##1.0.4

date@2020-05-25

name@金角大王

change:

1、序列化的地方补了三个字段，防止填充的时候出现undifined值

-------------------------

##1.0.5

date@2020-05-27

name@金角大王

change:

1、新增了node外设strokeStyle,fillStyle两个属性

2、新增了replaceStageWithJson,getAllNodes两个方法

3、修改了borderRadius默认值null为0，避免转化的时候出现NaN值，导致replaceStageWithJson方法执行失败

-------------------------

##1.0.6

date@2020-05-28

name@金角大王

change:

1、修改了replaceStageWithJson方法中设置图片的方式，并且只有elementType为node类型的时候才设置图片

2、删除所有扩展，因为连初始化元素是node还是TextNode都搞错了。现只保留了源码

3、elementType为link的时候，新增了deviceA.deviceId,deviceZ.deviceId,lineType==link类型

4、删除了elementType==displayElement时的diviceId属性，挪到elementType==node类型下，因为link类型等不需要这个属性

5、对dragable,selected,showSelected,isMouseOver这四个不进行序列化

6、隐藏线的shadowColor

-------------------------

##1.0.7

date@2020-05-28

name@金角大王

change:

1、新增了replaceStageWithJson方法调用的参数（isReplace），如果isReplace == true，全部替换stage，否则只追加

-------------------------

##1.0.8

date@2020-06-09

name@金角大王

change:

1、修改node内设strokeStyle,fillStyle的值

date@2020-06-18

name@金角大王

change:

1、给container自由变动类型增加20内边距

2、去除container选中时候的样式

3、container的text的Top_Left，Top_Right的y值都+20

-------------------------

##1.0.9

date@2020-07-02

name@金角大王

change:

1、对node元素新增btnType字段

2、对container进行字段补充，新增了childNode字段，用来解决编辑topo的时候，调用setLocation失败

3、container的内容边距做了调整，x、y各-20，width、height各+40


-------------------------

##1.1.0

date@2020-07-14

name@金角大王

change:

1、删除对上下左右键的监听，因为输入框里光标无法左右移动了

2、鼠标滚轮事件的修改，放大缩小反一反


-------------------------

##1.1.1

date@2020-07-14

name@金角大王

change:

1、修改border的位置，进行外扩


-------------------------

##1.1.2

date@2020-08-04

name@金角大王

change:

1、修改线的出发位置（横坐标-20），到终点的位置（纵坐标+10）


-------------------------

##1.1.3

date@2020-08-05

name@金角大王

change:

1、在1.0.9中container的内容边距做了调整，但这其实不是合适的做法，所以把1.0.9中关于container的内容边距的修改还原了，改为修改AutoBoundLayout方法里，矩形的绘制边界
2、去掉了线的首尾的空档，因为当endNode在begainNode上方的时候，计算还是有偏差，所以暂时回退1.1.2中修改的点，5G消息平台中可以继续沿用1.1.2版本，其他的项目推荐最新版本




***关于数据可视化 [ QUANTAXIS ] DC***
===========

    数据可视化
    构架

>我们在这一步只干一件事情：将输入的数据交互式的表达出来
>所以问题也变得非常简单，将数据从mysql中取出，然后以一定的方式输入到nodejs后台
>肯定是`json`格式 中间可能需要一些非关系型数据库来完善比如redis，mongoDB
<br>



```
需要的工具

'dc.js'
'mysql'
'cookie-parser'
'ajax'
'redis' 
```
    $todo list
    1. 建立一个nodejs网站
    2. 写好中间件以及路由跳转
    3. 完成与mysql的交互
    4. cookie 与redis缓存
    5. dc.js构架


>mission
>已经搭建好一个服务器+mysql
>现在要干一件事<br>
>做一个list+ajax 动态回显
>或者是treeNodes 动态加载


我们需要仔细对于业务逻辑进行考虑，首先需要考虑的关于算法的逻辑问题

如何对于不同的算法进行优化和回显
如何进行客户端的分布式计算
如何对于不同分布式计算的结果对于服务器进行异步回调的逻辑


使用一种轻量级 稳定 多适应的语言来进行开发是最核心的问题
最好有守护进程以及较好的IO能力



---
关于DC.js 进行数据可视化的问题

数据如何标准化
数据如何废弃和回收

--- 

a to do list 
>关于下面职业生涯规划的转变问题
核心关注的问题应该偏向于机器学习 时间序列 金融的问题的结合和概括

不能脱离金融理论去进行算法的构建
在分形市场理论以及以后的更多理论上
通过机器学习算法去实现更多的可能性
机器学习算法的实现工具--和生产环境下的真实检验
通过一些轻量级和分布式应用的开发和构建
来判断模型最终的好坏问题 


更多的考虑则涉及到一部分的数据可视化
这个属于生产环境下的逻辑问题

数据可视化应该作为一种标准化的流程构建  而不是一种附加
对于数据的严谨的态度和对于产品的严格要求  注定我们不能用一种浮躁的态度来面对我们的结果

数据可视化和交互式数据设计是非常重要的一环

所以总体部分上看，似乎和之前的商业设计/数据挖掘/一体化解决方案提供商没有较大的区别
但是 核心的逻辑以及框架的构成已经完全不同

这可以当做<strong>yutiansut 2.0</strong> 版本的到来和改进
其实主要的核心还是一个逻辑和优先级的问题

什么是主要逻辑  也就对应了框架的架构趋势


对于主要逻辑的追求会附带很多其他的东西  这就需要一个类似目录树的东西， 将逻辑串联起来，把看似无关的各个部分都构建起来


总结起来 我们需要一个能够快速搭建原型并能快速进入生产环境的东西

目前看起来  基于python/go/JavaScript的几种架构都非常具有吸引力

对于golang的调研看起来  go和nodejs的功能出现了较大的相似度 如果坚持使用nodejs做开发的话 和golang的同质化程度较高
没有必要强行上golang
python可以放入考虑的流程中 主要是考虑到基于python的机器学习应用较多 
另外完全使用javascript来进行开发也不是特别的稳定 

对于算法的实现  可以一部分在matlab中实现 也可以放在python中实现

因为matlab对于服务器的安装、支持都较为困难

不如单纯使用python


核心：轻量级 快速应用  开源

似乎是nodejs要比python快上很多 也许研究nodejs是一种很不错的方向

主要是对于算法的实现问题
如何快速实现需要实现的算法 快速的将事件和问题响应起来 
另外 多平台和展示的需要

```
javascript和css的结合  如果我们能够控制这两个在页面上进行一部分的运算  嵌入到网页工具箱中的
另外一部分是网页、客户端提交到主机的一个标准的数据流请求 或者是运算请求  另外是服务器与其他应用的跨域交互应用

前端和后端的并行交互 
需要考虑的另外一个关于算法实现的问题 



对于标准数据流的封装非常的重要 因为对于跨域而言，一个标准的数据传输格式会大大提升交互的效率，采用json或者HFS5格式的
对于json格式的打包而言  matlab显得非常不合时宜  因为matlab的对象化编程注定让其无法以json格式接受数据和传输数据

对于大规模数据传输问题而言 json格式可以穿插着lua脚本和xml格式的数据  来提升数据质量和和特定要求下的数据传输要求


然而现在最大的问题就在于 如何将matlab，python算法更多的实现在javascript中，包括新开发的算法  如何以一种更好的形式去调用和更新

语言的改写  是一种非常浪费时间的事情  对于同一个算法的不同语言实现，有时候甚至浪费了一个项目80%以上的时间
我们希望出现一个类似于html+javascript+css模式架构的东西出现 

html就是应用本身  包括了所有的框架

css是搭在框架上的装饰物和样式  分离出来的样式表可以有效的减少重复开发和代码紊乱的问题

而javascript是所有函数和功能的实现办法  只需要打包完毕 就能在不同的html中运行 发挥作用


我们也希望这种模式分离的类设计思想 能够提高  并进入实际应用的场景中

将算法打包好 在一定api中调用 就能一次性完整实现



我们致力于并希望能够通过构建一个服务主机
通过这个主机处理模拟的市场数据 来构造一个人为金融市场并处理和协调关系





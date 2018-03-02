# 1、JavaScript基础

## 1.1 闭包的原理？
```javascript
function a(){
  alert(1);
}
```

## 1.2 原型链，继承有哪些

### 1.3
```javascript
var bb=1;
function aa(bb){
  bb=2;
  alert(bb);
};
aa(bb);
alert(bb);
```
结果是2,1

## 1.4 JS实现继承有哪些方式
1、使用对象冒充实现继承  
2、使用call  
3、使用apply  
4、采用原型链的方式继承

## 1.5 事件代理
事件代理的原理一个父元素，有两个子元素，两个元素的顺序不定，怎么通过事件代理的方式找到

### 1.6 事件注册

### 1.7 原型

### 1.8 js 对象绑定有哪四种方式

### 1.8 双向绑定原理

# 2、JavaScript进阶

### 2.1 web workers的理解  

### 2.2 设计一个布局方案，使得页面在pc和pad端显示为一行三列，在于手机端为一列三行  

### 2.3 自定义一个浏览器兼容的事件绑定方法需要注意哪些问题  

### 2.4 [跨域有哪些，以及它们之间的区别](https://github.com/sakila1012/font-end-interview-question/issues/3)

### 2.5 js中也会有排序的需求，用js实现一个标准的排序方法，对某个数字数组进行由低到高排序 

### 2.6 将多维数组转换为一维数组，比如[1,[2,3,[5,6,[7,8]]]],转换为[1,2,3,4,5,6,7,8]
解决方案：有两种方式
	将数组转换为字符串[1,[2,3,[5,6,[7,8]]]].join(",").split(",");
        通过正则方式
### 2.7 创建一个js类，模拟实现方法的重载

### 2.8 请根据以下提供的HTML，实现一个图片自动轮图，每3秒切换一张图片，循环播放。（允许使用jQuery）
```html
<style>
  #slider{
    width:250px;
    margin-left:auto;
    margin-right:auto;
    position:relative;
  }
  #slider img{
    width:100%;
  }
</style>
<div id="slider">
  <ul>
    <li><img src="http://example.com/pic01.png"/></li>
    <li><img src="http://example.com/pic02.png"/></li>
    <li><img src="http://example.com/pic03.png"/></li>
  </ul>
</div>
<script>
  
</script>
```
### 2.9 以下代码段中，在'This is a child'文本上点击后，输出的结果是（D）
```html
<div id="root">
		<div id="parent">
			<div id="child">this is a child</div>
		</div>
	</div>
	<script>
		var childEle = document.getElementById("child");
		var parentEle = document.getElementById("parent");
		var rootEle = document.getElementById("root");

		childEle.addEventListener("click",handleEvent,false);
		parentEle.addEventListener("click",handleEvent,false);
		rootEle.addEventListener("click",handleEvent,false);

		function handleEvent(e){
			console.log(e.target.id);
			return false;
		}
	</script>
```
A:child,parent,root;  
B:child;  
C:root,root,root;  
D:child,child,child.  

### 2.10 设计并实现一个combox（下拉选择框）（携程2017机试）  
1、combox内容可编辑，下拉区域可滚动（一共包含了10W条数据）  
2、根据输入的内容做prefix匹配，展示匹配的可选择内容列表（要求提高匹配效率，考察算法能力，空间复杂度和时间复杂度）

### 2.11 你知道哪些JS的第三方库或框架，请举例说明，并阐述他们有哪些优点？  
我知道的有第三方库有jquery，zepto，Angular，react，node.js，bootstrap，vue，还有百度的fis，阿里的weex。

### 2.12 浏览器兼容问题有哪些，怎么解决的

#3、计算机网络

## 3.1 进程是资源分配的最小单位，线程是CPU调度的最小单位
## 3.2 HTTP状态码
1xx 临时响应

2xx 成功


3xx 重定向

4xx 客户端错误
403
404
405
413
5xx 服务器端错误
501
502
503
504
## 3.3 HTTP协议使用的端口号
       默认是使用TCP端口号
## 3.4 无线网络和有线网络在osi结构从上到下从从哪一层开始不一样的？

## 3.5 UDP伪首部

# 4 数据库

    union和union的区别
# 5 二叉树

## 5.1 一个完全二叉树有770个节点，那么它的叶子节点数共有多少个？  
根据二叉树的性质：对于一个非空的二叉树，如果叶子节点数为n0，度为2的节点数为n2，则n0=n2+1;  
根据完全二叉树的定义可得：在完全二叉树度为1的节点n1只能取两种情况，要么为0，要么为1.  
所以n0+n1+n2=770;  
n0=n2+1;  
2n0=770-n1  
n1取1，所以n0=770/2=385  
2^9-1<770<2^10-1  
k=9(该二叉树的高度为k)  
770-(2^9-1)=259 表示第k层有259个节点  
259/2+1=130对应k-1层的父节点  
2^(k-1)-130=126 (第k-1层总共总共有2^8=256个节点，减去非叶子节点130，得到第k-1个叶子节点)  
总共叶子节点数为259+126=385

### 5.1 K-means 的原理，有哪些输入参数

# 6 其他

## 6.1 SQL注入

## 6.2 Oauth2

## 6.3 说说你熟悉的设计模式(https://github.com/FrankKai/FrankKai.github.io/issues/3)

## 6.4 说一下你理解的模块机智

## 6.5 MVVM 原理

## 6.6 最熟悉框架的路由机制

## 6.7 状态管理

## 6.8 统计字符串中单词出现的次数

## 6.9 平时遇到的跨域问题

## 6.10 下面这段代码的输出

## 6.11 ["1","2","3"].map(parseInt)返回的是什么？

## 6.12 下面代码中“入库”的颜色是？

## 7 谈谈个人理想中的团队

## 7.1 个人成长空间

## 7.2 公司对员工的成长和进步的重视程度

## 7.3 加班情况

## 7.4 员工补贴，福利

## 7.5 绩效考核和年终奖

## 算法
## 8.1 [递归](https://github.com/sakila1012/font-end-interview-question/issues/2)

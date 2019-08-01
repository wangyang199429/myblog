#####HTML关键词
>1.**内核**：IE firdent ;Firefox:gecko
Safair:webkit
Opera:Blink
>2. <DOCTYPE>
3.Quirks **怪异模式**，srranddards: 宽高问题
4.div+css优于table:快，清晰，简洁
5.strong和em
6.**优雅降级**：复杂到简单
渐进增强：不断补充（保证基础不变的前提)
7.**多域名储存**：缓存，并发，节约cookie带宽，优化响应速度
8.**网页标准和制定**：web健康，简化开发，提高安全
9.**cookies**:4k,零时当前页；sessionStorage:5M，定期销毁
localStorage:5M,本地，永久存储
10.**src**:替换（嵌入），href：引用（下载过来）1
11.**图片格式**png jpg jpeg svg 新的Webp
12.**微格式**：语义化xhtml，额外提示
13.**缓存**js/css请求缓存：dns缓存,cdn缓存,浏览器缓存，服务器缓存
14.**图片加载优化**:图片懒加载，预加载，CSSsprite，SVGsprite，Iconfont、Base64
15.**HTML语义化**：爬虫，结构，维护，传阅
16.**SEO**：搜索抓取和排序规律，关键词分析，
17.CSS:外部，内部，内联
18.CSS：id ，类，属性，后代，自带，群组，优先级
19：**隐藏**：display:none;vidibility:hidden; height:0;
z-index:-1000;
20:**hove访问后五样式**：L-V-H-Alink,visited,hover,active）
21.快：padding,margin,width,hieght;行内：padding-left(right) margin-left(right)
22.**外边距重叠**：两正取大(负去绝对值大)，一正一负相加
23.**垂直居中**：absolute; 图片垂直居中：display:table-cell; 
text-align:center; 
24.**px与em**：px固定值，em相对值，预设px与em之间的关系
27.**reset:清除默认样式** normalize.css,但是影响优化
28.**Sass.Less**：动态css样式语言，结构清晰，便于扩展和调用，多重继承，
30.**link和@import**:link与页面同时加载，@import待页面加载完 link权重高
31.**盒子模型**：内容、内边距、外边距（一般不计入盒子实际宽度）、边框
33.**BFC**：块级格式化上下文
35.. **Doctype 的作用**？严格模式与混杂模式
36.**HTML 与 XHTML：严格**：结束，小写，&quot;属性&quot;，《&特殊编码，图徐alt,
38.3 **像素问题**:dislpay:inline -3px,Ie z-index
IE6 不支持 PNG 透明背景(用gif)
39.**WEB与w3c**：书写规则，搜索几率、加载，维护，阅览，等角度
40.**块级元素**：div p h1 h2 h3 h4 form ul ，行内a b br i span select
41.**前端3层**：html结构，css表示层，js行为层
42.**空元素**：br hr input link
43.**dsplay**:block/none/inline-block/list-item
position:fixed/relative/static/inherit
57.**可继承**:font-size/font-family/color/ul/li/dl/dd/ddt
**不可继承**：border/padding/margin/width/height





##### JS基础
>2.**类型及转换**：强制（parseInt(),parseFloat(),Number()） 
隐式（== ,!!） 
2.**字符串数组api** split():切割成数组
join(),连接成字符串
4.pop()尾删 ;shift():头删; push()尾加；Ushift()头加
5.**普通事件**：重叠覆盖
**事件绑定**：事件冒泡，事件捕获addEventLisntener
removeEventLIstener 取消绑定事件 
>6. IE 和 DOM **事件流的区别**：执行顺序，参数，有无on,this指向
>7. **IE 和标准下有哪些兼容性的写法**：事件对象 event 
Var ev = ev || window.event 
>8. **call 和 apply 的区别**
call(thisObj，Object1,Object2...) 
apply(thisObj，[argArray])
9.**b继承a的方法**Student.prototype=father;
a为father方法，b 为刚定义的一个函数对象
11.obj.appendChid()
obj.insertBefore()
obj.replaceChild()
obj.removeChild()
12.**本地对象**：array obj regecp
**内置对象**:Math 等不可实例化
**宿主对象**:l浏览器自带document.window等
13.**window.onload**原生，所有文件加载完后执行,1次
window.ready: jQuery库函数,先于前者，多次
14.==和===的不同
15.**js的同源策略**:主机名，域名和端口号的组合
16.**js:直译式脚本语言**，动态，弱类型，基于原型的语
言;js引擎-->解释器，用于客户端，兼容ECMA，又称ECMAScript
解释型脚本，向html做交互，跨平台
17.**数组的检测**
typeof Array.isArray===&quot;undefined&quot;
Object.prototype.toString.call(arg)===&quot;[object Array]&quot;
18.**写入内容到dom树**$(“#id”).val();
19.**DOM常见操作**：var dom=document.getElementById(&quot;ID&quot;)
dom.innerHTML=&quot;xxxx&quot;
dom.style.color=&quot;#000&quot;
21.**DON事件流**: 事件捕获，目标阶段，事件冒泡
22.区别undefined和is not defined
26.熟悉Array.join( &quot;&quot;)
27.连字符变驼峰:arr[i]=arr[i].charAt(0).toUpperCase()+
arr[i].substr(1,arr[i].length-1)
28.**倒排数组**:Array.reverse();降序:Array.soft(function(a,b){return b-a}
29.**输出各种日期**:var d=new Date();
d.getFullYear(); d.getMonth(); d.getDate();
30.字符串要赋值才能改变
35.array1.concat(array2);array.splice(1,1)
36.DOM的操作
``` html
<ul id=&quot;myList&quot;><li>Coffee</li><li>Tea</li></ul>
``` 
`var node=document.createElement(&quot;LI&quot;); `

`var textnode=document.createTextNode(&quot;Water&quot;); `
`node.appendChild(textnode); `
`document.getElementById(&quot;myList&quot;).appendChild(node);`
`appendChild();removeChild();replaceChild();insertBefor();`
>37.**url参数转为json**
`var urlitem=urlArray[i];`
var item=urlitem.split(&quot;=&quot;) 
`urlObject[item[0]]=item[1];`
38.**邮箱正则**:`var regMial=/^([a-zA-Z0-9_])+@([a-zA-Z0-9_])+((.[a-zA-Z0-9_]{2,3}){1,2})$/`
39.**去前后空格**
str=str.replace(/^\s+/,&apos;&apos;).replace(/\s+$/,&apos;&apos;)
41.caller返回一个对函数的引用
caller返回正在被执行的函数
45.检索当前页面中的表单元素中的所 有文本框，并将它们全部清空
``` js
for(vari=0;i<document.forms.length; i++)
{ for(var j=0;j<document.forms.elements.length; j++){ 
    if(document.forms.elements[j].type==”text”)
     document.forms.elements[j].value=”&quot;; }}
 ```
>57.**关闭窗口确认**：`if(confirm(&quot;确定退出?&quot;)){window.close}`
62.**浏览器 对象**:window document location screen history navigator; 方法：alert()
confirm() prompt() open() colse();
65.**创建函数**: function sum1(a,b){} ;var sum=function(a,b){};
var sum3 =new Function(&quot;a&quot;,&quot;
b&quot;,&quot;return a+b&quot;)
66.**继承的实现**:1.构造继承法,2.原型继承法 3.实例
继承法
67.**js创建对象**:1.var obj={}; 2.var obj=new 
Object();
3.var obj=function(){} 4.function obj(){} 
5.var obj=new Objrct();
68.cookie :空间瞎弄，不安全
71.document.write innerHTML
72.**内存泄漏**：setTimeout ;闭包，控制台日日历 循环
73.jsonp动态的创建script标签，回调函数，ajax
是页面无刷新请求
74.outerHTML
109.bind(),live(),delgate()的区别
112.**优化代码**：代码重用，避免全局变量，拆分函
数，注释
112.**readonly个disabled的区别**，都不可编辑，且
前者不可复制，前者对input(text/password)有
效；disabled对于所有的表单元素都有效
128.**GET和POST区别**:get:查询不修改，数据库安
全，传参易失真post:操作数据库，传参稳定安全
129.200：成功;302:临时换URI路径；403拒绝执
行；404请求失败；500:服务器问题；
131:**常用的http协议**：tcp/ip协议。udp协议；
134：sql漏洞(sql)，xss漏洞（js,css）
135.数组Object.prototype.toString.call(arg)===&quot;[object Array]
136:数组API：string(str); arr.join(&quot;-&quot;); arr1=arr1.concat(值1,值2，arr2,...);arr.slice(start,end); arr.splice(start,n);
arrsplice(strat,n,值1，值2,...);(删除并添加)
；arr.reserse(); arr.sort()(升序) arr.push
(值) arr.unshift(值) 
137:**事件冒泡等**
``` js
document.addEventListener('click';
, myFunction, true);
element.removeEventListener(&quot;mousemove&quot;, myFunction);
btn1Obj.attachEvent(&quot;onclick&quot;,method1);
document.getElementById(&apos;need_hide&apos;)
.onclick = function(e) {stopPropagation(e);
 ```
106:bom对象:window;document;location;navigator;screen;history;
152.alert/confirm/prompt
154.Math.ceil(Math.min(Math.max(x - 100, 0), 1));
167.伪数组：比如argument参数；getElementsByTagName;
可用Array.prototype.slice.call转正

175.完整的dom操作生成并提交input的form表单
``` html
window.onload=function(){
var form=document.createElement(&quot;form&quot;);
form.setAttribute(&quot;method&quot;,&quot;post&quot;);
form.setAttribute(&quot;action&quot;,&quot;
http://127.0.0.1/save.php&quot;);
var input=document.createElement(&quot;input&quot;);
form.appendChild(input);
document.body.appendChild(form);
input.value=&quot;cxc&quot;;
form.submit();
}
 ```
>183: 第107页不会
184.捕获异常:window.error try{}catch(){}finally{};
23.H5新表单：datalist datetime output keygen 
date month week time nimber range emailurl
5.简述ajax的过程:1,XMLHttpRequest对象2.http请求3.
设置响应http请求状态变化的函数4.发送http请求5.获取异
步调用返回的数据6.js和dom局部刷新
11.ajax优缺点：1.异步，局部，提升，节省；2.不支持返
回,暴露，seo较弱，破坏程序异常机制
16.http请求的全过程:



#### JS高级
>5.Handlebars 是一个 JavaScript 页面模板库，帮助你轻
松的构建语义化模板。
49.**如何编写高性能的Javascript?**
1.DocumentFrament 优化多次append
2.通过模板元素clone替代createElement
3.使用innerHTML赋值代替构建dom元素
4.将循环控制量保存到局部变量
5.顺序无关遍历时，用while代替for
6.将分支按照性能顺序从高到低排列
7.三目代替分支
8.不断执行的时候，优先考虑使用serInterval
51.**javascrit对象的几种创建方式：**
1.**工厂模式**；构造函数模式；原始模式；混合构造函数和原
型模式；动态原型模式；寄生构造函数模式；稳妥构造函数模式
52.**javascript继承的6种方式**
>1.原型链继承；借用构造函数继承；组合继承(原型+借用构造)；原型式继承；寄生式继承；寄生组合继承；
53.javascript原型，原型链?有什么特点？
>1. 原型对象也是普通的对象，是对象一个自带隐式的 
__proto__ 属性，原型也有可能有自 己的原型，如果一个
原型对象的原型不为 null 的话，我们就称之为原型链 
>2. 原型链是由一些用来继承和共享属性的对象组成的（有限
的）对象链
56.**Sass,less动态语言**；动态样式语言，css的预处理器；
编译成css; sass支持条件语句if{}else{} for()等 ;
less需要先引入less.js
57.apply()和call();
object.call(this,obj1,obj2,obj3)
object.apply(this,arguments)
59.**对this的理解**：
在 JavaScript 中，this 通常指向的是我们正在执行的函
数本身，或者是，指向该函数所属 的对象。 
全局的 this → 指向的是 Window ；
函数中的 this → 指向的是函数所在的对象 ；
对象中的 this → 指向其本身
64.**require.js**它不仅仅用于加载模块依赖和相关的命令，
RequireJS帮助我们写出模块化的JavaScript代码，这非常
有利于代码的可扩展性和重用性；核心是实现 js 的加载模
块，维护 js 的依赖关系，控制好文件加载的先后顺序
69.setInterval(fn1,500)重复执行；setInterval(fn1
(),500)执行一次
73.**写一个通用的事件监听函数**:(待续)
77**new操作符具体干了什么**
1、创建一个空对象，并且 this 变量引用该对象，同时还继
承了该函数的原型。 
2、属性和方法被加入到 this 引用的对象中。 
3、新创建的对象由 this 所引用，并且最后隐式的返回 this 。 var obj = {}; obj.__proto__ = Base.prototype; Base.call(obj);
79.j**s延迟加载的方式有哪些？**
defer；和async；动态吃按键dom；按需异步载入js；
97.**介绍项目经验**，合作开发，独立开发
98.**开发中遇到的困难**，如何解决的？
99.**你对前端工程师这个职位是怎么理解的？**你认为他的前景如何?
前端是最贴近用户的程序员，比后端、数据库、产品经理、运营、安全都近。 
1、实现界面交互
2、提升用户体验
3、有了 Node.js，前端可以实现服务端的一些事情 171大宝贝4. 前端是最贴近用户的程序员，前端的能力就是能让产品从 90 5.分进化到 100 分，甚至更好，
6.参与项目，快速高质量完成实现效果图，精确到 1px；
7.与团队成员，UI 设计，产品经理的沟通； 
8.做好的页面结构，页面重构和用户体验；
9.处理 hack，兼容、写出优美的代码格式；
10.针对服务器的优化、拥抱最新前端技术。

##### 其它相关的加分项：
>1. 都使用和了解过哪些编辑器?都使用和了解过哪些日常工具? 
>2. 都知道有哪些浏览器内核?开发过的项目都兼容哪些浏览器? 
>3. 瀑布流布局或者流式布局是否有了解 
>4. HTML5 都有哪些新的 API? 
>5. 都用过什么代码调试工具? 
>6. 是否有接触过或者了解过重构。
>7. 你遇到过比较难的技术问题是？你是如何解决的？

1.闭包不用了的时候，把他设置为null
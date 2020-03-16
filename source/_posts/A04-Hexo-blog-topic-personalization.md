---
title: Hexo 博客主题个性化
top: true
categories: Hexo
tags:
 - 主题个性化
 - Hexo
 - Material X
 - spfk
description: Hexo 博客主题的美化，添加一些实用功能，定制你的专属博客【持续更新】
thumbnail: https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/thumbnail/hexo.png
avatar: https://cdn.jsdelivr.net/gh/TRHX/CDN-for-itrhx.com@2.1.9/images/trhx.png
icons: [fas fa-heading]
---

本文将讲述一些博客主题的美化、实用功能的添加，本文以作者 [luuman](https://luuman.github.io/Home/H1/index.html) 的 [spfk](https://github.com/luuman/hexo-theme-spfk) 主题和作者 [xaoxuu](https://xaoxuu.com/) 的 [Material X](https://xaoxuu.com/wiki/material-x/) 主题为例，文章会不定时进行更新。文章涉及有关参考资料、教程、链接如有侵权请联系我删除！

本文在CSDN的链接：[《Hexo 博客优化之博客美化》](https://itrhx.blog.csdn.net/article/details/85420403)、[《Hexo 博客优化之实用功能添加》](https://itrhx.blog.csdn.net/article/details/85010191)，Hexo 博客专栏，从前期搭建到后期美化，帮您解决常见问题：[《Github/Coding Pages + Hexo》](https://itrhx.blog.csdn.net/category_9285510.html)，对您有帮助就点个赞吧❤️

**请注意：**不同主题可能方法有些不同，相同主题不同版本，配置方法也有所差异！

**博客美化前提条件：**有一定的前端基础，了解 HTML、CSS、JS，了解 CSS 预处理语言 Sass、Less、Stylus，搞懂 hexo 的目录结构。

**博客美化通用步骤：**选定主题，认真阅读主题文档，分析主题目录结构，了解每个文件是对应网页哪个部分的，认真阅读美化教程，美化教程本质上只为你提供核心代码和思路，具体代码要添加到哪个地方，需要你自己搞懂主题结构，添加到需要的、合适的位置！

**博客美化终极奥秘：**创作第一，体验第二，避免繁杂，简洁为上！

---

# <font color=#FF0000> 【01】添加评论系统 </font>

主流的评论系统有很多，比如：网易云跟帖、多说、友言、畅言、来必力（LiveRe）、Disqus、Valine、Gitment等等，目前网易云跟帖、多说、友言都已经关闭了，还有些可能需要翻墙，比较麻烦，百度了一下，最后还是选择了来必力评论系统

进入[来必力官网](https://livere.com)，注册一个账号（注册时可能需要翻墙）

<fancybox>
![001](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/001.jpg)  
</fancybox>

注册完毕之后，登录，进入安装页面，选择 City 免费版安装，安装之后你会得到一段代码

<fancybox>
![002](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/002.jpg)
</fancybox>

<fancybox>
![003](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/003.jpg)
</fancybox>

<fancybox>
![004](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/004.jpg)
</fancybox>

我们打开主题文件下的 <font color=#FF0000>_config.yml</font> 文件，添加如下代码：

<fancybox>
![005](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/005.png)
</fancybox>

在 <font color=#FF0000>\themes\hexo-theme-spfk\layout\\_partial\comments</font> 文件夹下新建一个 <font color=#FF0000>livere.ejs</font> 的文件，在里面填写来必力提供的代码：

``` JS
<!-- 来必力City版安装代码 -->
<div id="lv-container" data-id="city" data-uid="这里是你的uid">
	<script type="text/javascript">
		(function(d, s) {
        var j, e = d.getElementsByTagName(s)[0];
    
        if (typeof LivereTower === 'function') { return; }
    
        j = d.createElement(s);
        j.src = 'https://cdn-city.livere.com/js/embed.dist.js';
        j.async = true;
    
        e.parentNode.insertBefore(j, e);
        })(document, 'script');
	</script>
    <noscript>为正常使用来必力评论功能请激活JavaScript</noscript>
</div>
<!-- City版安装代码已完成 -->
```

打开 <font color=#FF0000>\themes\hexo-theme-spfk\layout\\_partial\article.ejs </font>文件，在适当位置添加如下红框中的代码：

<fancybox>
![006](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/006.jpg)
</fancybox>

完成以上操作之后，我们就可以使用来必力评论系统了

<fancybox>
![007](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/007.jpg)
</fancybox>

---

# <font color=#FF000> 【02】添加卡通人物 </font>

我在逛别人博客的时候偶然发现右下角居然有一个萌萌的卡通人物，还能根据你鼠标位置摇头，瞬间被吸引到了，赶紧也给自己博客添加一个吧！[点击此处](https://github.com/EYHN/hexo-helper-live2d)进入该项目地址  

输入如下命令获取 live2d ：

``` shell
$ npm install --save hexo-helper-live2d  
```

输入以下命令，下载相应的模型，将 <font color=#FF0000>packagename</font> 更换成模型名称即可，更多模型选择请[点击此处](https://github.com/xiazeyu/live2d-widget-models)，各个模型的预览请[访问原作者的博客](https://huaji8.top/post/live2d-plugin-2.0/)  

``` shell
$ npm install packagename
```

打开站点目录下的 <font color=#FF0000>_config.yml</font> 文件，添加如下代码：

``` yaml
live2d:
  enable: true
  scriptFrom: local
  model:
    use: live2d-widget-model-haruto #模型选择
  display:
    position: right  #模型位置
    width: 150       #模型宽度
    height: 300      #模型高度
  mobile:
    show: false      #是否在手机端显示
```

设置好过后我们就拥有了一个卡通人物

<fancybox>
![008](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/008.jpg)
</fancybox>

---

# <font color=#FF0000> 【03】自定义鼠标指针样式 </font>

在 <font color=#FF0000> \themes\material-x\source\less\\_base.less</font> 文件 body 样式里写入如下代码：

``` css
body {
    cursor: url(https://cdn.jsdelivr.net/gh/TRHX/CDN-for-itrhx.com@2.1.6/images/mouse.cur),auto;
    background-color: @theme_background;
    ......
    ......
}
```

鼠标指针可以用 Axialis CursorWorkshop 这个软件自己制作，不同主题具体放的文件有所不同，确保在博客主体 body 的 CSS 文件中即可，其中的鼠标指针链接可替换成自己的，首先尝试加载 https://cdn.jsdelivr.net/gh/TRHX/CDN-for-itrhx.com@2.1.6/images/mouse.cur ，如果该文件不存在或由于其他原因无效，那么 auto 会被使用，也就是自动默认效果，图片格式为.ico、.ani、.cur，建议使用.cur，如果使用.ani或者其他格式无效，原因是浏览器兼容问题，请阅读[参考文档](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Basic_User_Interface/Using_URL_values_for_the_cursor_property)或者参考以下兼容表：

| 浏览器                                                | 最低版本        | 格式                                   |
| :-----------------------------------------------: | :----------------: | :---------------------------------: |
| Internet Explorer                                 | 6.0                 | .cur / .ani                            |
| Firefox (Gecko), Windows and Linux | 1.5 (1.8)         | .cur / .png / .gif / .jpg          |
| Firefox (Gecko)                                  | 4.0 (2.0)         | .cur / .png / .gif / .jpg / .svg |
| Opera                                                 | ---                   | ---                                       |
| Safari (Webkit)                                   | 3.0 (522-523) |   .cur / .png / .gif / .jpg        |

拓展阅读：[《CSS 鼠标样式 cursor属性》](https://blog.csdn.net/ixygj197875/article/details/79338360) （By：歪脖先生的博客）

---

# <font color=#FF0000> 【04】添加鼠标点击爱心效果 </font>

在<font color=#FF0000> \themes\hexo-theme-spfk\source\js</font> 下新建文件 <font color=#FF0000>love.js</font>，在 <font color=#FF0000>love.js</font> 文件中添加以下代码：

``` JS
!function(e,t,a){function n(){c(".heart{width: 10px;height: 10px;position: fixed;background: #f00;transform: rotate(45deg);-webkit-transform: rotate(45deg);-moz-transform: rotate(45deg);}.heart:after,.heart:before{content: '';width: inherit;height: inherit;background: inherit;border-radius: 50%;-webkit-border-radius: 500%;-moz-border-radius: 50%;position: fixed;}.heart:after{top: -5px;}.heart:before{left: -5px;}"),o(),r()}function r(){for(var e=0;e<d.length;e++)d[e].alpha<=0?(t.body.removeChild(d[e].el),d.splice(e,1)):(d[e].y--,d[e].scale+=.004,d[e].alpha-=.013,d[e].el.style.cssText="left:"+d[e].x+"px;top:"+d[e].y+"px;opacity:"+d[e].alpha+";transform:scale("+d[e].scale+","+d[e].scale+") rotate(45deg);background:"+d[e].color+";z-index:99999");requestAnimationFrame(r)}function o(){var t="function"==typeof e.onclick&&e.onclick;e.onclick=function(e){t&&t(),i(e)}}function i(e){var a=t.createElement("div");a.className="heart",d.push({el:a,x:e.clientX-5,y:e.clientY-5,scale:1,alpha:1,color:s()}),t.body.appendChild(a)}function c(e){var a=t.createElement("style");a.type="text/css";try{a.appendChild(t.createTextNode(e))}catch(t){a.styleSheet.cssText=e}t.getElementsByTagName("head")[0].appendChild(a)}function s(){return"rgb("+~~(255*Math.random())+","+~~(255*Math.random())+","+~~(255*Math.random())+")"}var d=[];e.requestAnimationFrame=function(){return e.requestAnimationFrame||e.webkitRequestAnimationFrame||e.mozRequestAnimationFrame||e.oRequestAnimationFrame||e.msRequestAnimationFrame||function(e){setTimeout(e,1e3/60)}}(),n()}(window,document);
```

在 <font color=#FF0000>\themes\hexo-theme-spfk\layout\layout.ejs</font> 文件末尾添加以下代码：

``` html
<!-- 页面点击小红心 -->
<script type="text/javascript" src="/js/love.js"></script>
```

完成以上操作后，当我们点击鼠标的时候就可以看见爱心的特效了

<fancybox>
![009](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/009.jpg)
</fancybox>

---

# <font color=#FF0000> 【05】添加鼠标点击显示字体效果 </font>

在<font color=#FF0000> \themes\hexo-theme-spfk\source\js</font> 下新建文件 <font color=#FF0000>click_show_text.js</font>，在 <font color=#FF0000>click_show_text.js</font> 文件中添加以下代码：

``` JS
var a_idx = 0;
jQuery(document).ready(function($) {
    $("body").click(function(e) {
        var a = new Array
        ("富强", "民主", "文明", "和谐", "自由", "平等", "公正", "法治", "爱国", "敬业", "诚信", "友善");
        var $i = $("<span/>").text(a[a_idx]);
        a_idx = (a_idx + 1) % a.length;
        var x = e.pageX,
        y = e.pageY;
        $i.css({
            "z-index": 5,
            "top": y - 20,
            "left": x,
            "position": "absolute",
            "font-weight": "bold",
            "color": "#FF0000"
        });
        $("body").append($i);
        $i.animate({
            "top": y - 180,
            "opacity": 0
        },
      3000,
      function() {
          $i.remove();
      });
    });
    setTimeout('delay()', 2000);
});

function delay() {
    $(".buryit").removeAttr("onclick");
}
```

其中的社会主义核心价值观可以根据你自己的创意替换为其他文字

如果想要每次点击显示的文字为不同颜色，可以将其中 `color` 值进行如下更改：

```js
"color": "rgb(" + ~~(255 * Math.random()) + "," + ~~(255 * Math.random()) + "," + ~~(255 * Math.random()) + ")"
```

然后在 <font color=#FF0000>\themes\hexo-theme-spfk\layout\layout.ejs</font> 文件末尾添加以下代码：

``` html
<!--单击显示文字-->
<script type="text/javascript" src="/js/click_show_text.js"></script>
```

最终实现效果如下：

<fancybox>
![010](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/010.png)
</fancybox>

---

# <font color=#FF0000> 【06】添加鼠标点击烟花爆炸效果 </font>

在 <font color=#FF0000>\themes\material-x\source\js</font> 目录下新建一个 <font color=#FF0000>fireworks.js</font> 的文件，里面写入以下代码：

``` JS
"use strict";function updateCoords(e){pointerX=(e.clientX||e.touches[0].clientX)-canvasEl.getBoundingClientRect().left,pointerY=e.clientY||e.touches[0].clientY-canvasEl.getBoundingClientRect().top}function setParticuleDirection(e){var t=anime.random(0,360)*Math.PI/180,a=anime.random(50,180),n=[-1,1][anime.random(0,1)]*a;return{x:e.x+n*Math.cos(t),y:e.y+n*Math.sin(t)}}function createParticule(e,t){var a={};return a.x=e,a.y=t,a.color=colors[anime.random(0,colors.length-1)],a.radius=anime.random(16,32),a.endPos=setParticuleDirection(a),a.draw=function(){ctx.beginPath(),ctx.arc(a.x,a.y,a.radius,0,2*Math.PI,!0),ctx.fillStyle=a.color,ctx.fill()},a}function createCircle(e,t){var a={};return a.x=e,a.y=t,a.color="#F00",a.radius=0.1,a.alpha=0.5,a.lineWidth=6,a.draw=function(){ctx.globalAlpha=a.alpha,ctx.beginPath(),ctx.arc(a.x,a.y,a.radius,0,2*Math.PI,!0),ctx.lineWidth=a.lineWidth,ctx.strokeStyle=a.color,ctx.stroke(),ctx.globalAlpha=1},a}function renderParticule(e){for(var t=0;t<e.animatables.length;t++){e.animatables[t].target.draw()}}function animateParticules(e,t){for(var a=createCircle(e,t),n=[],i=0;i<numberOfParticules;i++){n.push(createParticule(e,t))}anime.timeline().add({targets:n,x:function(e){return e.endPos.x},y:function(e){return e.endPos.y},radius:0.1,duration:anime.random(1200,1800),easing:"easeOutExpo",update:renderParticule}).add({targets:a,radius:anime.random(80,160),lineWidth:0,alpha:{value:0,easing:"linear",duration:anime.random(600,800)},duration:anime.random(1200,1800),easing:"easeOutExpo",update:renderParticule,offset:0})}function debounce(e,t){var a;return function(){var n=this,i=arguments;clearTimeout(a),a=setTimeout(function(){e.apply(n,i)},t)}}var canvasEl=document.querySelector(".fireworks");if(canvasEl){var ctx=canvasEl.getContext("2d"),numberOfParticules=30,pointerX=0,pointerY=0,tap="mousedown",colors=["#FF1461","#18FF92","#5A87FF","#FBF38C"],setCanvasSize=debounce(function(){canvasEl.width=2*window.innerWidth,canvasEl.height=2*window.innerHeight,canvasEl.style.width=window.innerWidth+"px",canvasEl.style.height=window.innerHeight+"px",canvasEl.getContext("2d").scale(2,2)},500),render=anime({duration:1/0,update:function(){ctx.clearRect(0,0,canvasEl.width,canvasEl.height)}});document.addEventListener(tap,function(e){"sidebar"!==e.target.id&&"toggle-sidebar"!==e.target.id&&"A"!==e.target.nodeName&&"IMG"!==e.target.nodeName&&(render.play(),updateCoords(e),animateParticules(pointerX,pointerY))},!1),setCanvasSize(),window.addEventListener("resize",setCanvasSize,!1)}"use strict";function updateCoords(e){pointerX=(e.clientX||e.touches[0].clientX)-canvasEl.getBoundingClientRect().left,pointerY=e.clientY||e.touches[0].clientY-canvasEl.getBoundingClientRect().top}function setParticuleDirection(e){var t=anime.random(0,360)*Math.PI/180,a=anime.random(50,180),n=[-1,1][anime.random(0,1)]*a;return{x:e.x+n*Math.cos(t),y:e.y+n*Math.sin(t)}}function createParticule(e,t){var a={};return a.x=e,a.y=t,a.color=colors[anime.random(0,colors.length-1)],a.radius=anime.random(16,32),a.endPos=setParticuleDirection(a),a.draw=function(){ctx.beginPath(),ctx.arc(a.x,a.y,a.radius,0,2*Math.PI,!0),ctx.fillStyle=a.color,ctx.fill()},a}function createCircle(e,t){var a={};return a.x=e,a.y=t,a.color="#F00",a.radius=0.1,a.alpha=0.5,a.lineWidth=6,a.draw=function(){ctx.globalAlpha=a.alpha,ctx.beginPath(),ctx.arc(a.x,a.y,a.radius,0,2*Math.PI,!0),ctx.lineWidth=a.lineWidth,ctx.strokeStyle=a.color,ctx.stroke(),ctx.globalAlpha=1},a}function renderParticule(e){for(var t=0;t<e.animatables.length;t++){e.animatables[t].target.draw()}}function animateParticules(e,t){for(var a=createCircle(e,t),n=[],i=0;i<numberOfParticules;i++){n.push(createParticule(e,t))}anime.timeline().add({targets:n,x:function(e){return e.endPos.x},y:function(e){return e.endPos.y},radius:0.1,duration:anime.random(1200,1800),easing:"easeOutExpo",update:renderParticule}).add({targets:a,radius:anime.random(80,160),lineWidth:0,alpha:{value:0,easing:"linear",duration:anime.random(600,800)},duration:anime.random(1200,1800),easing:"easeOutExpo",update:renderParticule,offset:0})}function debounce(e,t){var a;return function(){var n=this,i=arguments;clearTimeout(a),a=setTimeout(function(){e.apply(n,i)},t)}}var canvasEl=document.querySelector(".fireworks");if(canvasEl){var ctx=canvasEl.getContext("2d"),numberOfParticules=30,pointerX=0,pointerY=0,tap="mousedown",colors=["#FF1461","#18FF92","#5A87FF","#FBF38C"],setCanvasSize=debounce(function(){canvasEl.width=2*window.innerWidth,canvasEl.height=2*window.innerHeight,canvasEl.style.width=window.innerWidth+"px",canvasEl.style.height=window.innerHeight+"px",canvasEl.getContext("2d").scale(2,2)},500),render=anime({duration:1/0,update:function(){ctx.clearRect(0,0,canvasEl.width,canvasEl.height)}});document.addEventListener(tap,function(e){"sidebar"!==e.target.id&&"toggle-sidebar"!==e.target.id&&"A"!==e.target.nodeName&&"IMG"!==e.target.nodeName&&(render.play(),updateCoords(e),animateParticules(pointerX,pointerY))},!1),setCanvasSize(),window.addEventListener("resize",setCanvasSize,!1)};
```

然后在 <font color=#FF0000>\themes\material-x\layout\layout.ejs</font> 文件中写入以下代码：

``` html
<canvas class="fireworks" style="position: fixed;left: 0;top: 0;z-index: 1; pointer-events: none;" ></canvas> 
<script type="text/javascript" src="//cdn.bootcss.com/animejs/2.2.0/anime.min.js"></script> 
<script type="text/javascript" src="/js/fireworks.js"></script>
```

最终效果：

<fancybox>
![011](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/011.gif)
</fancybox>

---

# <font color=#FF0000> 【07】添加彩色滚动变换字体 </font>

在你想要添加彩色滚动变换字体的地方写入以下代码即可，其中文字可自行更改：

``` JS
<div id="binft"></div>
  <script>
    var binft = function (r) {
      function t() {
        return b[Math.floor(Math.random() * b.length)]
      }  
      function e() {
        return String.fromCharCode(94 * Math.random() + 33)
      }
      function n(r) {
        for (var n = document.createDocumentFragment(), i = 0; r > i; i++) {
          var l = document.createElement("span");
          l.textContent = e(), l.style.color = t(), n.appendChild(l)
        }
        return n
      }
      function i() {
        var t = o[c.skillI];
        c.step ? c.step-- : (c.step = g, c.prefixP < l.length ? (c.prefixP >= 0 && (c.text += l[c.prefixP]), c.prefixP++) : "forward" === c.direction ? c.skillP < t.length ? (c.text += t[c.skillP], c.skillP++) : c.delay ? c.delay-- : (c.direction = "backward", c.delay = a) : c.skillP > 0 ? (c.text = c.text.slice(0, -1), c.skillP--) : (c.skillI = (c.skillI + 1) % o.length, c.direction = "forward")), r.textContent = c.text, r.appendChild(n(c.prefixP < l.length ? Math.min(s, s + c.prefixP) : Math.min(s, t.length - c.skillP))), setTimeout(i, d)
      }
      var l = "",
      o = ["青青陵上柏，磊磊涧中石。", "人生天地间，忽如远行客。","斗酒相娱乐，聊厚不为薄。", "驱车策驽马，游戏宛与洛。","洛中何郁郁，冠带自相索。","长衢罗夹巷，王侯多第宅。","两宫遥相望，双阙百余尺。","极宴娱心意，戚戚何所迫？"].map(function (r) {
      return r + ""
      }),
      a = 2,
      g = 1,
      s = 5,
      d = 75,
      b = ["rgb(110,64,170)", "rgb(150,61,179)", "rgb(191,60,175)", "rgb(228,65,157)", "rgb(254,75,131)", "rgb(255,94,99)", "rgb(255,120,71)", "rgb(251,150,51)", "rgb(226,183,47)", "rgb(198,214,60)", "rgb(175,240,91)", "rgb(127,246,88)", "rgb(82,246,103)", "rgb(48,239,130)", "rgb(29,223,163)", "rgb(26,199,194)", "rgb(35,171,216)", "rgb(54,140,225)", "rgb(76,110,219)", "rgb(96,84,200)"],
      c = {
        text: "",
        prefixP: -s,
        skillI: 0,
        skillP: 0,
        direction: "forward",
        delay: a,
        step: g
      };
      i()
      };
      binft(document.getElementById('binft'));
  </script>
```

最终效果：

<fancybox>
![012](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/012.gif)
</fancybox>

---

# <font color=#FF0000> 【08】添加字数统计和阅读时长 </font>

先在博客目录下执行以下命令安装 <font color=#FF0000>hexo-wordcount</font> 插件：

``` shell
$ npm i --save hexo-wordcount
```

注意：在 [Material X](https://xaoxuu.com/wiki/material-x/) 主题中，字数统计和阅读时长的功能我已提交 PR，在最新版本中，只需要安装插件后，在主题 `config.yml` 配置文件里，将 `word_count` 关键字设置为 `true` 即可，对于旧版本，可以通过以下方法实现：

以 [Material X](https://xaoxuu.com/wiki/material-x/) 主题（版本 1.2.1）为例，在 <font color=#FF0000>\themes\material-x\layout\\_meta</font> 目录下创建 <font color=#FF0000>word.ejs</font> 文件，在 <font color=#FF0000>word.ejs</font> 文件中写入以下代码：

```JS
<% if(isPostList || !isPostList){ %>
  <% if (theme.word_count && !post.no_word_count) { %>
    <div style="margin-right: 10px;">
      <span class="post-time">
        <span class="post-meta-item-icon">
          <i class="fa fa-keyboard"></i>
          <span class="post-meta-item-text">  字数统计: </span>
          <span class="post-count"><%= wordcount(post.content) %>字</span>
        </span>
      </span>
      &nbsp; | &nbsp;
      <span class="post-time">
        <span class="post-meta-item-icon">
          <i class="fa fa-hourglass-half"></i>
          <span class="post-meta-item-text">  阅读时长≈</span>
          <span class="post-count"><%= min2read(post.content) %>分</span>
        </span>
      </span>
    </div>
  <% } %>
<% } %>
```

然后在主题的配置文件 <font color=#FF0000>_config.yml</font> 找到 <font color=#FF0000>meta</font> 关键字，将 <font color=#FF0000>word</font> 填入 <font color=#FF0000>header</font> 中：

```bash
meta:
  header: [title, author, date, categories, tags, counter, word, top]
  footer: [updated, share]
```

最后在主题目录下的 <font color=#FF0000>_config.yml</font> 添加以下配置即可

```yaml
word_count: true
```

效果图：

<fancybox>
![036](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/036.png)
</fancybox>

---

同样的，以 [spfk](https://github.com/luuman/hexo-theme-spfk) 主题为例，在 <font color=#FF0000>\themes\hexo-theme-spfk\layout\\_partial\post</font> 目录下创建 <font color=#FF0000>word.ejs</font> 文件，在 <font color=#FF0000>word.ejs</font> 文件中写入以下代码：

``` JS
<div style="margin-top:10px;">
    <span class="post-time">
      <span class="post-meta-item-icon">
        <i class="fa fa-keyboard-o"></i>
        <span class="post-meta-item-text">  字数统计: </span>
        <span class="post-count"><%= wordcount(post.content) %>字</span>
      </span>
    </span>
    &nbsp; | &nbsp;
    <span class="post-time">
      <span class="post-meta-item-icon">
        <i class="fa fa-hourglass-half"></i>
        <span class="post-meta-item-text">  阅读时长: </span>
        <span class="post-count"><%= min2read(post.content) %>分</span>
      </span>
    </span>
</div>
```

然后在 <font color=#FF0000>\themes\hexo-theme-spfk\layout\\_partial\article.ejs</font> 中适当位置添加以下代码：

<fancybox>
![013](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/013.jpg)
</fancybox>

最后在主题目录下的 <font color=#FF0000>_config.yml</font> 添加以下配置

``` yaml
word_count: true
```

如果显示的位置不好，可以自行更改其位置，成功配置后的效果如下：

<fancybox>
![014](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/014.jpg)
</fancybox>

<fancybox>
![015](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/015.png)
</fancybox>

另外：要在博客底部显示所有文章的总字数，可以[点击此处](https://www.npmjs.com/package/hexo-wordcount)，根据你博客底部文件的类型选择相应的代码放在适当的位置即可，前提是要安装好 <font color=#FF0000>hexo-wordcount</font> 插件，例如我使用 [Material X](https://xaoxuu.com/wiki/material-x/) 主题，在 <font color=#FF0000>\themes\material-x\layout\\_partial</font> 目录下的 <font color=#FF0000>footer.ejs</font> 文件中添加如下代码：

``` JS
<i class="fas fa-chart-area"></i>
<span class="post-count">字数统计：<%= totalcount(site) %></span>
```

实现效果如下：

<fancybox>
![016](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/016.png)
</fancybox>

---

# <font color=#FF0000> 【09】添加背景音乐 </font>

打开网页版[网易云音乐](https://music.163.com/)，选择你准备添加的背景音乐，点击生成外链播放器，前提是要有版权，不然是无法生成外链播放器的，复制底下的HTML代码

<fancybox>
![017](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/017.jpg)
</fancybox>

<fancybox>
![018](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/018.jpg)
</fancybox>

然后将此代码放到你想要放的地方，比如放在博客的左侧，则打开 <font color=#FF0000>\themes\hexo-theme-spfk\layout\\_partial\left-col.ejs</font> 文件，将复制的HTML代码粘贴进去，再进行适当的位置设置让播放器更美观，其中 <font color=#FF0000>auto=1</font> 表示打开网页自动播放音乐，<font color=#FF0000>auto=0</font> 表示关闭自动播放音乐

<fancybox>
![019](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/019.jpg)
</fancybox>

最后效果如下：

<fancybox>
![020](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/020.jpg)
</fancybox>

这种网易云音乐外链的方式有很多局限性，因此推荐使用<font color=#FF0000>aplayer</font>，GitHub地址为：https://github.com/MoePlayer/APlayer ，参考教程：[《hexo上的aplayer应用》](https://blog.yleao.com/2018/0902/hexo%E4%B8%8A%E7%9A%84aplayer%E5%BA%94%E7%94%A8.html)

---

# <font color=#FF0000> 【10】添加网站运行时间 </font>

一个比较好的小功能，可以看见自己的博客运行多久了，时间一天天的增加，成就感也会一天天增加的
在 <font color=#FF0000>\themes\hexo-theme-spfk\layout\\_partial\footer.ejs</font> 文件下添加以下代码：

``` JS
<span id="timeDate">载入天数...</span><span id="times">载入时分秒...</span>
<script>
    var now = new Date(); 
    function createtime() { 
        var grt= new Date("08/10/2018 17:38:00");//在此处修改你的建站时间，格式：月/日/年 时:分:秒
        now.setTime(now.getTime()+250); 
        days = (now - grt ) / 1000 / 60 / 60 / 24; dnum = Math.floor(days); 
        hours = (now - grt ) / 1000 / 60 / 60 - (24 * dnum); hnum = Math.floor(hours); 
        if(String(hnum).length ==1 ){hnum = "0" + hnum;} minutes = (now - grt ) / 1000 /60 - (24 * 60 * dnum) - (60 * hnum); 
        mnum = Math.floor(minutes); if(String(mnum).length ==1 ){mnum = "0" + mnum;} 
        seconds = (now - grt ) / 1000 - (24 * 60 * 60 * dnum) - (60 * 60 * hnum) - (60 * mnum); 
        snum = Math.round(seconds); if(String(snum).length ==1 ){snum = "0" + snum;} 
        document.getElementById("timeDate").innerHTML = "本站已安全运行 "+dnum+" 天 "; 
        document.getElementById("times").innerHTML = hnum + " 小时 " + mnum + " 分 " + snum + " 秒"; 
    } 
setInterval("createtime()",250);
</script>
```

最后效果如下：

<fancybox>
![021](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/021.png)
</fancybox>

---

# <font color=#FF0000> 【11】添加百度统计 </font>

百度统计是百度推出的一款免费的专业网站流量分析工具，能够告诉用户访客是如何找到并浏览用户的网站，在网站上做了些什么，非常有趣，接下来我们把百度统计添加到自己博客当中

访问[百度统计首页](https://tongji.baidu.com)，注册一个账号后登陆，添加你的博客网站

<fancybox>
![022](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/022.jpg)
</fancybox>

接着点击代码获取，复制该代码

<fancybox>
![023](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/023.jpg)
</fancybox>

然后到目录 <font color=#FF0000>\Hexo\themes\hexo-theme-spfk\layout\\_partial</font> 下新建一个 <font color=#FF0000>baidu-analytics.ejs</font> 文件，里面粘贴你刚刚复制的代码

<fancybox>
![024](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/024.jpg)
</fancybox>

修改主题文件夹下的 <font color=#FF0000>_config.yml</font> 文件，将你的key（图中涂掉部分）填写进去：

<fancybox>
![025](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/025.jpg)
</fancybox>

所有操作完成后可以在百度统计管理页面检查代码是否安装成功，如果代码安装正确，一般20分钟后，可以查看网站分析数据

<fancybox>
![026](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/026.jpg)
</fancybox>

另外推荐：[友盟](https://web.umeng.com/main.php?c=user&a=index)，2010年4月在北京成立，安全、可靠、公正、第三方的网站流量统计分析系统

---

# <font color=#FF0000>【12】浏览器网页标题恶搞</font>

当用户访问你的博客时点击到了其他网页，我们可以恶搞一下网页标题，呼唤用户回来，首先在目录 <font color=#FF0000>\themes\material-x\source\js</font> 下新建一个 <font color=#FF0000>FunnyTitle.js</font> 文件，在里面填写如下代码：

```javascript
// 浏览器搞笑标题
var OriginTitle = document.title;
var titleTime;
document.addEventListener('visibilitychange', function () {
    if (document.hidden) {
        $('[rel="icon"]').attr('href', "/funny.ico");
        document.title = '╭(°A°`)╮ 页面崩溃啦 ~';
        clearTimeout(titleTime);
    }
    else {
        $('[rel="icon"]').attr('href', "/favicon.ico");
        document.title = '(ฅ>ω<*ฅ) 噫又好啦 ~' + OriginTitle;
        titleTime = setTimeout(function () {
            document.title = OriginTitle;
        }, 2000);
    }
});
```

其中 `funny.ico` 是用户切换到其他标签后你网站的图标，`favicon.ico` 是正常图标，然后在 <font color=#FF0000>\themes\material-x\layout\layout.ejs</font> 文件中添加如下代码：

```xml
<!--浏览器搞笑标题-->
<script type="text/javascript" src="/js/FunnyTitle.js"></script>
```

再次部署博客后就可以看见标题搞笑的效果了：

<fancybox>
![027](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/027.jpg)
</fancybox>

<fancybox>
![028](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/028.jpg)
</fancybox>

---

# <font color=#FF0000>【13】背景添加动态线条效果 </font>

在 <font color=#FF0000>\Hexo\themes\hexo-theme-spfk\layout\layout.ejs</font> 文件中添加如下代码：

``` html
<!--动态线条背景-->
<script type="text/javascript"
color="220,220,220" opacity='0.7' zIndex="-2" count="200" src="//cdn.bootcss.com/canvas-nest.js/1.0.0/canvas-nest.min.js">
</script>
```

其中：

- color：表示线条颜色，三个数字分别为(R,G,B)，默认：（0,0,0）
- opacity：表示线条透明度（0~1），默认：0.5
- count：表示线条的总数量，默认：150
- zIndex：表示背景的z-index属性，css属性用于控制所在层的位置，默认：-1

最终实现效果：

<fancybox>
![029](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/029.jpg)
</fancybox>

---

# <font color=#FF0000>【14】添加人体时钟 </font> #

无意中发现了个有趣的人体时钟 HONE HONE CLOCK，作者是个日本人，[点击此处](http://chabudai.org/blog/)访问作者博客，[点击此处](http://chabudai.org/blog/?p=59)在作者原博客上查看动态样式，[点击此处](http://chabudai.sakura.ne.jp/blogparts/honehoneclock/honehone_clock_tr.swf)查看动态大图，如果你的博客上有合适的地方，加上一个人体时钟会很有趣的

<fancybox>
![030](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/030.png)
</fancybox>

实现代码：

``` html
<!--人体时钟背景透明-->
<script charset="Shift_JIS" src="http://chabudai.sakura.ne.jp/blogparts/honehoneclock/honehone_clock_tr.js"></script>

<!--人体时钟背景白-->
<script charset="Shift_JIS" src="http://chabudai.sakura.ne.jp/blogparts/honehoneclock/honehone_clock_wh.js"></script>
```

其他网页小挂件推荐：

- http://abowman.com/ 里面有很多有趣的小挂件，可以养养鱼、龟、狗、仓鼠等各式各样的虚拟宠物，能根据你的鼠标指针位置移动，直接复制代码就可以用
- http://www.revolvermaps.com/ 它提供网站访客地理信息，可以以2D、3D等形式显示
- http://www.amazingcounters.com/ 免费网站计数器，有非常多的样式供你选择，可以设置计数器初始数值，可以设置按访问量计数，也可以按独立访问者计数
- https://www.seniverse.com/widget/get 心知天气提供基于Web的免费天气插件，可以为你的网站添加一项简洁美观的天气预报功能，并自动适配PC和手机上的浏览

---

# <font color=#FF0000>【15】添加RSS订阅 </font>

RSS订阅是站点用来和其他站点之间共享内容的一种简易方式，即Really Simple Syndication（简易信息聚合），如果不会使用，可以参见百度百科：https://baike.baidu.com/item/RSS%E8%AE%A2%E9%98%85/663114 ；首先我们安装feed插件，在本地hexo目录下右键`git bash here`，输入以下命令：

``` shell
$ npm install hexo-generator-feed
```

等待安装完成后，打开hexo目录下配置文件的`_config.yml`，在末尾添加以下配置：

``` yaml
# Extensions
## Plugins: http://hexo.io/plugins/
#RSS订阅
plugin:
- hexo-generator-feed
#Feed Atom
feed:
type: atom
path: atom.xml
limit: 20
```

随后打开主题配置文件`_config.yml`，添加以下配置：

``` yaml
rss: /atom.xml
```

至此，RSS订阅功能添加完成

---

# <font color=#FF0000>【16】添加网站雪花飘落效果 </font>

样式一和样式二分别如下：

<fancybox>
![031样式一](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/031.jpg)
</fancybox>

<fancybox>
![032样式二](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/032.jpg)
</fancybox>

实现方法：在 <font color=#FF0000>\Hexo\themes\hexo-theme-spfk\source\js</font> 目录下新建一个 <font color=#FF0000>snow.js</font> 文件，粘贴以下代码：

``` JS
/*样式一*/
(function($){
	$.fn.snow = function(options){
	var $flake = $('<div id="snowbox" />').css({'position': 'absolute','z-index':'9999', 'top': '-50px'}).html('&#10052;'),
	documentHeight 	= $(document).height(),
	documentWidth	= $(document).width(),
	defaults = {
		minSize		: 10,
		maxSize		: 20,
		newOn		: 1000,
		flakeColor	: "#AFDAEF" /* 此处可以定义雪花颜色，若要白色可以改为#FFFFFF */
	},
	options	= $.extend({}, defaults, options);
	var interval= setInterval( function(){
	var startPositionLeft = Math.random() * documentWidth - 100,
	startOpacity = 0.5 + Math.random(),
	sizeFlake = options.minSize + Math.random() * options.maxSize,
	endPositionTop = documentHeight - 200,
	endPositionLeft = startPositionLeft - 500 + Math.random() * 500,
	durationFall = documentHeight * 10 + Math.random() * 5000;
	$flake.clone().appendTo('body').css({
		left: startPositionLeft,
		opacity: startOpacity,
		'font-size': sizeFlake,
		color: options.flakeColor
	}).animate({
		top: endPositionTop,
		left: endPositionLeft,
		opacity: 0.2
	},durationFall,'linear',function(){
		$(this).remove()
	});
	}, options.newOn);
    };
})(jQuery);
$(function(){
    $.fn.snow({ 
	    minSize: 5, /* 定义雪花最小尺寸 */
	    maxSize: 50,/* 定义雪花最大尺寸 */
	    newOn: 300  /* 定义密集程度，数字越小越密集 */
    });
});
```

```JS
/*样式二*/
/* 控制下雪 */
function snowFall(snow) {
    /* 可配置属性 */
    snow = snow || {};
    this.maxFlake = snow.maxFlake || 200;   /* 最多片数 */
    this.flakeSize = snow.flakeSize || 10;  /* 雪花形状 */
    this.fallSpeed = snow.fallSpeed || 1;   /* 坠落速度 */
}
/* 兼容写法 */
requestAnimationFrame = window.requestAnimationFrame ||
    window.mozRequestAnimationFrame ||
    window.webkitRequestAnimationFrame ||
    window.msRequestAnimationFrame ||
    window.oRequestAnimationFrame ||
    function(callback) { setTimeout(callback, 1000 / 60); };

cancelAnimationFrame = window.cancelAnimationFrame ||
    window.mozCancelAnimationFrame ||
    window.webkitCancelAnimationFrame ||
    window.msCancelAnimationFrame ||
	window.oCancelAnimationFrame;
/* 开始下雪 */
snowFall.prototype.start = function(){
    /* 创建画布 */
    snowCanvas.apply(this);
    /* 创建雪花形状 */
    createFlakes.apply(this);
    /* 画雪 */
    drawSnow.apply(this)
}
/* 创建画布 */
function snowCanvas() {
    /* 添加Dom结点 */
    var snowcanvas = document.createElement("canvas");
    snowcanvas.id = "snowfall";
    snowcanvas.width = window.innerWidth;
    snowcanvas.height = document.body.clientHeight;
    snowcanvas.setAttribute("style", "position:absolute; top: 0; left: 0; z-index: 1; pointer-events: none;");
    document.getElementsByTagName("body")[0].appendChild(snowcanvas);
    this.canvas = snowcanvas;
    this.ctx = snowcanvas.getContext("2d");
    /* 窗口大小改变的处理 */
    window.onresize = function() {
        snowcanvas.width = window.innerWidth;
        /* snowcanvas.height = window.innerHeight */
    }
}
/* 雪运动对象 */
function flakeMove(canvasWidth, canvasHeight, flakeSize, fallSpeed) {
    this.x = Math.floor(Math.random() * canvasWidth);   /* x坐标 */
    this.y = Math.floor(Math.random() * canvasHeight);  /* y坐标 */
    this.size = Math.random() * flakeSize + 2;          /* 形状 */
    this.maxSize = flakeSize;                           /* 最大形状 */
    this.speed = Math.random() * 1 + fallSpeed;         /* 坠落速度 */
    this.fallSpeed = fallSpeed;                         /* 坠落速度 */
    this.velY = this.speed;                             /* Y方向速度 */
    this.velX = 0;                                      /* X方向速度 */
    this.stepSize = Math.random() / 30;                 /* 步长 */
    this.step = 0                                       /* 步数 */
}
flakeMove.prototype.update = function() {
    var x = this.x,
        y = this.y;
    /* 左右摆动(余弦) */
    this.velX *= 0.98;
    if (this.velY <= this.speed) {
        this.velY = this.speed
    }
    this.velX += Math.cos(this.step += .05) * this.stepSize;

    this.y += this.velY;
    this.x += this.velX;
    /* 飞出边界的处理 */
    if (this.x >= canvas.width || this.x <= 0 || this.y >= canvas.height || this.y <= 0) {
        this.reset(canvas.width, canvas.height)
    }
};
/* 飞出边界-放置最顶端继续坠落 */
flakeMove.prototype.reset = function(width, height) {
    this.x = Math.floor(Math.random() * width);
    this.y = 0;
    this.size = Math.random() * this.maxSize + 2;
    this.speed = Math.random() * 1 + this.fallSpeed;
    this.velY = this.speed;
    this.velX = 0;
};
// 渲染雪花-随机形状（此处可修改雪花颜色！！！）
flakeMove.prototype.render = function(ctx) {
    var snowFlake = ctx.createRadialGradient(this.x, this.y, 0, this.x, this.y, this.size);
    snowFlake.addColorStop(0, "rgba(255, 255, 255, 0.9)");  /* 此处是雪花颜色，默认是白色 */
    snowFlake.addColorStop(.5, "rgba(255, 255, 255, 0.5)"); /* 若要改为其他颜色，请自行查 */
    snowFlake.addColorStop(1, "rgba(255, 255, 255, 0)");    /* 找16进制的RGB 颜色代码。 */
    ctx.save();
    ctx.fillStyle = snowFlake;
    ctx.beginPath();
    ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
    ctx.fill();
    ctx.restore();
};
/* 创建雪花-定义形状 */
function createFlakes() {
    var maxFlake = this.maxFlake,
        flakes = this.flakes = [],
        canvas = this.canvas;
    for (var i = 0; i < maxFlake; i++) {
        flakes.push(new flakeMove(canvas.width, canvas.height, this.flakeSize, this.fallSpeed))
    }
}
/* 画雪 */
function drawSnow() {
    var maxFlake = this.maxFlake,
        flakes = this.flakes;
    ctx = this.ctx, canvas = this.canvas, that = this;
    /* 清空雪花 */
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    for (var e = 0; e < maxFlake; e++) {
        flakes[e].update();
        flakes[e].render(ctx);
    }
    /*  一帧一帧的画 */
    this.loop = requestAnimationFrame(function() {
        drawSnow.apply(that);
    });
}
/* 调用及控制方法 */
var snow = new snowFall({maxFlake:60});
snow.start();
```

然后在 <font color=#FF0000>\Hexo\themes\hexo-theme-spfk\layout\layout.ejs</font> 文件里引用即可：

``` html
<!-- 雪花特效 -->
<script type="text/javascript" src="\js\snow.js"></script>
```

如果没效果，请确认网页是否已载入JQurey，如果没有请在下雪代码之前引入JQ即可：

``` html
<script type="text/javascript" src="http://libs.baidu.com/jquery/1.8.3/jquery.js"></script>
<script type="text/javascript" src="http://libs.baidu.com/jquery/1.8.3/jquery.min.js"></script>
```

原文链接：[《分享两种圣诞节雪花特效JS代码(网站下雪效果)》](https://ihuan.me/2172.html)

---

# <font color=#FF0000>【17】添加 Fork me on GitHub 效果 </font>

效果图：

<fancybox>
![033](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/033.jpg)
</fancybox>

[点击此处](https://blog.github.com/2008-12-19-github-ribbons/)可以查看更多样式，将相应样式的代码复制到你想要放的地方就OK了，代码里的链接也要替换成你的，更多创意，比如 Follow me on CSDN ，只需要用PS改掉图片里的文字，替换掉相应链接即可

---

# <font color=#FF0000>【18】添加背景动态彩带效果 </font>

样式一是鼠标点击后彩带自动更换样式，样式二是飘动的彩带：

<fancybox>
![034](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/034.jpg)
</fancybox>

实现方法：在 <font color=#FF0000>\themes\material-x\layout\layout.ejs</font> 文件的<font color=#FF0000>body</font>前面添加如下代码：

``` html
<!-- 样式一（鼠标点击更换样式） -->
<script src="https://g.joyinshare.com/hc/ribbon.min.js" type="text/javascript"></script>
```

``` html
<!-- 样式二（飘动的彩带） -->
<script src="https://g.joyinshare.com/hc/piao.js" type="text/javascript"></script>
```

---

# <font color=#FF0000>【19】添加背景代码雨特效 </font>

新建 `DigitalRain.js`，写入以下代码：

```JS
window.onload = function(){
    //获取画布对象
    var canvas = document.getElementById("canvas");
    //获取画布的上下文
    var context =canvas.getContext("2d");
    var s = window.screen;
    var W = canvas.width = s.width;
    var H = canvas.height;
    //获取浏览器屏幕的宽度和高度
    //var W = window.innerWidth;
    //var H = window.innerHeight;
    //设置canvas的宽度和高度
    canvas.width = W;
    canvas.height = H;
    //每个文字的字体大小
    var fontSize = 12;
    //计算列
    var colunms = Math.floor(W /fontSize);	
    //记录每列文字的y轴坐标
    var drops = [];
    //给每一个文字初始化一个起始点的位置
    for(var i=0;i<colunms;i++){
        drops.push(0);
    }
    //运动的文字
    var str ="WELCOME TO WWW.ITRHX.COM";
    //4:fillText(str,x,y);原理就是去更改y的坐标位置
    //绘画的函数
    function draw(){
        context.fillStyle = "rgba(238,238,238,.08)";//遮盖层
        context.fillRect(0,0,W,H);
        //给字体设置样式
        context.font = "600 "+fontSize+"px  Georgia";
        //给字体添加颜色
        context.fillStyle = ["#33B5E5", "#0099CC", "#AA66CC", "#9933CC", "#99CC00", "#669900", "#FFBB33", "#FF8800", "#FF4444", "#CC0000"][parseInt(Math.random() * 10)];//randColor();可以rgb,hsl, 标准色，十六进制颜色
        //写入画布中
        for(var i=0;i<colunms;i++){
            var index = Math.floor(Math.random() * str.length);
            var x = i*fontSize;
            var y = drops[i] *fontSize;
            context.fillText(str[index],x,y);
            //如果要改变时间，肯定就是改变每次他的起点
            if(y >= canvas.height && Math.random() > 0.99){
                drops[i] = 0;
            }
            drops[i]++;
        }
    };
    function randColor(){//随机颜色
        var r = Math.floor(Math.random() * 256);
        var g = Math.floor(Math.random() * 256);
        var b = Math.floor(Math.random() * 256);
        return "rgb("+r+","+g+","+b+")";
    }
    draw();
    setInterval(draw,35);
};
```

在主题文件的相关css文件中（以 <font color=#FF0000>Material X 1.2.1</font> 主题为例，在<font color=#FF0000>\themes\material-x-1.2.1\source\less\\_main.less</font> 文件末尾）添加以下代码：

```css
canvas {
  position: fixed;
  right: 0px;
  bottom: 0px;
  min-width: 100%;
  min-height: 100%;
  height: auto;
  width: auto;
  z-index: -1;
}
```

然后在主题的 <font color=#FF0000>layout.ejs</font> 文件中引入即可：

```html
  <!-- 数字雨 -->
  <canvas id="canvas" width="1440" height="900" ></canvas>
  <script type="text/javascript" src="/js/DigitalRain.js"></script>
```

最终效果：

<fancybox>
![035](https://cdn.jsdelivr.net/gh/TRHX/ImageHosting/ITRHX-PIC/A04/035.jpg)
</fancybox>

代码来源：http://www.lxl8800.cn/Main/Resource

---

# <font color=#FF0000>【20】自定义一个不使用主题模板渲染的独立页面 </font>

&nbsp;&nbsp;&nbsp;&nbsp;有时候我们需要新建一个独立的页面，这个页面<font color=#FF0000>不使用主题的渲染，具有自己独立的样式</font>，可以放一些自己的作品，相册什么的，以下就介绍这种独立页面的实现方法。

<font color=#FF0000>方法一：</font>

&nbsp;&nbsp;&nbsp;&nbsp;使用 Hexo 提供的跳过渲染配置，在博客根目录的配置文件 `_config.yml` 里找到 `skip_render` 关键字，在后面添加想要跳过渲染的页面，比如我们创建 `\source\about\index.html`， 配置文件填写：`skip_render: about\**`，那么就表示 `\source\about` 里所有的文件将跳过渲染，里面的文件将会被直接复制到 public 文件夹，此时就会得到一个独立的 about 页面；官方文档：https://hexo.io/docs/configuration

<font color=#FF0000>方法二：</font>

&nbsp;&nbsp;&nbsp;&nbsp;在文章头部的 Front-matter 里添加配置 `layout: false` 来跳过渲染配置，比如我们要使 about 页面跳过渲染，创建 `\source\about\index.md`，将这个页面的相关 HTML 代码写进`.md`文件并保存，然后在 `index.md` 的头部写入：

``` yaml
---
layout: false
---

{% raw %}

这里是 HTML 代码

{% endraw %}
```

PS：Front-matter 是 `.md` 文件最上方以 --- 分隔的区域，用于指定个别文件的变量，官方文档：https://hexo.io/docs/front-matter

效果可以对比我的[博客主页](https://www.itrhx.com/)和[关于页面](https://www.itrhx.com/about/)

---

# <font color=#FF0000>【21】更改本地预览端口号</font>

hexo博客在执行 `hexo s` 进行本地预览的时候，默认端口号是4000，当该端口号被占用时会报错 `Error: listen EADDRINUSE 0.0.0.0:4000` ，此时可以关闭占用该端口的进程，也可以更换端口号，更换端口号可以通过以下两种方法实现：

方法一：在根目录的 `_config.yml` 配置文件内加上如下代码更改 `hexo s` 运行时的端口号：

```
server:
  port: 5000
  compress: true
  header: true
```

方法二：通过 `hexo server -p 5000` 命令来指定端口，这种方法只是本次执行有效

---

# <center><font color=#FF0000>未完待续......</font></center>
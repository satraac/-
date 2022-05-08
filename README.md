#         项目介绍

这是一个基于html和css的基础项目，很适合新手来练手，新手在写html时会犯的错误，也可以通过这个项目体现出来。

## 网站头部

```ht
  <div class="header wrapper">
    <h1>
        <a href="#"><img src="./images/logo.png" alt=""></a>
    </h1>
    <!--导航区域-->
    <div class="nav">
        <ul>
            <li><a href="#">首页</a></li>
            <li><a href="#">课程</a></li>
            <li><a href="#">职业规划</a></li>
        </ul>
    </div>

    <!-- 搜索区域-->
    <div class="search">
        <input type="text" placeholder="请输入关键词">
        <button></button>
    </div>
    <!-- 用户 -->
    <div class="user">
        <img src="./images/user.png" alt="">
        <span>lili</span>
    </div>

    </div>
```

一开始先来布置网站的头部，在css（外联式）中也确定了一个版心，页面内容都是跟着版心走的，

这是头部的css

```css
/* 头部 */
.header{
    height: 42px;
    /* background-color: pink; */
    /* margin-top: 30px;
    margin-bottom: 30px; */
    margin: 30px auto;
}
h1{
    float: left;
}
/* 导航 */
.nav{
    float: left;
    margin-left: 70px;
    height: 42px;
    /* background-color: green; */
}
.nav li{
 float: left;  
 margin-right: 26px; 
}
.nav li a{
    display: block;
    padding: 0  9px;
    height: 42px;
    line-height: 42px;
    /* border-bottom: 2px solid #00a4ff; */

    font-size: 18px;
    color: #050505;
}
.nav li a:hover{
    border-bottom: 2px solid #00a4ff;
}
/* 搜索 */
.search{
    float: left;
    margin-left: 59px;
    width: 412px;
    height: 40px;
    border: 1px solid #00a4ff;
}
.search input{
    float: left;
    padding-left: 20px;
    /* 左右加起来的尺寸要小于等于410 */
    width: 360px;
    height: 38px;
    border: 0;
}
/* 控制placeholder的样式 */
.search input::placeholder{
    font-size: 14px;
    color: #bfbfbf;
}

.search button{
    float: left;
    width: 50px;
    height: 40px;
    background-image: url(../images/btn.png);
    border: 0;
}
.user{
    float: right;
    margin-right: 35px;
    height: 42px;
    line-height: 42px;
    /* background-color: green; */
}
.user img{
    /* 调节图片垂直对齐方式，middle：居中 */
    vertical-align: middle;
}
```

头部分三个区域，导航，搜索，用户，导航其实不是特别难，导航的知识点是学会灵活运动**margin**和**padding**。还有就是记得把li里面的a标签转行内块或者块级标签来设置宽度和高度。记得添加**hover**。

搜索的话先创建一个父级标签来装需要的标签。在里面来个input标签调浮动，把边框去除，边框去除很重要不然会覆盖父级的边框，还有input的尺寸不能超过360px，之后还要添加一个图片，超过360px图片会放不下。创建button标签来放图片。

用户区域首先要调浮动，调与搜索区域的距离和行高，再调下图片的垂直要用这个`vertical-align: middle;`标签调。

## 轮播图

网页的轮播图也称焦点图，是用户第一眼看到的图，对用户的视觉感受起到了很大作用。

```html
<div class="banner">
        <div class="wrapper">
        <div class="left">
            <ul>
                <li><a href="#">前端开发<span>></span></a></li>
                <li><a href="#">后端开发<span>></span></a></li>
                <li><a href="#">移动开发<span>></span></a></li>
                <li><a href="#">人工智能<span>></span></a></li>
                <li><a href="#">商业预测<span>></span></a></li>
                <li><a href="#">云计算&大数据<span>></span></a></li>
                <li><a href="#">运维&从测试<span>></span></a></li>
                <li><a href="#">UI设计<span>></span></a></li>
                <li><a href="#">产品<span>></span></a></li>
            </ul>
        </div>
        <div class="right">
            <h2>我的课程表</h2>
            <div class="content">
                <dl>
                    <dt>继续学习，程序语言设计</dt> 
                    <dd>正在学习，使用对象</dd>
                </dl>
                <dl>
                    <dt>继续学习，程序语言设计</dt> 
                    <dd>正在学习，使用对象</dd>
                </dl>
                <dl>
                    <dt>继续学习，程序语言设计</dt> 
                    <dd>正在学习，使用对象</dd>
                </dl>
            </div>
            <div>
                <a href="#" class="more">全部课程</a>
            </div>
        </div>
    </div>
    </div>
```

首先定义一个div来布局，不要设置宽度，要铺满屏幕，再wrapper的css把图片放进里面去。来定义一个left和right来分别来装左边和右边的内容。

这是以下css

```css
/* 轮播图 */
.banner{
    height: 420px;
    background-color: #1c036c;
}
.banner .wrapper{
    height: 420px;
    background-image: url(../images/banner2.png);
}
.banner .left{
    float: left;
    padding: 0 20px;
    width: 190px;
    height: 420px;
    /* 行高属于控制文字的属性，能继承 */
    line-height: 44px;
    background-color: rgba(0, 0, 0, 0.3);
}
.banner .left span {
    float: right;
}
.banner .left ul a{
    font-size: 14px;
    color: #fff;
}
.banner .left a:hover{
    color: #00b4ff;
}

.banner .right{
    float: right;
    margin-top: 50px;
    width: 228px;
    height: 300px;
    background-color: #fff;
}
.banner .right h2{
    height: 48px;
    background-color: #9bceea;
    text-align: center;
    line-height: 48px;
    font-size: 18px;
    color: #fff;
}
.banner .right .content{
    padding: 0 18px;
} 
.banner .right .content dl{
    padding: 11px 0;
    border-bottom: 2px solid #e5e5e5 ;
}
.banner .right .content dt{
    font-size: 16px;
    color: #4e4e4e;
}
.banner .right .content dd{
    font-size: 14px;
    color: #4e4e4e;
}
.banner .right .more{
    display:block;
    width: 200px;
    height: 40px;
    margin: 4px auto 0;
    border: 1px solid  #00a4ff;

    font-size: 16px;
    color: #00a4ff;
    line-height: 40px;

    font-weight: 700;
    text-align: center;
}

```

left的内容是有点半透明的内容bgc的模式用rgba模式在最后一个数值添0.3其余都是0就好。其余就是调字体，不再详解。

right的内容关键是要熟练运用border和dl标签，再调下外边距和内边距就好了。还有就是如果要往a标签调内容大小记得要转换为行内块或者块级标签。

## 精品推荐

```htm
 <!-- 精品推荐 -->
    <div class="goods wrapper">
        <h2>精品推荐</h2>
        <ul>
            <li><a href="#">jquery</a></li>
            <li><a href="#">spark</a></li>
            <li><a href="#">mysql</a></li>
            <li><a href="#">javaweb</a></li>
            <li><a href="#">mysql</a></li>
            <li><a href="#">javaweb</a></li>
        </ul>
        <a href="#" class="xingqu">修改兴趣</a>
    </div>
```

如代码所示，这一部分无需赘述，

```css
/* 精品推荐 */
.goods{
    margin-top: 8px;
    padding-left: 34px;
    padding-right:26px ;
    height: 60px;
    background-color: #fff;
    box-shadow: 0px 2px 3px 0px 
	rgba(118, 118, 118, 0.2);
    line-height: 60px;
}
.goods h2{
    float: left;
    font-size: 16px;
    color: #00a4ff;
    font-weight: 400;
}
.goods ul{
    margin-left: 35px;
    float: left;
}
.goods ul li{
    float: left;
}
.goods li a{
    border-left: 1px solid #bfbfbf;
    padding: 0 35px;
    font-size: 16px;
    color: #050505;
}
.goods .xingqu{
    float: right;
    font-size: 14px;
    color: #00a4ff;
}
```

css的话，重点是加**box**-**shadow**这个标签，来达到阴影效果，还有就是记得加浮动，调间距

## 精品推荐课程

```html
<div class="box wrapper">
        <div class="title">
            <h2>精品推荐</h2>
            <a href="#">查看全部</a>
        </div>
    <div class="content">
        <ul>
            <li><a href="#">
         <img src="./images/course01.png" alt="">
         <h3>Think PHP 5.0 博客系统实战项目演练</h3>
         <p><span>高级</span>  •  1125人在学习</p>
            </a>
        </li>
        <li><a href="#">
            <img src="./images/course01.png" alt="">
            <h3>Think PHP 5.0 博客系统实战项目演练</h3>
            <p><span>高级</span>  •  1125人在学习</p>
               </a>
           </li>
           <li><a href="#">
            <img src="./images/course01.png" alt="">
            <h3>Think PHP 5.0 博客系统实战项目演练</h3>
            <p><span>高级</span>  •  1125人在学习</p>
               </a>
           </li>
           <li><a href="#">
            <img src="./images/course01.png" alt="">
            <h3>Think PHP 5.0 博客系统实战项目演练</h3>
            <p><span>高级</span>  •  1125人在学习</p>
               </a>
           </li>
           <li><a href="#">
            <img src="./images/course01.png" alt="">
            <h3>Think PHP 5.0 博客系统实战项目演练</h3>
            <p><span>高级</span>  •  1125人在学习</p>
               </a>
           </li>
           <li><a href="#">
            <img src="./images/course01.png" alt="">
            <h3>Think PHP 5.0 博客系统实战项目演练</h3>
            <p><span>高级</span>  •  1125人在学习</p>
               </a>
           </li>
           <li><a href="#">
            <img src="./images/course01.png" alt="">
            <h3>Think PHP 5.0 博客系统实战项目演练</h3>
            <p><span>高级</span>  •  1125人在学习</p>
               </a>
           </li>
           <li><a href="#">
            <img src="./images/course01.png" alt="">
            <h3>Think PHP 5.0 博客系统实战项目演练</h3>
            <p><span>高级</span>  •  1125人在学习</p>
               </a>
           </li>
           <li><a href="#">
            <img src="./images/course01.png" alt="">
            <h3>Think PHP 5.0 博客系统实战项目演练</h3>
            <p><span>高级</span>  •  1125人在学习</p>
               </a>
           </li>
           <li><a href="#">
            <img src="./images/course01.png" alt="">
            <h3>Think PHP 5.0 博客系统实战项目演练</h3>
            <p><span>高级</span>  •  1125人在学习</p>
               </a>
           </li>
        </ul>
    </div>
</div>
```

精品推荐的话，就是要用a标签装图片，h3用来当标题，p来说明，高级那还套了个span，来改高级的颜色

```css
/* 精品课程 */
.box{
    margin-top:  35px; ;
}
.box .title{
    height: 40px;
    /* background-color: pink; */
   
}
.box .title h2{
    float: left;
    font-size: 20px;
    color: #494949;
    font-weight: 400;
}
.box .title a{
    float: right;
    font-size: 12px;
    color: #a5a5a5;
    margin-right: 30px;
}
.box .content li{
    float: left;
    width: 228px;
    height: 270px;
    background-color: #fff;
    margin-right: 15px;
    margin-bottom: 15px;
}
.box .content li:nth-child(5n){
    margin-right: 0;
}
.box .content li h3{
    padding: 20px;
    font-size: 14px;
    font-weight: 400;
    color: #050505;
}
.box .content li p{
    padding: 0 23px;
    font-size: 12px;
    color: #606060;
}
.box .content li span{
    color: #ff7c2d;
}
```

间距与字体颜色，没什么好讲，同学们自己去练

## 网页结尾

```html
  <div class="footer">
        <div class="wrapper">
            <div class="left">
                <img src="./images/logo.png" alt="">
                <p>学成在线致力于普及中国最好的教育它与中国一流大学和机构合作提供在线课程。<br>
                    © 2017年XTCG Inc.保留所有权利。-沪ICP备15025210号</p>
                    <a href="#">下载app</a>
            </div>
            <div class="right">
                <dl>
                    <dt>关于学成网</dt>
                    <dd><a href="#">合作机构</a>
                    </dd>
                      <dd>
                         <a href="#">合作导师</a>
                     </dd>
                </dl>

                <dl>
                    <dt>新手指南</dt>
                    <dd><a href="#">合作机构</a>
                    </dd>

                      <dd>
                         <a href="#">合作导师</a>
                     </dd>
                </dl>

                <dl>
                    <dt>合作伙伴</dt>
                    <dd><a href="#">合作机构</a>
                    </dd>
                      <dd>
                         <a href="#">合作导师</a>
                     </dd>
                </dl>
                
            </div>
        </div>
    </div>
```

css

```css
.footer{
    margin-top: 40px;
    padding-top: 30px;
    height: 417px;
    background-color: #fff;
}
.footer .left{
    float: left;
}
.footer .left p{
    margin: 25px 0 10px;
    font-size: 12px;
    color: #666666;
}
.footer .left a{
    display: inline-block;
    width: 120px;
	height: 36px;
    font-size: 16px;
    line-height: 36px;
    text-align: center;
    color: #00a4ff;
    border: 1px solid #00a4ff;
}

.footer .right{
    float: right;
}
.footer .right dl{
    float: right;
    margin-left: 120px;
}
.footer .right dl dt{
    font-size: 16px;
    color:  #333333;
}
.footer .right dl  dd a{
    font-size: 12px;
    color: #333333;
}
```

结尾你跟着敲吧，来理解，无他，唯手熟尔

# htmlTest1
html div+css布局的简单练习：商城项目
练习笔记：
1	写网页的时候，先写div主要是通过类的方式，然后再写类的具体样式。
2	用的较多的类自己封装出来。比如浮动等等。
3	为了解决浏览器的兼容性，采用统一的d的reset.css样式，可以通过雅虎的Yui的Reset.css样式的基础上进行修改。
4	精灵图：将小的图片放一张大的图片上面，且图片的变化不大，图片之间要留空隙。在下方留下足够的大小。
5	margin的参数顺序：上面，右面，下面，左面
6 	居中：margin :0 auto;
7	搜索引擎优化：将logo加上标题<h1>将里面的字设置为...还可以加上title
	.logo_l{
	    width: 200px;
	    height: 65px;
	    background: url('../img/sprite.png') -26px 0;
	    margin:15px 0 10px 20px;
	   /* 搜索引擎优化部分*/首行缩进
	    text-indent: -1000em;
	}
	<div class="logo">
        <h1 class="logo_l fl">梅兰网</h1>
        <div class="logo_r fr" ></div>
	</div>
8	子元素的margin没有加上去，反而加到了父元素上这是：外边距的合并问题
	解决方法：
		1，加边框
    	        2,加overflow:hidden
9	在标题栏上加图标
	在比特虫的网站中，将png的图标，转换为icon的图标，16*16
	在</head>的上方写上：<link rel="shout icon" href="faciocn.ion">
10 	nav是导航栏的意思
        导航条用ul和li来做，是为了方便布局和搜索引擎优化。
        让<li>在同一行里面显示：flat:left;
11	当前的意思：current
	.nav li a.current{
		bacgrond-colcor:#;
	}
	.nav li a:hover,
	:focus {
		bacgrond-colcor:#;
	}
12	优化	
	（1）父级的盒子高度可以不用给，用里面孩子盒子的高度给撑开
	（2）将元素相同的属性放在相同的类中，尽量减少代码的冗余。
13	css2中盒子的宽度：width+border+padding
14	推荐的网站查英语词汇：爱词霸
15	a span cm b u i ins都是行内元素，没有宽度和高度
	解决方法：	display: inline-block;
				float: left;
	注：元素加了浮动，都会转换为行内块元素：inline-block

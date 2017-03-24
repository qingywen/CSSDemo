CSS多列等高布局

> CSS布局中有很多地方都需要用到多列等高，除了创建faux列的方法，我们还有兼容性更好而且更简便的方案，即利用`padding-bottom`与`margin-bottom`正负值互相抵消的做法来实现多列等高。

> 关键理论：我们给每个容器中的每个列设置比较大的底内边距和相反的负外边距，这样做的目的是消除这个高度。然而这样也会导致每个列的内容溢出容器。此时再把容器的`overflow`属性设置为"hidden"，这样最长内容列的底部就会被剪裁。因此所有列就与最长列等高。

html模块：

	<div class="wrapper">
		<div class="box">
			<h1>Andy Budd</h1>
			<p>LONDON -- A Chinese national has been injured in Wednesday's terrorist attack outside the parliament compound in London, the Chinese Embassy confirmed Thursday.</p>
		</div>
		<div class="box">
			<h1>Richard Rutter</h1>
			<p>LONDON -- A Chinese national has been injured in Wednesday's terrorist attack outside the parliament compound in London, the Chinese Embassy confirmed Thursday.The latest information on the embassy's website warns Chinese nationals in Britain to avoid going to crowded places and going out alone at night.</p>
		</div>
		<div class="box">
			<h1>Jeremy Keith</h1>
			<p>LONDON</p>
		</div>
	</div>

CSS模块：

	.wrapper {
		width: 920px;
		margin: 0 auto;
		overflow: hidden;
		border:1px solid green;
	}

	.box {
		width: 30%;
		padding-bottom: 3000px;
		margin-bottom: -3000px;
		margin-left: 2.5%;
		float: left;
		display: inline;
		background: #acacac;
	}

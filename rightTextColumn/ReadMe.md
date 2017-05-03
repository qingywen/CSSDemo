#CSS多列文本等高

> 在报纸、期刊等很多地方我们需要用到多列文本等高，此时`column-count`、 `column-width`、 `column-gap`、 `column-rule`属性就可以一展身手啦！

> 关键理论：将容器的`column-count`属性设置为你想要的列数如3列，浏览器会自动将文本分成三列显示，列的宽度默认由容器宽度均分，若不够则两列或一列。
> 
> `column-count` : 规定列数。
> 
> `column-gap` : 规定列之间的间隙。
>
> `column-rule` : 规定列之间的宽度、样式和颜色。

>  支持 ： chrom,firefox,ie(10及以上)

html模块：

	<div class="col">
		<p>
			President Xi Jinping and his Russian counterpart,Putin,Vladimir Putin,Vladimir Putin,Vladimir Putin, highlighted on Thursday the importance of ruling party exchanges amid the two sides' efforts to deepen comprehensive and strategic cooperation.President Xi Jinping and his Russian counterpart,Putin,Vladimir Putin,Vladimir Putin,Vladimir Putin, highlighted on Thursday the importance of ruling party exchanges amid the two sides' efforts to deepen comprehensive and strategic cooperation.President Xi Jinping and his Russian counterpart,Putin,Vladimir Putin,Vladimir Putin,Vladimir Putin, highlighted on Thursday the importance of ruling party exchanges amid the two sides' efforts to deepen comprehensive and strategic trhsrht sfgsasdfa.
		</p>
	</div>

CSS模块：

	.col {
		column-count: 3;
		column-width: 14em;
		column-gap: 2em;
		column-rule: 1px solid #ccc;
	}
	p {
		display: inline;
	}

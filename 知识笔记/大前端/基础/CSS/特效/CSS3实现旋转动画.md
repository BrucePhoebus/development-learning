# CSS3实现旋转动画

## 普通实现

```html
<!DOCTYPE html>
<!--
	旋转动画：360°旋转、180°旋转、90°旋转、45°旋转
-->
<html>
<head>
	<meta charset="UTF-8">
</head>
<style>
	.box {
		height: 100px;
		width: 100px;
		background-color: #c1c1c1;
	}

	.box1 {
		position: absolute;
		height: 100px;
		width: 100px;
		background-color: #c1c1c1;
		top: 50%;
		left: 50%;
		margin-top: -50px;
		margin-left: -50px;
	}

	.rotate {
		transition: All 0.4s ease-in-out;
		-webkit-transition:All 0.4s ease-in-out;
		-moz-transition:All 0.4s ease-in-out;
		-o-transition:All 0.4s ease-in-out;
	}

	.rotate360:hover {
		transform: rotate(360deg);
		-webkit-transform: rotate(360deg);
		-moz-transform: rotate(360deg);
		-o-transform: rotate(360deg);
		-ms-transform: rotate(360deg);
	}
	
	.rotate180:hover {
		transform: rotate(180deg);
		-webkit-transform: rotate(180deg);
		-moz-transform: rotate(180deg);
		-o-transform: rotate(180deg);
		-ms-transform: rotate(180deg);
	}
	
	.rotate90:hover {
		transform: rotate(90deg);
		-webkit-transform: rotate(90deg);
		-moz-transform: rotate(90deg);
		-o-transform: rotate(90deg);
		-ms-transform: rotate(90deg);
	}
	
	.rotate45:hover {
		transform: rotate(45deg);
		-webkit-transform: rotate(45deg);
		-moz-transform: rotate(45deg);
		-o-transform: rotate(45deg);
		-ms-transform: rotate(45deg);
	}
</style>
<body>
<div class="rotate rotate360 box1">旋转360°</div>
<div class="rotate rotate360 box">旋转360°</div>
<div class="rotate rotate180 box">旋转180°</div>
<div class="rotate rotate90 box">旋转90°</div>
<div class="rotate rotate45 box">旋转45°</div>
</body>
</html>
```

## 动态语法改造

#### SCSS改造

```css
/* 执行动画以及执行时间设定 */
@mixin dz($time:0.25s){
    -webkit-transition: all $time ease-in-out;
    -moz-transition: all $time ease-in-out;
    -o-transition: all $time ease-in-out;
    -ms-transition: all $time ease-in-out;
    transition: all $time ease-in-out;
}

/* 旋转动画调用 */
@mixin xz($deg:360){
    transform:rotate($deg+deg);
    -webkit-transform:rotate($deg+deg);
    -moz-transform:rotate($deg+deg);
    -o-transform:rotate($deg+deg);
    -ms-transform:rotate($deg+deg);
}
```

**使用方式**

```css
#rotateDiv {
    @include dz();
    &:hover {
        @include xz(90);
    }
}
```

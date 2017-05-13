# CSS 关于图片的属性（未完待续、、、）

## 图片太大的响应式

```
img{
	max-width: 100%;
	//高度一般可不加
	max-height: 100%;
}

```

相对于父元素。将最大宽高撑到100%，不要超过父元素，来达到图片缩放的目的。



## 背景图片的响应式

```css
background: url(地址);
background-repeat: norepeat;
background-position: center center;

background-size: cover;
```


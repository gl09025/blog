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


## 文本溢出点
```css
.content p{
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
```

#### 指定几行溢出点



http://www.zhangxinxu.com/wordpress/2009/09/%E5%85%B3%E4%BA%8E%E6%96%87%E5%AD%97%E5%86%85%E5%AE%B9%E6%BA%A2%E5%87%BA%E7%94%A8%E7%82%B9%E7%82%B9%E7%82%B9-%E7%9C%81%E7%95%A5%E5%8F%B7%E8%A1%A8%E7%A4%BA/

http://www.daqianduan.com/6179.html


#### 父子margin合并

父元素加padding

```HTML
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>JS Bin</title>
</head>
<style>
.a {
  width: 100px;
  height: 100px;
  background: red;
  margin: 10px;
  padding: 0.1px;
}

.b {

  width: 90px;
  height: 90px;
  background: blue;
  margin: 20px;
}
</style>
<body>
<div class="a">
  <div class="b"></div>
</div>
  
</body>
</html>
```
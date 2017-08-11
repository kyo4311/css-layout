# 居中布局

```
布局要求：内容宽度1000px,左右两个块为100px宽高，靠近内容浮动
```

html
```html
<div class="box"></div>
<div class="left">Left</div>
<div class="right">Right</div>
```

```css
.box{
    width: 1000px;
    height: 2000px;
    margin: auto;
    background: #eee;
}
.left,.right{
    width: 100px;
    height: 100px;
    background: #222;
    position: fixed;
    color: #fff;
    text-align: center;
    line-height: 100px;
}
.left{
    bottom: 100px;
    left: 50%;
    margin-left: -600px;
}

.right{
    bottom: 100px;
    left: 50%;
    margin-left: 500px;
}
```
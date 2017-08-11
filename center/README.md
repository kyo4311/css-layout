# 居中布局

```
布局要求：外层大小不定，内层大小不定，同层居中
```

html
```html
<div class="box table">
    <div class="child"></div>
</div>
```

通用css
```css
.box{
    width: 200px;
    height: 200px;
    border: 1px solid #ccc;
}

.child{
    width: 100px;
    height: 100px;
    background: yellow;
    text-align: center;
    line-height: 100px;
}

```

### 使用flex布局

```css
.flex{
    display: flex;
    justify-content: center;
    align-items: center;
}
```


### 使用定位布局
```css
.position{
    position: relative;
}

.position .child{
    position: absolute;
    left: 50%;
    top: 50%;
    /*margin:-50px 0 0 -50px; */
    transform: translate(-50%, -50%);    /* 50%为自身尺寸的一半 */
}
```


### 使用表格布局
```css
.table{
    display: table-cell;
    text-align: center;
    vertical-align: middle;
}
.table .child{
    display: inline-block;
}
```


### 使用网格布局

```css
.grid{
    display: grid;
    justify-content: center;
    align-items: center;
}
```
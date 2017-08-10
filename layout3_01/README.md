# 已知高度，三列布局

```
布局要求：高度固定为100px, 左边固定300px，右边200px 中间自适应。
```

根据以上要求，我们先写一些通用的css样式
```css
body{margin: 0; padding: 0;}
.left{background:#ccc; width: 300px;}
.center{background: yellow;}
.right{background:#eee; width: 200px;}
.layout, .left, .right, .center{height: 100px;}
.layout{margin-bottom: 20px;}
```

### 使用float布局

css
```css
.layout.float .left{float: left;}
.layout.float .right{float: right;}
```
html
```html
<section class="layout float">
    <article>
        <div class="left">left</div>
        <div class="right">right</div>
        <div class="center">使用float布局</div>
    </article>
</section>
```

### 使用flex布局
css
```css
.layout.flex article{ display: flex; }
.layout.flex .center{flex-grow: 1;}
```

html
```html
<section class="layout flex">
    <article>
        <div class="left">left</div>
        <div class="center">使用flex布局</div>
        <div class="right">right</div>
    </article>
</section>
```

### 使用定位布局

css
```css
.layout.absolute article{ position: relative; }
.layout.absolute .left{position: absolute; left: 0; top: 0;}
.layout.absolute .right{position: absolute; right: 0; top: 0;}
.layout.absolute .center{position: absolute; left: 300px; right: 200px; top: 0;}
```

html
```html
<section class="layout absolute">
    <article>
        <div class="left">left</div>
        <div class="center">使用定位布局</div>
        <div class="right">right</div>
    </article>
</section>
```

### 使用表格布局

css
```css
.layout.table article{display: table; width: 100%;}
.layout.table .left{display: table-cell;}
.layout.table .cetner{display: table-cell;}
.layout.table .right{display: table-cell;}
```

html
```html
<section class="layout table">
    <article>
        <div class="left">left</div>
        <div class="center">使用表格布局</div>
        <div class="right">right</div>
    </article>
</section>
```

### 使用网格布局

css
```css
.layout.grid article{display: grid; grid-template-columns:300px auto 200px;}
```

html
```html
<section class="layout grid">
    <article>
        <div class="left">left</div>
        <div class="center">使用网格布局</div>
        <div class="right">right</div>
    </article>
</section>
```
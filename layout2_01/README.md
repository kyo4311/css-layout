# 已知高度两列布局

```
布局要求：高度固定为100px,左边固定300px，右边自适应。
```

根据以上要求，我们先写一些通用的css样式
```css
*{margin: 0; padding: 0;}
.left{background:#ccc; width: 300px;}
.right{background:#eee;}
.layout, .left, .right{height: 100px;}
.layout{margin-bottom: 20px;}
```

### 使用float布局

css
```css
.layout.float .left{float: left;}
```
html
```html
<section class="layout float">
    <article>
        <div class="left"></div>
        <div class="right">使用float布局</div>
    </article>
</section>
```

### 使用flex布局
css
```css
.layout.flex article{ display: flex; }
.layout.flex .right{flex-grow: 1;}
```

html
```html
<section class="layout flex">
    <article>
        <div class="left"></div>
        <div class="right">使用flex布局</div>
    </article>
</section>
```

### 使用定位布局

css
```css
.layout.absolute article{ position: relative; }
.layout.absolute .left{position: absolute; left: 0; top: 0;}
.layout.absolute .right{position: absolute; left: 300px; right: 0; top: 0;}
```

html
```html
<section class="layout absolute">
    <article>
        <div class="left"></div>
        <div class="right">使用定位布局</div>
    </article>
</section>
```

### 使用表格布局

css
```css
.layout.table article{display: table; width: 100%;}
.layout.table .left{display: table-cell;}
.layout.table .right{display: table-cell;}
```

html
```html
<section class="layout table">
    <article>
        <div class="left"></div>
        <div class="right">使用表格布局</div>
    </article>
</section>
```

### 使用网格布局

css
```css
.layout.grid article{display: grid; grid-template-columns:300px auto;}
```

html
```html
<section class="layout grid">
    <article>
        <div class="left"></div>
        <div class="right">使用网格布局</div>
    </article>
</section>
```
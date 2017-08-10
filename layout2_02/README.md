# 未知高度，两列布局

```
布局要求：左边固定300px，右边自适应，高度自适应
```

根据以上要求，我们先写一些通用的css样式
```css
body{margin: 0; padding: 0;}
.left{background:#ccc; width: 300px;}
.right{background:#eee;}
.layout{margin-bottom: 20px;}
```

### 使用float布局

css
```css
.layout.float article{overflow: hidden;}
.layout.float .left{float: left;}
.layout.float .right{overflow: hidden;}
.layout.float .left,
.layout.float .right{padding-bottom: 9999px; margin-bottom: -9999px;}
```
html
```html
<section class="layout float">
    <article>
        <div class="left">left</div>
        <div class="right">
            <p>float布局</p>
            <p>float布局</p>
            <p>float布局</p>
            <p>float布局</p>
        </div>
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
        <div class="left">
            <p>flex布局</p>
            <p>flex布局</p>
            <p>flex布局</p>
            <p>flex布局</p>
        </div>
        <div class="right">
            <p>flex布局</p>
        </div>
    </article>
</section>
```

### 使用定位布局

css
```css
.layout.absolute article{ position: relative;}
.layout.absolute .left{position: absolute; left: 0; top: 0; bottom: 0; }
.layout.absolute .right{padding: 0 0 0 300px; overflow: hidden;  }
```

html
```html
<section class="layout table">
    <article>
        <div class="left">left</div>
        <div class="right">
            <p>table布局</p>
            <p>table布局</p>
            <p>table布局</p>
            <p>table布局</p>
        </div>
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
<section class="layout absolute">
    <article>
        <div class="left">left</div>
        <div class="right">
            <p>定位布局</p>
            <p>定位布局</p>
            <p>定位布局</p>
        </div>
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
        <div class="left">
            left
        </div>
        <div class="right">
            <p>网格布局</p>
            <p>网格布局</p>
            <p>网格布局</p>
            <p>网格布局</p>
            <p>网格布局</p>
        </div>
    </article>
</section>
```
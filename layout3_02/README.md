# 未知高度，三列布局

```
布局要求：左边固定300px，右边200px 中间自适应。高度自适应
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
.layout.float .left{float: left;  }
.layout.float .right{float: right;}
.layout.float .center{overflow: hidden;}
.layout.float .left,
.layout.float .center,
.layout.float .right{padding-bottom: 9999px;margin-bottom: -9999px;}
.layout.float article{overflow: hidden;}
```
html
```html
<section class="layout float">
    <article>
        <div class="left">left</div>
        <div class="right">right</div>
        <div class="center">
            <p>使用float布局</p>
            <p>使用float布局</p>
            <p>使用float布局</p>
            <p>使用float布局</p>
            <p>使用float布局</p>
        </div>
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
        <div class="center">
            <p>使用flex布局</p>
            <p>使用flex布局</p>
            <p>使用flex布局</p>
            <p>使用flex布局</p>
            <p>使用flex布局</p>
        </div>
        <div class="right">right</div>
    </article>
</section>
```

### 使用定位布局

css
```css
.layout.absolute article{ position: relative; }
.layout.absolute .left{position: absolute; left: 0; top: 0; bottom: 0;}
.layout.absolute .right{position: absolute; right: 0; top: 0; bottom: 0;}
.layout.absolute .center{padding: 0 200px 0 300px; overflow: hidden;}
```

html
```html
<section class="layout absolute">
        <article>
            <div class="center">
                <p>使用定位布局</p>
                <p>使用定位布局</p>
                <p>使用定位布局</p>
                <p>使用定位布局</p>
                <p>使用定位布局</p>
            </div>
               <div class="left">left</div>
            <div class="right">right</div>
        </article>
    </section>
```

### 使用表格布局

css
```css
.layout.table article{display: table; width: 100%;}
.layout.table .left{display: table-cell;}
.layout.table .center{display: table-cell;}
.layout.table .right{display: table-cell;}
```

html
```html
<section class="layout table">
    <article>
        <div class="left">left</div>
        <div class="center">
            <p>使用表格布局</p>
            <p>使用表格布局</p>
            <p>使用表格布局</p>
            <p>使用表格布局</p>
        </div>
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
        <div class="center">
            <p>使用网格布局</p>
            <p>使用网格布局</p>
            <p>使用网格布局</p>
            <p>使用网格布局</p>
            <p>使用网格布局</p>
        </div>
        <div class="right">right</div>
    </article>
</section>
```
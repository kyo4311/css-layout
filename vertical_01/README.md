# 上方固定，下方自适应

```
布局要求：上方固定100px,下方自适应。
```

### 使用flex布局
css
```css
html,body{height: 100%;}
body{margin: 0; padding: 0;}
section{display: flex;flex-direction: column;height: 100%;}
header{height: 100px;background: #eee;}
article{background: yellow; overflow: hidden; flex-grow: 1;}
```

html
```html
<section>
    <header>我是顶部</header>
    <article>
        <h1>上方固定，下方自适应</h1>
        <p>布局要求：上方固定100px,下方自适应。</p>
    </article>
</section>
```

### 使用定位布局

css
```css
body{margin: 0; padding: 0;}
header{height: 100px;background: #eee;}
article{background: yellow; position: absolute;top: 100px; bottom: 0; right: 0; left: 0;}
```

html
```html
<section>
    <header>我是顶部</header>
    <article>
        <h1>上方固定，下方自适应</h1>
        <p>布局要求：上方固定100px,下方自适应。</p>
    </article>
</section>
```

### 使用表格布局

css
```css
html,body{height: 100%;}
body{margin: 0; padding: 0;}
section{display: table; width: 100%; height: 100%;}
header{height: 100px;background: #eee; display: table-row;}
article{background: yellow;display: table-row; }
```

html
```html
<section>
    <header>我是顶部</header>
    <article>
        <h1>上方固定，下方自适应</h1>
        <p>布局要求：上方固定100px,下方自适应。</p>
    </article>
</section>
```

### 使用网格布局

css
```css
html,body{height: 100%;}
body{margin: 0; padding: 0;}
section{width: 100%; height: 100%; display: grid; grid-template-rows:100px auto;}
header{background: #eee;}
article{background: yellow; }
```

html
```html
<section>
    <header>我是顶部</header>
    <article>
        <h1>上方固定，下方自适应</h1>
        <p>布局要求：上方固定100px,下方自适应。</p>
    </article>
</section>
```
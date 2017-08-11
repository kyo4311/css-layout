# 上下固定，中间自适应

```
布局要求：上下固定100px,中间自适应。
```


```html
<section>
    <header>我是顶部</header>
    <article>
        <h1>上下固定，中间自适应</h1>
        <p>布局要求：上下固定100px,中间自适应。</p>
    </article>
    <footer>底部</footer>
</section>
```

### 使用flex布局
css
```css
html,body{height: 100%;}
body{margin: 0; padding: 0;}
section{display: flex;flex-direction: column;height: 100%;}
header{height: 100px;background: #eee;}
footer{height: 100px; background: #eee;}
article{background: yellow; overflow: hidden; flex-grow: 1;}
```



### 使用定位布局

css
```css
body{margin: 0; padding: 0;}
header{height: 100px;background: #eee;}
article{background: yellow; position: absolute;top: 100px; bottom: 100px; right: 0; left: 0;}
footer{height: 100px;background: #eee; position: absolute; bottom: 0;right: 0; left: 0;}
```



### 使用表格布局

css
```css
html,body{height: 100%;}
body{margin: 0; padding: 0;}
section{display: table; width: 100%; height: 100%;}
header,footer{height: 100px;background: #eee; display: table-row;}
article{background: yellow;display: table-row; }
```


### 使用网格布局

css
```css
html,body{height: 100%;}
body{margin: 0; padding: 0;}
section{width: 100%; height: 100%; display: grid; grid-template-rows:100px auto 100px;}
header{background: #eee;}
article{background: yellow;}
```
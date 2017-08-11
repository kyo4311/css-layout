# 居中布局

```
布局要求：4列瀑布流
```

html
```html
<section>
    <article class="n1">1</article>
    <article class="n2">2</article>
    <article class="n3">3</article>
    <article class="n4">4</article>
    <article class="n5">5</article>
    <article class="n6">6</article>
    <article class="n7">8</article>
    <article class="n8">9</article>
    <article class="n9">10</article>
    <article class="n10">11</article>
</section>
```

```css
section{
    column-count: 4;
    column-gap: 20px;
}
article{
    background: #eee;
    margin-bottom: 20px;
    break-inside: avoid;
}
.n1{height: 280px;}
.n2{height: 450px;}
.n3{height: 360px;}
.n4{height: 520px;}
.n5{height: 410px;}
.n6{height: 260px;}
.n7{height: 760px;}
.n8{height: 310px;}
.n9{height: 270px;}
.n10{height: 160px;}
```
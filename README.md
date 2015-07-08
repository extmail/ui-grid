# ui-grid [![spm version](http://spmjs.io/badge/rui-grid)](http://spmjs.io/package/rui-grid)

---

CSS 栅格系统，将一行内容分为 12个格子，通过配置 class 名的方式控制布局。


```html
<div class="ui-grid" >
    <div class="ui-grid-row">
        <div class="ui-grid-3">3</div>
        <div class="ui-grid-3">3</div>
        <div class="ui-grid-3">3</div>
        <div class="ui-grid-3">3</div>
    </div>
</div>
```
## ui-grid
包裹元素

## ui-grid-row
行元素

行元素内的 ui-grid{number} 相加要正好等于12

## ui-grid-[1~12]
单元格元素

`.ui-grid` 默认百分比布局

设置 `width` 则是定宽布局，浏览器宽度小于定宽出现横向滚动条

单元格元素之间没有间隙，需要通过内容的内外边距调节

**尽量不要增加 `.ui-grid-[1~12]` 的样式**

```css
// 不要这样做
.page .ui-grid-1{
    border:1px solid blue;
}
```
```html
<div class="ui-grid" >
    <div class="ui-grid-row">
        <div class="ui-grid-1">1</div>
        <div class="ui-grid-11">11</div>
    </div>
</div>
```

```css
// 推荐这样做
.content{
    border:1px solid blue;
}
```
```html
<div class="ui-grid" >
    <div class="ui-grid-row">
        <div class="ui-grid-1">
            <div class="content">1</div>
        </div>
        <div class="ui-grid-11">11</div>
    </div>
</div>
```

## 示例

---

<style>
.ui-grid-row {
    color:white;
    text-shadow:0px 1px 3px #666;
    margin-bottom: 10px;
}
.ui-grid-1{
    background-color: #CCCCFF
}
.ui-grid-2{
    background-color: #99CCCC
}
.ui-grid-3{
    background-color: #CCFFFF
}
.ui-grid-4{
    background-color: #6699CC
}
.ui-grid-5{
    background-color: #3399CC
}
.ui-grid-6{
    background-color: #336699
}
.ui-grid-6+.ui-grid-6 {
    background-color: #99CCFF
}
.ui-grid-7{
    background-color: #99CCFF
}
.ui-grid-8{
    background-color: #99CCCC
}
.ui-grid-9{
    background-color: #6699CC
}
.ui-grid-10{
    background-color: #99CCFF
}
.ui-grid-11{
    background-color: #0099CC
}
.ui-grid-12{
    background-color: #99CCFF
}

</style>
<link rel="stylesheet" href="ui-grid.css">

### 6:6
````html
<div class="ui-grid">
    <div class="ui-grid-row">
        <div class="ui-grid-6">
            ui-grid-6    
        </div>
        <div class="ui-grid-6">
            ui-grid-6
        </div>
    </div>
</div>
````

### 3:9
````html
<div class="ui-grid">
    <div class="ui-grid-row">
        <div class="ui-grid-3">
            ui-grid-3    
        </div>
        <div class="ui-grid-9">
            ui-grid-9
        </div>
    </div>
</div>
````

### 2:10
````html
<div class="ui-grid">
    <div class="ui-grid-row">
        <div class="ui-grid-2">
            ui-grid-2
        </div>
        <div class="ui-grid-10">
            ui-grid-10
        </div>
    </div>
</div>
````

### 固定宽度

````css
.fixed {
    width:400px;
}
````
````html
<div class="ui-grid fixed">
    <div class="ui-grid-row">
        <div class="ui-grid-3">
            ui-grid-3
        </div>
        <div class="ui-grid-4">
            ui-grid-4
        </div>
        <div class="ui-grid-5">
            ui-grid-5
        </div>
    </div>
</div>
````
### 更多情况
````html
<div class="ui-grid">
    <div class="ui-grid-row">
        <div class="ui-grid-11">
            ui-grid-11
        </div>
        <div class="ui-grid-1">
            ui-grid-1
        </div>
    </div>
    <div class="ui-grid-row">
        <div class="ui-grid-2">
            ui-grid-2
        </div>
        <div class="ui-grid-2">
            ui-grid-2
        </div>
        <div class="ui-grid-2">
            ui-grid-2
        </div>
        <div class="ui-grid-2">
            ui-grid-2
        </div>
        <div class="ui-grid-2">
            ui-grid-2
        </div>
        <div class="ui-grid-2">
            ui-grid-2
        </div>
    </div>
    <div class="ui-grid-row">
        <div class="ui-grid-3">
            ui-grid-3
        </div>
        <div class="ui-grid-3">
            ui-grid-3
        </div>
        <div class="ui-grid-3">
            ui-grid-3
        </div>
        <div class="ui-grid-3">
            ui-grid-3
        </div>
    </div>
    <div class="ui-grid-row">
        <div class="ui-grid-2">
            ui-grid-2
        </div>
        <div class="ui-grid-8">
            ui-grid-8
        </div>
        <div class="ui-grid-2">
            ui-grid-2
        </div>
    </div>
    <div class="ui-grid-row">
        <div class="ui-grid-7">
            ui-grid-7
        </div>
        <div class="ui-grid-5">
            ui-grid-5
        </div>
    </div>
</div>
````
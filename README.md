# rainui-grid [![spm version](http://spmjs.io/badge/rainui-grid)](http://spmjs.io/package/rainui-grid)

---


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

## ui-grid-[1~12]
单元格元素

`.ui-grid` 默认百分比布局

设置 `width` 则是定宽布局，浏览器宽度小于定宽出现横向滚动条

单元格元素之间没有间隙，需要通过内容的内外边距调节

**不要修改 `.ui-grid-[1~2]` 各种元素的 `margin` 和 `padding`**


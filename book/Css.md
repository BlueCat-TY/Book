# Css 整理笔记  
### 1. placeholder 占位符样式（文本框提示语）
```css
::-webkit-input-placeholder {
    color: #fff;
}
```
### 2. 元素水平垂直居中
```css
div {

    display:-webkit-flex;
    -webkit-align-items: center;
    -webkit-justify-content: center;

    display: flex;
    align-items: center; /*垂直居中*/
    justify-content: center; /*水平居中*/
}
```
### 3. 强制文本大小写
```css
div {
    /*uppercase（大写）| lowercase（小写）| capitalize（正常）*/
    text-transform: uppercase; 
}
```

### 4. 去掉浏览器默认样式
```css
div {
    -webkit-appearance: none;
}
```

### 5. 文字间距
```css
div {
    word-spacing: 10px;
}
```

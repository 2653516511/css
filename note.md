### 1. 
不论在什么浏览器中，图片默认都会向下撑大3像素。
解决办法：display: block
### 2. 高度塌陷的问题
1) 给父元素加overflow:hidden。但是会产生一个问题就是：如果有定位position的时候，就会影响效果了；
2) 给最后加一个空的元素，设clear: both。
3) 给父元素添加样式：
```js
.parent:after {
    content: '';        //content设为空
    display: block;     //设为block
    clear: both;
}
```

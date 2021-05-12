# 本地预览方法

```
yarn global add http-server
hs . -c-1
```
# 总结

* 使用dome，即使用div标签来画线效率会很慢，网页会有卡顿感！（x分支使用的是div画点，不推荐用来画线）
* 应该使用canvas来进行优化！（y分支使用canvas，解决了性能问题，可以用来流畅地画线啦）
* 要实现鼠标点击画线，则要先设定一个参照变量（参考y1分支）
* 部署到手机端时，要先考虑到识别是否是触屏
  ```html
  let isTouchDevice = 'ontouchstart' in document.documentElement;
        console.log(isTouchDevice)
  ```
  然后在用 canvas.xxx = () =>{} 来进行坐标点抓取。实现的效果可以用 console.log() 大法来进行打印检验！
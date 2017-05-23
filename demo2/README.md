1. 在THREE.js中定义一个点

> 在三维空间中，一个点是由x，y，z 所组成的，在THREE.js中，点可以在右手坐标系中表示：
```
THREE.Vector3 = function (x, y, z) {
  this.x = x || 0
  this.y = y || 0
  this.z = z || 0
}
```

上述代码即是在THREE下定义啦一个类

当需要一个点时，可以通过`new` 的形式来定义。

`var point1 = new THREE.Vector3()`

```
var material = new THREE.LineBasicMaterial({
  // params in here...
})
```
LineBasicMaterial 用来定义饿一种材质外观
其中可传入参数 @params
Color: 线条颜色，默认0xfff
LineWidth: 线条宽度,默认1px
Linecap: 线条两端外观，默认圆角端点
Linejoin: 两个线条连接处外观，默认"round"， 表示圆角
VertColors: 定义材质是否使用顶点颜色
Fog: 定义材质颜色时候受全局雾效的影响
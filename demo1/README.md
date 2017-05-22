## THREE.js


三大组件

1. 场景 (scene)

```
var scene = new THREE.Scene()
```

2. 相机 (camera)

```
var camera = new THREE.PerspectiveCamera(75, window.innerWidth/window.innerHeight, .1, 1000);
```

3. 渲染器 (renderer)

```
var renderer = new THREE.WebGLRenderer()
render.setSize(window.innerWidth, window.innerHeight)
document.body.appendChild(renderer, domElement)
```

4. 三大组件创建完成后，要做的就是酱物体添加到场景中

```
var geometry = new THREE.CubeGeometery(1,1,1)
var material = new THREE.MeshBasicMaterial({color: 0x00ff00});
var cube = new THREE.Mesh(geometry, material)
scene.add(cube)
```


5. 渲染

```
renderer.render(sceen, camera,renderTarget, forceClear)
```

其中包含了四个参数：
> scene 前面所创建的场景
> camera 前面创建的相机
> renderTarget 渲染目标， 默认渲染到前面定义的render变量中
> 每次绘制之前都会将画布的内容清除，既是自动清除标志为false

6. 渲染循环

渲染有两种方式： 实时渲染和离线渲染


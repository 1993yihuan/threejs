#threejs三维场景
>测试threejs相关API，同时里面也有一些好玩demo

##以下是关于一些文件夹的说明

###一些主要的东西
构建一个三维场景，主要需要[基本组件、材质、光源、动画、相机]元素，采用右手定则，通过改变这些元素的相对位置，构建一个完整可操作交互的web应用

###01
#####初始化场景
```javascript
var scene = new THREE.Scene();
```
#####当创建场景组件时，可以定义它的坐标位置
```javascript
cube.position.x = -4;
cube.position.y = 3;
cube.position.z = 0;
```
#####定义场景中光源信息
```javascript
new THREE.SpotLight(0xffffff);
```
#####定义相机的位置
```javascript
camera.position.x = -30;
camera.position.y = 40;
camera.position.z = 30;
```
#####定义相机的聚焦点
```javascript
camera.lookAt(scene.position);
```
#####添加这些元素
```javascript
scene.add(spotLight);
```
#####加入动画，不断更新视图
```javascript
requestAnimationFrame(render);
```
#####最后一步
```javascript
renderer.render(scene, camera);
```

###02
#####加入了stats监控
```javascript
var stats = initStats();
```
#####通过Gui进行测试数据交互
```javascript
gui.add(controls, 'addCube');
```
![](http://olcrntw9l.bkt.clouddn.com/QQ20170214-154408.gif)

*Yihuan He email:yihuan1993@qq.com*

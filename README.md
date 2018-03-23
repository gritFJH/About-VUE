#### 项目创建流程

1. 安装vue-cli的脚手架
```
npm install -g vue-cli
```
2. 初始化一个项目
```
vue init webpack my-project
```
3. 进入项目
```
cd my-project
```
4. 安装依赖
```
npm install
```
5. 启动项目
```
npm run dev
```

#### 项目目录结构
1. index.html ：        根目录的html文件，项目根视图
2. .postpackage.json：  postcss配置文件
3. gitignore ：         git上传时的忽略文件
4. editorconfig文件：   配置文件（语法编码等，不需要了解）
5. babellrc ：          针对ES6
6. static目录：          静态文件目录（服务器启动之后，可以直接访问到该目录下的内容，通常会把自己写的一些比如json文件和一些文档都可以放在这个目录中）
7. src：                源码文件
8. config：             配置文件（主要针对于开发上的一些服务器上的配置，比如开发环境的配置、生产环境的配置）
9. build：               包含服务器和webpack配置文件(webpack.base.conf.js基本配置文件，webpack.dev.conf.js开发环境下的配置文件，webpack.prod.conf.js生产环境下的配置文件)
```<template></template>是一组承载容器，不会被渲染成组件```
#### vue基本指令
0. {{}}：其中只能存在单行语句，并且不能作用在html属性上
1. v-html：渲染文本，能够解析html标签
2. v-text: 渲染文本，不能解析html标签，会将包裹的html标签原样输出
3. v-bind：绑定，被绑定的属性会变成动态的，可以动态改变绑定的class和ID，哪个属性是活的，就用v-bind进行绑定。绑定之后属性等号后面就是对象传入，所有属性都可以用v-bind进行绑定。
4. v-bind 的简写为“:”
#### 条件渲染
1. v-if
2. v-else
3. v-else-if
4. v-show :结果与v-if相同，但是没有了v-else
5. v-if和v-show的区别：v-if是真正的条件渲染，因为他会确保在切换过程中条件快内的时间监听器和子组件适当的被销毁和重建。v-if也是惰性的，如果在初始渲染时条件为假，则什么也不做，一直到条件第一次变为真时，才会开始渲染条件块。相比之下，v-show就简单的多，不过初识条件是什么，元素总会被渲染，并且只是简单的基于CSS进行切换。一般来说，v-if有更高的切换开销，而v-show又更高的初识渲染开销，因此，如果需要非常频繁的切换，则使用v-show较好，如果在运行时条件很少切换，则使用v-if比较好。

#### 列表渲染(开发过程中使用非常频繁)
1. v-for：用于数组渲染，对象也可以进行渲染，但是尽量不要使用对象进行渲染，尽量对象只用作读取
每个列表都要添加key，否则会有警告。
#### 事件监听
1. v-on指令监听dom事件，并在触发时运行一些JavaScript代码。
2. methods
3. 事件参数
4. 修饰符
#### 创建一个新的组件
1. components目录中新建一个文件，命名为.vue结尾
2. 组成：
  1. 一个组件必须包含三个部分：视图（template）、js部分（<script></script>）、样式（<style></style>）


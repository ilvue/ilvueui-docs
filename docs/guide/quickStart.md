# 快速上手

## 使用之前
高效的开发，离不开基础工程的搭建。在开始使用 ilvue UI 之前，有必要先了解以下基础知识，我们也假设您已经写过 Vue，并掌握了下面的内容。

* [Vue组件](https://cn.vuejs.org/v2/guide/components.html)
* [单文件组件](https://cn.vuejs.org/v2/guide/single-file-components.html)

以下概念贯穿 ilvue UI 前后，建议开发者花点时间来了解。

* props 传递数据
* slot 内容分发
* events $emit @click 事件
## 使用 Vue CLI 3 
> 我们为最新的 Vue CLI 3 提供了相应的 ilvue UI（ilvue）插件，如果你正在用 Vue CLI 3，可以直接在插件中搜索 ilvue，安装插件来使用。

## 引入 ilvue
一般在 webpack 入口页面 main.js 中如下配置：

::: tip
```js
import Vue from 'vue';
import VueRouter from 'vue-router';
import Routers from './router.js';
import ilvue from 'ilvue';
import 'ilvue/dist/styles/ilvue.css';

Vue.use(VueRouter);
Vue.use(ilvue);

// The routing configuration
const RouterConfig = {
    routes: Routers
};
const router = new VueRouter(RouterConfig);

new Vue({
    el: '#app',
    router: router,
    render: h => h(App)
});
```
::: 

<baseComponent-star></baseComponent-star>
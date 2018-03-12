# test-spa

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```

For detailed explanation on how things work, consult the [docs for vue-loader](http://vuejs.github.io/vue-loader).

# Html5 History 模式
vue-router 默认使用hash模式--使用URL的hash来模拟一个完整的URL，#号在浏览器中的URL中是一个锚点，在当前页改变#号的参数的时候，页面回调转到锚点所在的位置，通过JAVASCRIPT我们可以获取到#号后的参数：
```
location.hash //获取url hash
location.hash = '#list' //改变URL hash
```

有这个#号，虽然不影响功能，但看起来有点奇怪，处女座一定不能忍。要消除这个＃号，需要做一下配置，修改 router/index.js：
```
export default new Router({
  mode: 'history',
  routes: routes
})
```

# SPA 
Single Page App ，本质上只是一个页面，然后再使用各种前端技术模拟出各个页面，与后台的通信全部通过API，上面的例子就是。
## 好处
- 网页端，APP，公众号等都有使用同一套API
- 路由在前端，后端只需要服务 API，大大减轻了服务器的压力
- 前后端可以做到彻底分离，方便开发
- 速度快，用户体验好，比肩原生应用

## 缺点
SEO问题

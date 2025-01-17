# al-keep-alive

## Features

一个升级版的keep-alive，可以用来缓存所有的页面，包括复用页面。
可以在实现一些多标签页面，打开标签需要缓存页面数据的场景下使用

## install

```js
npm install al-keep-alive
```

## 使用

```js
import { alKeepAlive } from 'al-keep-alive'
export default {
  components: { alKeepAlive }
}
```

```html
// 复用页面跳转的时候，路由不会跳转，所以需要在路由组件上添加一个key
// 需要把组件的路由地址传入到include数组中
// 例：localhost:8080/home/page3/3
// 需要把/home/page3/3作为参数push进include数组
<al-keep-alive :include="includePageNames">
  <router-view :key="$route.fullPath" />
</al-keep-alive>
```
[github](https://github.com/blunlove/al-keep-alive)
欢迎大家star，提供issues。

## License

LicenseFinder is released under the [MIT](http://www.opensource.org/licenses/mit-license) License.

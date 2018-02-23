# vue-scroller-liu

基于vux分割的scroll

## Install

```
npm install vue-scroller-liu

```
## API

name|type|description
:-----:|:-----:|:-----:
value|object|对象，上拉或者下拉的状态双向绑定，使用 v-model 绑定，pulldownStatus 及 pullupStatus
height|string|容器高度，默认为整个viewport高度，注意，该属性接受的是 String 类型，比如 200px，如果你希望scroller自动计算除去头部尾部高度，请这样设置让组件自动计算，如height="-40"
lock-x|Boolean|锁定X方向
lock-y|Boolean|锁定Y方向
scrollbar-x|Boolean|是否显示横向滚动条
scrollbarY|Boolean|是否显示垂直方向滚动条
bounce|Boolean|是否显示边缘回弹效果
use-pulldown|Boolean|是否使用下拉组件
use-pullup|Boolean|是否使用上拉组件
pulldown-config|Object|下拉组件配置
pullup-config|Object|上拉组件配置
scroll-bottom-offset|Number|在距离底部多长距离时触发事件 on-scroll-bottom

## Event

name|description
:-----:|:-----:
on-scroll|容器滚动时触发，参数为top和left位置
on-scroll-bottom|滚动到底部时触发，注意事件会触发多次，如果你需要进行数据获取，记得设置一个状态值
on-pulldown-loading|用户触发下拉刷新状态，监听该事件以获取加载新数据
on-pullup-loading|用户触发上拉加载状态，监听该事件以加载新数据

## Method

name|description
:-----:|:-----:
reset|在内容变化(v-for渲染，异步数据加载)后需要调用，用以重新渲染，避免新加的内容无法上拉看到，一般在 $nextTick 回调里调用。easing 可以为 ease-in, ease-in-out, ease, bezier(n, n, n, n)
donePullup|设置上拉刷新操作完成，在数据加载后执行
disablePullup|禁用上拉刷新，在没有更多数据时执行
enablePullup|启用上拉刷新插件
donePulldown|设置下拉刷新操作完成，在数据加载后执行

## Actions

请确保在你的数据更新后进行reset操作

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

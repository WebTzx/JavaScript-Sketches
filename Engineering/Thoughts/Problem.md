> 对问题解决最彻底的效果就是忘记问题的存在

### 早期的问题

- 原生 js 方法太少，某些常规操作太繁琐，处理兼容问题很麻烦
  + 解决方案：封装
  + 业界标杆：underscore, lodash, jQuery
- 常用组件不希望重复造轮子，希望直接拷贝使用。某些组件具有一定复杂度，自己实现成本太高
  + 解决方案：封装
  + 业界标杆：iScroll.js, bootstrap, datepicker.jquery.js
  

> 组件化一直是前端开发的重要主题，早期的组件化关注点在于插件，随着现代框架的出现以及随之而来的开发模式的变化，组件化已经成为一整套方法论，组件的内涵也愈加丰富，不再仅仅是引用 + 配置，还增加了生命周期、父子关系、插槽、高阶组件、递归组件等概念

- 如何避免重复加载资源？
  + 缓存

- 如何解决文件更新后，覆盖之前的缓存？
  + 文件名 MD5

- 单个文件越来越大，维护成本越来越高
  + 解决方案：拆分，模块化

- 模块化带来的结果是文件越来越多，文件间的依赖关系也越来越复杂，急需一种能够解决依赖关系、同时控制文件加载时机的方案
  + 解决方案：模块加载器
  + 业界标杆：require.js, sea.js

- 模块化后，文件数量骤增，如何减少 HTTP 请求？
  + 解决方案：打包（bundler）
  + 业界标杆：webpack

- 所有文件达成一个包后引入的新问题：公共模块、异步模块如何抽离、拆分打包？
  + 解决方案：commonChunkPlugin、code split

- 自动拆分 chunk 后出现的新问题：改一个文件导致所有文件 md5 戳改变，从而导致缓存失效？
  + [解决方案](https://zhuanlan.zhihu.com/p/32361759?group_id=929010116083572736)

- 前端的常规任务如雪碧图、文件压缩、文件合并等，全靠手工操作太麻烦
  + 解决方案：自动化构建
  + 业界标杆：gulp, grunt, webpack, fis3

- 上线操作属于重复性的手工操作，太麻烦
  + 解决方案：自动化持续集成
  + Travis CI、Circle CI、Jenkins、AppVeyor

- 开发调试过程中，不希望每次都刷新页面，特别是某些情况下刷新会导致所有状态复原，必须从头来过
  + 解决方案：HMR（热更新，hot module replacement）

- JavaScript 缺少类型，可靠性不足
  + Microsoft: TypeScript
  + Facebook: Flow


### 设计稿自动生成可用页面


### JavaScript 编译目标语言？


### 前端产品的特征

- 持续维护，快速迭代
- 多类终端，多种版本
- 即时加载，依赖网络


### 软件领域一切工程问题的根源：代码量大了怎么办？


### 自动化构建和资源管理要实现的终极目标：每个状态只加载需要的资源

- 没有一个资源、一行代码是没用的、冗余的（资源总量最小化）
- 没有一个资源、一行代码是重复加载的（加载量最小化）
- 不同的设备加载匹配的资源（响应式加载）

前端监控
# HTML踩的坑

想了想, 还是将HTML模块抽一个出来, 的确也有一些平时会遇到稀奇古怪的东西值得一说.

### [common] 常见的coding规范

每个标签都有自己的语义. 我们coding时应该编写语义化的代码. 这样做的好处是什么呢? 它可以让方便小蜘蛛(搜索引擎)的抓取收录我们的信息.

1. `h1 ~ h6`表示标题. 不准滥用`h1`标签
2. ul标签多用于无序列表
3. ol标签用于有序列表
4. dl标签用于定义数据列表
5. Em, strong表示强调等

### [common] script标签

`<script>`加上了`type="ecmascript-6"`后, eslint部分规则会失效.

### [link]视频首屏最先加载方法

像爱奇艺、优酷等以视频为核心的网站, 用户点击进来无非就像看视频. 那么我们在进行性能优化的时候, 理所当然的先让用户看到想要看到的东西(视频). 因此我们会把视频依赖文件等最先加载.

![YouTube在网络慢的场景](./image/youtube.png)

但是浏览器会默认的将多媒体资源放在最后面加载, 无论你的标签在文档中放的多靠前. 这时的解决方案就是将`<script>`(初始化视频的js文件)改用为`<link>`标签引用.
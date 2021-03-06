# D0001

## 【HTML】 页面导入样式时，使用link和@import有什么区别

都是为了加载CSS文件

|对比|link|@import|
|----|----|-------|
|从属关系|XHTML标签|是 CSS 提供的语法规则，只有导入样式表的作用|
|加载顺序|link引用的CSS会同时被加载|@import引用的CSS会等到页面全部被下载完再被加载|
|兼容性|无|CSS2.1 +|
|DOM控制|可以使用JS控制DOM去改变样式|无法控制|

### 关于加载顺序

![代码](./assets/code_link_and_import.jpg)
![实际加载结果](./assets/result_link_and_import.jpg)

> 结论：如果同一级，按书写的先后顺序依次加载，如果import写在CSS文件中则会等到页面资源全部下载完再加载

---

## 【CSS】圣杯布局和双飞翼布局的理解和区别，并用代码实现

> 两者均为三栏布局的优化解决方案，因为浏览器渲染引擎在构建和渲染渲染树是异步的（谁先构建好谁先显示），那么将重点展示的部分提前即可优先渲染。

|-|优点|缺点|
|-|----|---|
|圣杯|结构简单，无多余 dom 层|中间部分宽度小于左侧时布局混乱(最小宽度2xL+R)|
|双飞翼|支持各种宽高变化，通用性强|dom 结构多余层，增加渲染树生成的计算量|

* [圣杯](./holy-grail.html)
* [双飞翼](./flying-wing.html)

## 参考

* [In Search of the Holy Grail](https://alistapart.com/article/holygrail/)

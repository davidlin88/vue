# vue学习笔记
* `v-model`：双向数据绑定[ 实例](https://davidlin88.github.io/vue/语法/v-model.html)
* `v-bind`：绑定属性，`v-bind:class:active`可简写为`:class:active`[ 实例](https:davidlin88.github.io/vue/语法/v-bind.html)
* `v-if`：为true时显示，为false不显示，html代码也不显示[ 实例](https:davidlin88.github.io/vue/语法/v-if.html)
* `v-show`：作用几乎同`v-if`[ 实例](https:davidlin88.github.io/vue/语法/v-show.html)
> **`v-if`与`v-show`区别：**<br/>
  在切换 v-if 块时，Vue有一个局部编译/卸载过程，因为 v-if 之中的模板也可能包括数据绑定或子组件。v-if 是真实的条件渲染，因为它会确保条件块在切换当中合适地销毁与重建条件块内的事件监听器和子组件。<br>
v-if 也是惰性的：如果在初始渲染时条件为假，则什么也不做——在条件第一次变为真时才开始局部编译（编译会被缓存起来）。
 相比之下，v-show 简单得多——元素始终被编译并保留，只是简单地基于 CSS 切换。<br>
 一般来说，v-if 有更高的切换消耗而 v-show 有更高的初始渲染消耗。<br>因此，**如果需要频繁切换 v-show 较好，如果在运行时条件不大可能改变 v-if 较好。**
 * `v-for`：循环，可用于绑定数组的数据来渲染一个项目列表，获得循环项的索引：`v-for="(person,index) in perople"`，默认第一个参数为循环项，第二参数为索引值[ 实例](https:davidlin88.github.io/vue/语法/v-for.html)
 * `v-on`：绑定事件监听器，`@click="greet"`可简写为`@click="greet"`;在`methods`对象中定义方法，方法中的`this`指向所在的Vue实例或组件(https:davidlin88.github.io/vue/v-on.html)
 * `component`：组件[ 实例](https:davidlin88.github.io/vue/语法/compenoent.html)
 
 

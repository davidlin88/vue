# vue学习笔记
### v-model
双向数据绑定 [实例](https://davidlin88.github.io/vue/语法/v-model.html)
### v-if/v-else-if/v-else
* `v-if`:判断vue.js的变量的值,执行页面渲染逻辑,即为true时显示(渲染)，为false不显示，html代码也不显示
* `v-else-if`/`v-else`:用在`v-if`后,作用类似 [实例](https://davidlin88.github.io/vue/语法/v-if.html)
### v-show
显示效果与`v-if`类似,但其会显示html代码 [实例](https://davidlin88.github.io/vue/语法/v-show.html)
> **`v-if`与`v-show`区别：**<br/>
  在切换 v-if 块时，Vue有一个局部编译/卸载过程，因为 v-if 之中的模板也可能包括数据绑定或子组件。v-if 是真实的条件渲染，因为它会确保条件块在切换当中合适地销毁与重建条件块内的事件监听器和子组件。<br>
v-if 也是惰性的：如果在初始渲染时条件为假，则什么也不做——在条件第一次变为真时才开始局部编译（编译会被缓存起来）。
相比之下，v-show 简单得多——元素始终被编译并保留，只是简单地基于 CSS 切换。<br>
一般来说，v-if 有更高的切换消耗而 v-show 有更高的初始渲染消耗。<br>因此，**如果需要频繁切换 v-show 较好，如果在运行时条件不大可能改变 v-if 较好。**
### v-for
* 1.循环数组元素，可用于绑定数组的数据来渲染一个项目列表，并获得循环项的索引：`v-for="(person,index) in perople"`，默认第一个参数为循环项，第二参数为索引值 [实例1](https:davidlin88.github.io/vue/语法/v-for.html)
* 2.循环JS对象,把对象内容显示到页面上 [实例2](https:davidlin88.github.io/vue/语法/v-for2.html)
### v-on
绑定事件监听器，`v-on:click="greet"`可简写为`@click="greet"`;在`methods`对象中定义方法，方法中的`this`指向所在的Vue实例或组件 [实例](https:davidlin88.github.io/vue/v-on.html)
### $component
组件 [实例](https://davidlin88.github.io/vue/语法/$compenoent.html)
### $computed
* 计算属性，处理元数据，便于二次利用 [实例](https:davidlin88.github.io/vue/语法/$computed.html)
* `getter`:计算属性`component`的值,`get:function(){...}`表示如何得到这个值
* `setter`:同样是计算属性的值,`set:function(value){...}`表示如何用这个变量的值给其他变量赋值
### $watch
监听属性,用于监听变量的变化,然后进行相应的处理 [实例](https:davidlin88.github.io/vue/语法/$watch.html)
[实例](https://davidlin88.github.io/vue/语法/getter和setter.html)
### v-bind
* 绑定属性，可简写为`:`,如`:class={active:isActive}`,其中,当`isActive`位`true`时,给元素绑定active的类 [实例1](https:davidlin88.github.io/vue/语法/v-bind.html);
* 绑定对象:`:class=myClass`,`myClass`是vue实例中data属性的一个子属性(对象) [实例2](https://davidlin88.github.io/vue/语法/v-bind2.html)

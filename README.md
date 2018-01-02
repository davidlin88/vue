# vue学习笔记
### v-text
* 简写为`{{}}`,写作`v-text="msg"`的形式时,会将标签内所有内容替换为Vue实例中的msg数据 [实例](https://davidlin88.github.io/vue/语法/v-text.html)
### v-html
* 写作`v-html="msg"`的形式时,会将标签内所有内容替换为Vue实例中的msg数据,并以html形式解析 [实例](https://davidlin88.github.io/vue/语法/v-html.html)
### v-model
* 为表单控件元素创建双向数据绑定,与输入框绑定: [实例1](https://davidlin88.github.io/vue/语法/v-model.html)
* 与表单复选框绑定: [实例2](https://davidlin88.github.io/vue/语法/v-model2.html)
* 与表单单选框绑定: [实例3](https://davidlin88.github.io/vue/语法/v-model3.html)
* 与下拉菜单绑定: [实例4](https://davidlin88.github.io/vue/语法/v-model4.html)
#### 表单修饰符
* 使用格式:`v-model.lazy="dataName"`[实例](https:davidlin88.github.io/vue/语法/表单修饰符.html)
* `.lazy`:用户输入内容时不做绑定数据的更新处理,失去焦点后才处理
* `.number`:将用户的内容转为数值类型,输入非数值时返回NaN
* `.trim`:自动去掉用户输入内容两端的空格
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
### v-bind
* 绑定属性，可简写为`:`,如`:class={active:isActive}`,其中,当`isActive`位`true`时,给元素绑定active的类 [实例1](https:davidlin88.github.io/vue/语法/v-bind.html);
* 绑定对象:`:class=myClass`,`myClass`是vue实例中data属性的一个子属性(对象) [实例2](https://davidlin88.github.io/vue/语法/v-bind2.html)
### 组件(component)
* 组件注册要写在vue声明之前 [全局组件实例](https://davidlin88.github.io/vue/语法/$component.html)
* 注册局部组件 [局部组件实例](https://davidlin88.github.io/vue/语法/$component2.html)
* 制作表格组件时,不能直接添加新组件,要用`is`属性在原表格的基础上替换属性,如写`<tr is="my-row1"></tr>`而非`<my-row1></my-row1>`,否则组件无法添加进原表格内,而是在其上方 [表格组件实例](https://davidlin88.github.io/vue/语法/$component3.html)
* 组件可在`data`属性内添加数据函数,而非数据属性 [添加数据函数的组件实例](https://davidlin88.github.io/vue/语法/$component4.html)
* 组件可在`computed`属性接收参数;`props`定义组件能接收的参数 [接收参数的组件实例](https://davidlin88.github.io/vue/语法/$component5.html)
* 组件可传递变量数据,即与vue实例中的数据绑定 [传递变量数据的组件实例](https://davidlin88.github.io/vue/语法/$component6.html)
* 组件参数可在`props`中添加验证语法,为组件中接收到的变量进行逻辑验证 [组件的验证语法实例](https://davidlin88.github.io/vue/语法/$component7.html) **疑问:为什么name前加:会报错?**
* 组件的事件传递 [实例](https://davidlin88.github.io/vue/语法/$component8.html)
* `slot`是父组件与自组件的通讯方式,可以将父组件的内容显示到子组件中 [实例](https://davidlin88.github.io/vue/语法/$component9.html)
* 子组件中可通过为多个`slot`命名,来接受父组件不同内容的数据 [实例](https://davidlin88.github.io/vue/语法/$component10.html)
### $computed
* 计算属性，处理元数据，便于二次利用 [实例1](https:davidlin88.github.io/vue/语法/$computed.html)
* `getter`:计算属性`component`的值,`get:function(){...}`表示如何得到这个值
* `setter`:同样是计算属性的值,`set:function(value){...}`表示如何用这个变量的值给其他变量赋值
[实例2](https://davidlin88.github.io/vue/语法/getter和setter.html)
### $watch
* 监听属性,用于监听变量的变化,然后进行相应的处理 [实例](https://davidlin88.github.io/vue/语法/$watch.html)

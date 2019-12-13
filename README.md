# vue
## 前端框架Vue学习

参考书籍：
《Vue.js实战》梁灏 编著

# 一.基础篇

    在3.3.1使用计算属性缓存 computed
             在3.3.2也可以使用 method定义相应的方法来计算
               二者有什么区别：
                   计算属性是基于它的依赖缓存的。
                   当一个计算属性所依赖的数据发生变化时，它才会重新取值，所以只要text不改变，计算属性也就不更新

###   4.v-bind绑定class 以及 style

    v-bind:class 也可以书写成 :class
    v-bind:style 也可以书写成 :style
        在实际业务中，:style的数组语法并不常用，因为往往可以写在一个对象里面；而较为常用的应当是计算属性
###    5.内置指令

``` 
    5.1基本指令
        5.1.1 v-clock
            在一般情况下，v-clock是一个解决初始化慢导致页面闪动的最佳实践、
            
        5.1.2 v-once
            v-once也是一个不需要表达式的指令，作用是定义它的元素或组件只渲染一次，包括元素或组件的所有的子节点。
         首次渲染后，不再随数据的变化重新渲染
         
    5.2条件渲染指令
        5.2.1 v-if v-else-if v-else
        
        5.2.2 v-show
        
        5.2.3 v-if与v-show的选择
            v-if与v-show具有类似的功能，不过v-if才是真正的条件渲染，它会根据表达式适当地的销毁或重建元素及绑定的事件或重建元素及绑定的事件或子组件，若表达式初始值为false，则一开始元素/组件并不会渲染，只有当条件第一次变成真时，才会编译。
            而v-show只是简单的CSS属性切换，无论条件真与否，都会被编译。相比之下，v-if更适合条件不经常改变的场景，因为它切换开销相对较大，而v-show适用于频繁切换条件。
            
    5.3列表渲染指令v-for
        5.3.1 基本用法
        	基本使用: 
        		item in items  
        		items 为参数 ，item为循环后的别名
        		
        	index索引的使用
        		（item，index） in items
        		 index即为索引
        		 
        	使用template渲染
        		例子：
        		  <template v-for="book in books">
                  	<li>书名:{{book.name}}-作者:{{book.author}}</li>
                   </template>
                   
            对象属性渲染
            
            键名+索引
            	{{index}}  {{key}}  {{value}}
            	
            迭代整数
            	n in 10
         
         5.3.2 数组更新
         	Vue包含了一组观察数组变异的方法，使用它们改变数组也会触发视图更新
         		push()
         		pop()
         		shift()
         		unshift()
         		splice()
         		sort()
         		reverse()
         		
         	使用以上方法会改变被这些方法调用的原始数组，有些方法不会改变原数组
         		filter()
         		concat()
         		slice()
         	它们返回的是一个新数组，在使用这些非变异方法时，可以使用新数组代替原数组
         		
         		
```
# vue
前端框架Vue学习
1.基础篇
    在3.3.1使用计算属性缓存 computed
             在3.3.2也可以使用 method定义相应的方法来计算
               二者有什么区别：
                   计算属性是基于它的依赖缓存的。
                   当一个计算属性所依赖的数据发生变化时，它才会重新取值，所以只要text不改变，计算属性也就不更新
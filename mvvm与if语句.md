# mvvm与if语句



if是编程中常用的过程式语法。react/elm自然不必说，每次界面都是计算出来的。在界面渲染中，vue也提供这种语法。但mve不提供。



组件与模型一一对应，if语句就不对应了，怎么办呢？



1. 用组件的display:none隐藏组件，作为一种条件渲染。可能面临多个界面元素、元素的多个属性都要加上判断语句，因为它们仍然会每次执行到。
2. 局部使用ArrayModel或mve内置的mvc模式的ifChildren等。缺点是每次变化都会重新渲染。亦不能使用类似vue的keep-alive。
3. 界面元素可以精细成DOM元素类型保持状态。
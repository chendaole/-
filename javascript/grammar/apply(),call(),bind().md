# apply() call() bind()

## 函数基础
>函数式编程： 由于JavaScript支持匿名函数，因此可以将函数作为对象来使用， 所以JavaScript不仅支持过程式编程（面向对象也是过程式编程的一种），还支持函数式编程。

## 上下文
>函数的每次调用都会拥有一个特殊值——本次调用的上下文（context）——这就是this关键字的值。 如果函数挂载在一个对象上，作为对象的一个属性，就称它为对象的方法。当通过这个对象来调用函数时，该对象就是此次调用的上下文， 也就是该函数的this的值。

*1.在js中不允许直接对this进行赋值，this作为一个关键词处理。*
*2.函数作为对象处理*

>每一个函数都包含一个prototype属性，这个属性是指向一个对象的引用，这个对象称作“原型对象”。 每一个函数都包含不同的原型对象。当将函数用作构造函数的时候，新创建的对象会从原型对象上继承属性。

**apply与call相似,只是在传递的参数的结构不相同**

`const f = function(arg1, arg2) {

}

f.call(obj, arg1, arg2);
f.apply(obj, [arg1, arg2]);`

####改变f的上下文，使f中的this指向obj。

**bind 拷贝**

·
const  f = function() {
  console.log('this is new function');
}

f.bind();
·

####bind作用实质上是将f()函数作为模板进行拷贝一份



###[References](http://wwsun.github.io/posts/javascript-functions.html)

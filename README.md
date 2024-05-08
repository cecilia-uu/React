# Virtual DOM versus Actual DOM
1. 本质是Object类型的对象（一般对象）
2. 虚拟DOM比较“轻”，真实DOM比较“重”。因为虚拟DOM是REACT内部在用，无需真实DOM上那么多的属性。
3. 虚拟DOM最终会被React转换成真实DOM，呈现在页面上。
# React JSX
1. 全称是：JavaScript XML
2. react定义的一种类似于XML的JS扩展语法：JS + XML
3. XML早期用于存储和传输数据，但比JSON复杂
```c
<student>
    <name>Tom</name>
    <age>19</age>
</student>
```

JSON:
- store information: simple
"{"name":"Tom","age":19}"
- revert: simple
    - pase: json->js
    - stringfy: js->json
4. 本质是React.createElement(component, props, ...children)方法的语法糖
5. 作用：用于简化虚拟DOM
- 写法：var ele = <h1>Hello JSX!</h1>
- Note1: 它不是字符串，也不是HTML/XML标签
- Note2: 它最终产生的就是一个JS对象
# 3. jsx语法规则：
1. 定义虚拟DOM时，不要写引号。
2. 标签中混入JS表达式时，要使用{}。
3. 样式的类名指定不要class，要用className.
4. 内联样式。要使用`style={{key:value}}`的形式去写。
5. 虚拟DOM只能有一个根标签。
6. 标签必须闭合。
7. 标签首字母
    （1）若小写字母开头，则将标签转为html同名元素，若HTML中无对应的元素，则报错。
    （2）若大写字母开头，react就去渲染对应的组件。若组件没有定义，则报错。
# 4. jsx练习
1. 一定要区分：`js语句（代码）`和`js表达式`
2. 表达式：一定会产生一个值，可以放在任何一个需要值的地方： `a`, `a+b`, `demo(1)`, `arr.map()`,
`function test(){}`
3. 语句（代码）：`if() {}`, `for() {}`, `switch() {case: xxx}`

# 模块与组件、模块化与组件化
## 1. 模块
对外提供特定功能的js程序，一般就是一个js文件
随着业务逻辑增加，代码越来越复杂
复用js，简化js的编写，提高运行效率
## 2.组件
用来实现局部功能效果的代码喝资源的集合（html/css/js/image等）
一个界面的功能更复杂
复用代码，简化项目编码，提高运行效率
## 创建模块化、组件化、工程化的项目

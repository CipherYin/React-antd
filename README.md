# React-antd
生态介绍:
    Vue生态： Vue+Vue-Router+Vuex+Axios+Babel+Webpack
    React生态： React+React-Router+Redux+Axios+Babel+Webpack

React脚手架：
    为什么使用yarn: yarn是新一代包管理工具；速度快，安装版本统一，更安全，更简洁的输出，更好的语意化，lock文件版本锁定
 如何安装和使用React脚手架

如何使用yarn:
    yarn init
    yarn add
    yarn remove
    yarn install

React 生命周期包括那些：
当组件在服务端被实例化，首次被创建时，以下方法依次被调用：
        componentDidMount 不会在服务端被渲染的过程中调用。
    初始化阶段：
    1. getDefaultProps:获取实例的默认属性
    2. getInitialState: 获取每个实例的初始化状态
    3. componentWillMount: 组件即将被装载、渲染到页面上
    4. render:组件在这里生成虚拟的 DOM 节点
    5. componentDidMount:组件真正在被装载之后,已经渲染出真实dom

    运行中状态
    6. componentWillReceiveProps: 组件将要接收到属性的时候调用
    7. shouldComponentUpdate: 组件接受到新属性或者新状态的时候（可以返回 false，接收数据后不更新，阻止 render 调用，后面的函数不会被继续执行了
    8. componentWillUpdate: 组件即将更新不能修改属性和状态
    9. componentDidUpdate:组件已经更新
    销毁阶段：
    10. componentWillUnmount: 组件即将销毁


    每次修改 state，都会重新渲染组件，实例化后通过 state 更新组件，会依次调用下列方法：

    1、shouldComponentUpdate
    2、componentWillUpdate
    3、render
    4、componentDidUpdate

    shouldComponentUpdate 是做什么的，（react 性能优化是哪个周期函数？）

    shouldComponentUpdate 这个方法用来判断是否需要调用 render 方法重新描绘 dom。因为 dom 的描绘非常消耗性能，如果我们能在 shouldComponentUpdate 方法中能够写出更优化的 dom diff 算法，可以极大的提高性能。


    在react17 会删除以下三个生命周期
    componentWillMount，componentWillReceiveProps ， componentWillUpdate

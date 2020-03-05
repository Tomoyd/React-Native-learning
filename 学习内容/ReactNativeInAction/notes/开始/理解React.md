#### 用State管理组件数据

组件的props和state改变时，组件将会进行渲染，运行render函数，此时所有的子组件也将会渲染

- State只能在本组件内用setState 来更新改变
- State可以通过子组件的props传递给子组件，Props不能在该组件内进行更新改变，只能通过父组件传递给下一代

State可以在组件创建时的创建函数内初始化或者用一个属性初始化，一旦初始化后，就可以在组件中通过this.state访问

也可以用forceUpdate强制选择

子组件的状态改变只会重新执行子组件的render函数，不会引起父组件重新执行render函数

#### 生命周期方法

> 可以让我们在创建和销毁组件的某个特定的生命周期点，去做一些动作

1. Mounting(creation):创建挂载中，会执行，constructor   componentWillMount，componentDidMount
2. Updating：**shouldComponentUpdate**，render ComponentDidUpdate
3. Unmounting：componentWillUnmount
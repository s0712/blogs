# VUE常见面试题
1. 什么是mvvm?
- - - -
>   
> MVVM是Model-View-ViewModel的缩写,mvvm是一种设计思想.Model层代表数据模型,也可以在Model中定义数据修改和操作的业务逻辑;view代表UI组件,它负责将数据模型转化为UI展现出来,ViewModel是一个同步view和Model的对象.  
>   
在MVVM架构下,View和model之间并没有直接的联系,而是通过viewmodel进行交互,Model和ViewModel之间的交互是双向的,因此View数据的变化会同步到Model中,而Model数据的变化也会立即反应到View中.

ViewModel通过双向数据绑定把View层和Model层连接了起来,而View和Model之间的同步工作完全是自动的,无需人为干涉,因此开发者只需要关注业务逻辑,不需要手动操作dom,不需要关注数据状态的同步问题,复杂的数据状态维护完全由MVVM来统一管理.




2. mvvm和mvc区别?
- - - -
>     
> mvc和mvvm其实区别并不大,都是一种设计思想,主要就是mvc中的Controller演变成mvvm中的viewModel.mvvm主要解决了mvc中大量的DOM操作使页面渲染性能降低,加载速度变慢 ,影响用户体验,和当Model频繁发生变化,开发者需要主动更新到view  
>    



3. Vue的优点?
- - - -
- 低耦合. 视图(view)可以独立于Model 的变化和修改,一个viewModle可以绑定到不同的”view”上,当view变化的时候Model 可以不变,当Model 变化的时候 view也可以不变
- 可重用性, 你可以把一些视图逻辑放在一个viewModel里面,让很多view重用这段视图逻辑
- 独立开发. 开发人员可以专注于业务逻辑和数据的开发(viewModel),设计人员可以专注于页面设计,使用Expression Blend可以很容易设计界面并生成xml代码
- 可测试,界面速来是比较难于测试的,而现在测试可以针对viewModel来写.


4. 请详细说下你对vue生命周期的理解?
- - - -
> 答:总共分为8个阶段 创建前/后,载入前/后,更新前/后,销毁前/后.  
- 创建前/后: 在beforeCreate阶段,vue实例的挂载元素
El和数据对象data都是为undelfined,还未初始化,在created阶段,vue实例的数据对象data有了,el,还没有

- 载入前/后:在BeforeMount阶段,vue实例的$el和data都初始化了,但还是挂载之前为虚拟的dom节点,data.message还未替换.在mounted阶段,vue实例挂载完成,data.message成功渲染

- 更新前/后:当data变化是,会触发beforeUpdate和updated方法.

- 销毁前/后:在执行destory方法后,对data的改变不会在出发周期函数,说明此时vue实例已经解除了事件监听以及和dom的绑定,但是dom结构依然存在,



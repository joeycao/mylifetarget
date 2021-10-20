#20211017


```ad-abstract
title: 标签

#vue原理分析
#vue运行原理


```

### 内容

#### 运行原理图
```nomnoml
[new Mvvm] --> [Complie]
[new Mvvm] --> [Observer]
[Observer] 通知变化 --> [Dep]
[Complie] +-> [Upader]
[Dep] --> [Watcher]
[Upader] -->[Watcher]
  
```

#### 程序加载图

```nomnoml

[<frame> 加载流程|
  
  [main.ts] new App --> [App.vue]
  
  [App.vue| 加载三方组件]
	
  [App.vue] 初始化路由 -- [Route.ts]
  
  [Route.ts] <:- [View]
  
  [View| 模板|脚本|样式]
	  
  [View] +- [模板|AST]
  [View] +- [脚本|引组引入 | TS装饰器 |服务类]
  [View] +- [样式|scss 样式]
  [脚本] +- [服务类]
  [服务类] +- [状态数据|事件接收器| 事件处理任务]
  
]

```


#### 原理分解
[[Vue 双向绑定]] 
[[Vue 编译原理]] 
[[Vue 装饰器]] 
[[Vue 混合]] 
[[Vue3 组合函数]] 



### 引用
```ad-quote
title: 引用

#YT 理科生看世界《vue源码解析》


```



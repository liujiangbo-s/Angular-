# Angular
Angular 学习总结

## Angular 简介
Angular 是一个基于 TypeScript 构建的开发平台。它包括：
- 一个基于组件的框架，用于构建可伸缩的 Web 应用
- 一组完美集成的库，涵盖各种功能，包括路由、表单管理、客户端-服务器通信等
- 一套开发工具，可帮助你开发、构建、测试和更新代码

## 搭建开发环境
 -	安装 Node.js 
 -	安装 NPM 包管理器
 -	安装 Angular CLI `npm install -g @angular/cli`

## 初始化、运行应用
`ng new my-app`

`ng serve --open --port xxxx`

## Angular 要点

### 指令

- 插值 - 在 HTML 中使用插值和表达式。**可以用做 HTML 元素的内容或元素的属性的值，用 {{ ... }} 表示，支持变量和表达式**

- 模板语句 - 响应模板中的事件。**语法 (event)="statement"**

- 属性绑定 - 设置目标元素的属性或指令中带 @Input() 装饰器的属性。**使用 [ ... ] 表示**

- 事件绑定 - 监听事件和 HTML。**使用 EventEmitter **

- 双向绑定 - 在类及其模板之间共享数据。***使用 ([ ... ]) 表示**

- 模板引用变量 - 使用特殊变量来引用模板中的 DOM 元素。**使用 # ... 表示**

- 输入和输出 - 在父级上下文和子指令或组件之间共享数据。**使用 @Input() 和 @Output() 表示**，@Input() 允许父组件更新子组件中的数据，@Output() 允许子组件向父组件发送数据。

- 模板中的 SVG - 动态生成交互式图形。

### 指令

#### 内置指令

##### 内置属性型指令
- ngClass -- 添加和删除一组 CSS 类。可以和**表达式**、**方法**一起使用
- ngStyle -- 添加和删除一组 HTML 样式。设置内联样式，一般与**方法**一起使用
- ngModel -- 将数据双向绑定添加到 HTML 表单元素。显示和更新属性，作用如下：
    - 在 **app.module.ts** 中使用，管理项目中所有的模块、内置库、组件、服务等
    - 在 HTML 标签上使用 [(ngModel)] 绑定数据
    - ngModel 适用于 ControlValueAccessor 支持的元素

##### 内置结构型指令
- ngIf -- 从模板中创建或销毁子视图。
- ngFor -- 为列表中的每个条目重复渲染一个节点。
    - index 索引号
    - trackBy 跟踪条目
- ngSwitch -- 一组在备用视图之间切换的指令。
    - ngSwitch -- 一个属性型指令，它更改其伴生指令的行为。
    - ngSwitchCase -- 结构型指令，当其绑定值等于开关值时将其元素添加到 DOM 中，而在其不等于开关值时将其绑定值移除。
    - ngSwitchDefault -- 结构型指令，当没有选中的 NgSwitchCase 时，将其宿主元素添加到 DOM 中。
- ng-container 为没有 DOM 元素的指令安排宿主    

### 组件



### 依赖注入
1. 创建一个 service，使用 @Injectable 来修饰
2. 在组件的 constructor() 中注入服务
3. 类似 asp.net core 的构造函数注入

### 生命周期


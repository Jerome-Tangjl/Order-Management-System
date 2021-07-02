# Order-Management-System

## 项目概述

该项目实现了一个广告牌公司订单管理系统的网站实现。该网站能实现人员客户信息的管理以及整个订单的业务流程。

### 业务流程如下：

1. 接单⼈员登录系统创建订单，若客户不存在则先创建客户。录入客户信息  以及测量数据。
2. 测量⼈员前往现场进⾏测量，将测量数据录⼊系统。录入长度、宽度、高度以及数量等信息。
3. 设计⼈员根据测量数据，设计⼴告牌，将设计样板图上传⾄系统。录入材质、样板图⽚等信息。
4. 报价⼈员根据设计⼴告牌的⼤⼩、材质、数量等，给出报价并录⼊系统。录入报价等信息。
5. 客户⼈员通过系统查看设计信息和报价后，决定是否接受。
6. ⼯⼚⼈员登录系统，查看设计信息后进⾏⽣产，⽣产完毕则在系统进⾏确认。
7. 安装⼈员线下从⼯⼚获得产品后，前往客户地址进⾏安装，安装完毕则在系统进⾏确认。
8. 结案⼈员登录系统，确认该笔订单⽆误，则该订单结束；否则线下上报给公司管理员，公司管理员进⾏修改。


### 开发环境及框架

#### 前端

- 开发环境：vscode
- 框架及库：vue.js、element-UI、Vue router、axios、Vue-cli

> vue启动方法：
> 
> npm install
> 
> npm run dev


#### 后端

- SpringBoot
- Spring Data JPA
- Java(TM) SE Runtime Environment (build 16+36-2231)
- Java HotSpot(TM) 64-Bit Server VM (build 16+36-2231, mixed mode, sharing)

#### 数据库

- MySQL

#### 其他

- nginx反向代理

### 项目模块

- 页面展示模块
- 人员管理模块
- 客户管理模块
- 订单管理模块



## 前端

前端分为界面展示模块，人员、客户管理模块以及订单管理模块四个部分

### 页面展示模块

使用vue组件的思想，将页面分成侧边栏以及展示操作主界面两个部分。

![image](https://user-images.githubusercontent.com/74498528/124267240-95224700-db6a-11eb-8eb8-9103e5ace4c3.png)

#### 侧边栏实现：

1. 定义vue组件结合Element-UI进行界面的设计
2. 点击不同的按钮会使主界面跳转到不同的操作展示界面
  - 使用vue-router定义不同组件对应的路径，然后使用router-link标签来实现页面的跳转。
3. 不同身份的用户登陆后侧边栏展示的路由跳转不同
  - 根据用户的身份信息以及对应的权限，使用v-for有选择的在界面上展示可跳转的路由。

#### 主界面实现:

- 使用Element-UI实现对界面的展示
- 定义了一系列的vue组件以及对应的路由，以便在进行不同操作时完成主界面路由的跳转。
- 主界面要执行人员添加删除修改、人员订单客户展示等操作。

### 人员管理模块

- 主要功能：为管理员提供用户管理的可视化操作，管理员可以添加，删除，修改，查看所有用户信息。另外，登录，查看修改自己的用户信息功能由于和人员相关，也被放入人员管理模块。
- 用户信息：姓名，电话，邮箱，密码，身份
- 用户身份：公司管理员，接单人员，测量人员，设计人员，报价人员，工厂人员，安装人员，结案人员 
- 用户权限：不同身份的用户有不同的权限，其中只有管理员能进入人员管理模块

1. 用户登录：
输入网址，若没有登陆或cookie，拦截进入到登录界面，输入用户密码后，前端向后端提交用户登录请求，通过后获得用户信息，进入到首页。

![image](https://user-images.githubusercontent.com/74498528/124267651-1ed21480-db6b-11eb-8c1e-544571efd09e.png)

2. 



#### 要做的事
1. 用户的创建，修改，删除，查看
2. 客户的创建，修改，删除，查看
3. 订单的创建，修改，删除，查看
4. 用户、客户、订单的展示（table）
5. 用户密码修改
6. 不同用户的权限控制
7. 用户的登陆
8. 用户、客户、订单的查询


### 后端

本地可以使用IntelliJ IDEA编译运行。服务器上使用`java -jar`指令运行发布的文件。

## 效果演示






# doracms 2.1.2

![DoraCMS](https://www.html-js.cn/upload/images/ueditor/1056072974769197056.jpg "DoraCMS")

## 2.1.2版本更新
1、前台接口独立抽取api 

2、完善国际化逻辑

3、细分了文章审核的几种状态

4、优化了模板编辑模块，修复模板编辑bug，加入了模板导入功能，更方便的进行新模板开发

5、添加了帮助中心，和APP版本管理模块

6、优化了登录和注册模块

7、优化文章模块，添加文章自动解析为APP可以识别的JSON格式

8、对查询比较多的模块（如文章，分类，留言等）设置了索引

9、修复了一些内部报错引起的服务端自动重启问题

10、修复了一些安全性方面的问题


## 2.0.0版本更新
1、生产环境日志目录可配置，修复用户部署生产报路径找不到的问题

2、新增广告管理模块，修复多图轮播显示不正常的问题

3、修复删除文章没有同步删除关联留言的问题

4、更新前端后台样式

5、修复留言过滤特殊字符的问题

6、添加了留言回复功能

7、修复文章上传缩略图某些jpg文件无法上传的问题

8、完善了后台首页信息总览

9、修复了后台修改其它管理员权限会把自己的权限置空的问题

更新方法： 
1、checkout 最新 2.0.0 代码

2、删除 node_modules,重新安装依赖包

3、找到 configs/settings.js，将 SYSTEMLOGPATH 参数值修改为正式服务器上(生产环境)的日志目录(very important!)

3、启动数据库，执行npm run dev 


## 说明

DoraCMS 使用的技术栈：

1、vue + vuex + vue-router 全家桶

2、webpack 2

3、nodejs 8.0 + express 4

4、mongodb 3+

演示地址： [前端开发俱乐部](https://www.html-js.cn)   
后台登录： https://www.html-js.cn/dr-admin     测试账号：doracms/123456

部署文档： [前端内容管理框架 DoraCMS2.0 部署介绍](https://www.html-js.cn/details/ryn2kSWqZ.html)   

## 目录结构

```
├─build // webpack 相关配置文件
│
├─configs // 配置文件
│  │  
│  └─logConfig.js  // 日志配置文件
│ 
├─logs // 日志目录
│
├─dist  // webpack 生成文档存放目录
│  │
│  ├─server
│  │
│  └─static
│      ├─css
│      │
│      ├─images
│      │
│      ├─img
│      │
│      └─js
│
├─server    // 服务端目录
│  │
│  ├─lib    // 核心层
│  │
│  └─routes // 路由文件
│
├─src           // 客户端程序目录
│  │
│  ├─api        // api 配置文件
│  │
│  ├─filters    // 过滤器
│  │
│  ├─index      // 前台组件
│  │
│  ├─manage     // 后台组件
│  │
│  ├─template   // 初始模版
│  │
│  └─utils      // 实用工具
│
└─utils
    ├─middleware // 中间件
    │
    ├─authPower.js // 资源鉴权
    │
    ├─authSession.js // session 鉴权
    │
    ├─authToken.js // token鉴权
    │
    ├─logUtil.js // 日志配置
    │
    ├─settings.js // 关键信息配置
    │
    └─validatorUtil.js // 信息校验

```





## 准备工作:
安装 NodeJS:
https://nodejs.org/zh-cn/

安装 Mongodb:
https://www.mongodb.com/download-center#community

```shell
# 安装依赖
$ npm install

# 开发模式
$ npm run dev

# 生产模式
$ npm run build

# 启动(需先生成静态文件)
$ npm run start
```

首页
http://localhost:8080

登录
http://localhost:8080/dr-admin

# 捐赠
如果你发现DoraCMS很有用，可以请生哥喝杯咖啡(⊙o⊙)哦
<img width="650" src="http://7xkrk4.com1.z0.glb.clouddn.com/payme.jpg" alt="">

# LICENSE

MIT

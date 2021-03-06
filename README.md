# 说明
刚开始学习nodejs时不免枯燥，总想着如何造一个好看的前端页面，尝试着在网上搜索相关的项目找找灵感，发现对于前端使用vue.js搭配后台nodejs的教程不多（也可能是我没找着:camel:），不管怎样，在这个大前提下**DMB**的开发工作开始了。

**DMB**是针对经常使用excel的个人或者团体（比如公司每月提交excel报表）而开发的excel数据管理系统，他能够帮助您完成表格的整合、编辑、数据筛选以及导出等等功能，一键导入、按需筛选、指定导出，**DMB**能让你不再被被一堆excel文件折磨。

**DBM**后端是使用nodejs开发的服务端应用，响应[DBM前端](https://github.com/carrayboy/vue-DBM)的请求，其中涉及到sql语句组装、基于url的权限控制、异步的同步实现等。

如果您也想使用vue.js结合nodejs开发一个带前后端的完整应用的话，参考**DBM**的实现也许能够帮您解决如下问题

> **如何拦截路由实现未登录的页面不允许访问？**

> **如何拦截网络请求并在后台做权限验证？**

> **如何将前端后台两个工程整合为一个工程部署？**

> **如何动态动态生成SQL语句实现动态建表、自定义筛选等数据库操作？**

> **如何实现文件上传、后端分页等等**

由于此项目使用业余时间来做且属于边学边做，开发周期较长，代码的整洁程度仍待提高，我将不断修改做到自己满意为止，如果您发现问题请直接在Issues中提出，或者您对模块的实现有更好的解决方案欢迎**Pull Requset**

如果对您有帮助，您可以点击右上角 "**Star**" 支持一哈！谢谢！

# 目标功能
- [x] 用户登录
- [x] 修改密码、注销
- [x] 创建用户
- [x] 启用、禁用用户
- [x] 创建、删除角色
- [x] 修改角色权限
- [x] 参考java shiro框架的权限管理简单实现
- [x] 以瀑布流的形式展示所有数据表格
- [x] 数据表格的名称、列项编辑（提供文本、数字、时间、选项以及图片五种列类型）
- [x] 数据表格的修改日志
- [x] 表数据展示以及后端分页
- [x] 表数据的新增、编辑、删除
- [x] 自定义表格筛选条件
- [x] excel文件导入
- [x] excel文件导出
- [ ] 操作日志


# 项目运行

# 克隆到本地
git clone https://github.com/carrayboy/nodejs-DBM.git

# 安装依赖包
npm install

# 配置Mysql数据库
1. 新建名称为vue_dm_db的数据库并执行conf目录下的vue_dm_db.sql脚本
2. 修改conf目录下的db.json配置数据库连接的账号密码
3. dev为开发环境，production为生成环境

# 启动服务
nodejs server.js

# 前端工程演示

[demo地址](https://carrayboy.github.io/vue-DBM/index.html)

# 对应的前端工程

[地址在这里](https://github.com/carrayboy/vue-DBM)

# 如何结合前后端项目
1. 打开cmd控制台，cd进入到前端工程的根目录运行npm run build
2. 等待一段时间将在dist目录下生产index.html与static文件夹，将其拷入后端的public目录下（运行nodejs server.js将会生成public目录）
3. 重启服务，在地址栏输入localhost:3982




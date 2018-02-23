安装node,express,mongo

express -e
e表示ejs模板引擎，不写 -e 默认的创建jade模板引擎

npm install  //读取根目录中的package.json文件然后安装项目所依赖的包

node app
启动项目
提示1：如果不能启动项目：看看app.js文件中没有监听端口。如果没有,
在 module.exports = app;语句之前添加app.listen(3000);

–node_modules   项目中依赖的包
–public         公共资源放的目录
–routes         学名 路由，里面放着一些路由文件
–views			 放着就是页面文件了
–app.js		 项目的入口文件。当然你也可以改成其他的名字。

sudo mongod  启动mongo
目录下 命令  mongo  连接mongo
或者下载可视化工具robomongo 连接mongo,填写对应的端口号

use flyfishBlog  \创建一个叫flyfishBlog的数据库
db.createCollection(“users”) \创建一个集合
db.users.insert({“name”:“admin”,“password”:“111”}) \给users集合添加一个文档。
db.users.find() \查询你添加的文档





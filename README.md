### 说明

- 该项目仅为樛木博客前端网站（包括PC管理端、web桌面端、移动端、App、小程序）托管静态资源，如：大图片、大文件（css字体库、插件等）等。

### 运行

- 开发环境使用静态资源

  1. 直接将静态资源地址代理至测试环境地址（推荐）

  2. 本地开启一个静态资源服务（不推荐）

    + 全局安装`http-server`  `npm i -g http-server`

    + 将该项目切换至`develop`分支  `git checkout develop`

    + 开启一个服务  `http-server`

    + 然后将静态资源地址代理至该服务地址`http://127.0.0.1:8080/`即可


- 测试环境使用静态资源

  + 部署樛木静态资源托管测试环境（具体看对应脚本）

  + 在`nginx`配置对应的代理

  + 然后将静态资源地址代理至该服务地址`https://www.jiumublog.cn/jiumu-static-test/`即可

- 生产环境使用静态资源

  + 部署樛木静态资源托管生产环境（具体看对应脚本）

  + 在`nginx`配置对应的代理

  + 然后将静态资源地址代理至该服务地址`https://www.jiumublog.cn/jiumu-static-prod/`即可


### 项目使用静态资源

- pc 项目使用
```
// .vue 文件
<img :src="$STATIC_URL + 'pc/tags.png'" alt=""> 

// .scss 文件
background: url('#{$STATIC_URL}/pc/tags.png');
```

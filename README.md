# roim-picx

### 预览地址
[roim-picx](https://roim.page)
> 该系统仅作为预览使用，每天有使用限额，请勿大量上传图片。不要使用该图床的地址作为生产使用，因为要定时删除。

### 一款基于Cloudflare的Worker、R2、Pages实现的图床应用，具有以下特点：
* 10GB的免费存储空间
* 每月300W次的不计流量的图片访问，每天10W的限制。
* 每月100W次的图片上传次数
* 不需要自己购买服务器，克隆代码后部署CloudFlare即可使用。
* 独立部署不需要担心被第三方删除数据。

## Token
> 4xVSYkCKw2ExbPNEaMPjCnaaOowU9sTf

### 已实现功能
* 图片批量上传
* 图片列表查询
* 图片删除
* 目录创建
* 按目录查询
* 链接地址点击复制
* 简单的身份认证功能，进入管理页面需要授权

### TODO
* 上传时支持选择目录。
* 提供删除图片的访问链接
* 管理页面支持分页加载图片

### 使用教程
* 1.fork项目到自己的github
* 2.注册CloudFlare并开通R2服务
* 3.找到Pages选项并且创建项目
* 4.选择项目创建方式
* 5.链接Github或GitLab并选需要构建的项目
*   框架预设：无
*   构建命令：npm run build
*   输出目录：dist
*   完成创建
* 6.设置环境变量
* AUTH_TOKEN：授权码
* BASE_URL：复制的路径，如无，则输入page域名(e.g. www.example.com)
* 7.设置项目的函数信息绑定R2和KV服务
* Workers & Pages -> {Project Name} -> Settings -> Functions
![Upload](https://pics.steventan.work/8M8lBhK.png)
![Upload](https://pics.steventan.work/FtnlBhK.png)
* 8.重新部署


### 项目参考来源
[1. cfworker-kv-image-hosting](https://github.com/realByg/cfworker-kv-image-hosting)

[2. HikariSearch](https://github.com/mixmoe/HikariSearch)

项目fork自roimdev/roim-picx

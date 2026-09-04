# 接口
多线路  
https://tvbox-interface.pages.dev/index.json  

多仓库  
https://tvbox-interface.pages.dev/duo.txt  

单线路文件  
https://tvbox-interface.pages.dev/单线路.txt  




# GitHub 使用 Pages 访问 TVBox 接口

> 缺点：会使用免费的 100G 流量

## 步骤 1：创建 GitHub 仓库

1. 登录 [GitHub](https://github.com/)。
2. 点击右上角的 `+` 号，选择 **New repository**（新建仓库）。
3. 填写仓库名称（例如：`tvbox-interface`）。
4. 将仓库设为 **Public**（公开，**注意：必须公开才能使用 Pages**）。
5. 勾选 **Add a README file**，点击 **Create repository**。

## 步骤 2：上传接口配置文件

1. 在刚建好的仓库中，点击 **Add file** -> **Create new file**。
2. 文件名输入：`index.json` 或 `tv.json`。
3. 在编辑框内粘贴你的 TVBox 接口配置代码（标准的 JSON 格式，包含 `sites`、`lives` 等字段）。
4. 点击右上角 **Commit changes...** 提交保存。

> **注意**：必须使用文件名输入：`index.json` 或 `tv.json`。没有这两个文件，点第三步不能出现相应设置。

## 步骤 3：开启 GitHub Pages 服务

1. 进入该仓库的 **Settings**（设置）选项卡。
2. 在左侧菜单栏找到并点击 **Pages**。
3. 在 **Build and deployment** 下方的 **GitHub Pages Jekyll** 选择 **Config**。点击右上角 **Commit changes**。
   弹出界面选择 **Commit changes**，点击左上角返回两次回到 **Settings** -> **Pages**。
4. 在 **Build and deployment** 下方的 **Static HTML** 选择 **Config**。点击右上角 **Commit changes**。
5. 点击左上角 **code** 返回主界面。

## 步骤 4：获取并使用接口链接

最终接口是：

- `https://你的用户名.github.io/tvbox-interface/`
- 或者 `https://你的用户名.github.io/tvbox-interface/index.json` 或 `tv.json`（取决于使用哪个文件）

其他文件是：

`https://你的用户名.github.io/tvbox-interface/文件路径/文件名.扩展名`

---

# Cloudflare Pages 部署 TVBox 接口步骤

## 一、 准备工作

1. 注册/登录 GitHub 账号。
2. 找到支持 Cloudflare Pages 的 TVBox 接口开源项目，将其 Fork 到你自己的仓库中。
3. 注册/登录 Cloudflare 账号。

## 二、 部署步骤

1. 登录 Cloudflare Dashboard。
2. 点击左侧菜单栏的 "Workers 和 Pages"，然后点击 "创建"。
3. 选择 "Pages" 选项卡，点击 "连接到 Git"。
4. 授权你的 GitHub 账号，并选择刚刚 Fork 的 TVBox 项目仓库。
5. 在构建设置（Build settings）页面，通常保持默认设置即可。
6. 点击 "保存并部署"，等待系统自动构建完成。

## 三、 接口使用

1. 部署完成后，Cloudflare 会生成一个以 `.pages.dev` 结尾的免费默认域名。
2. 最终接口地址是  
https://xxx.pages.dev/api （必须加上文件名.扩展名）
例如https://xxx.pages.dev/index.json  
3. 打开 TVBox 或影视仓客户端，进入设置 -> 配置地址，将该链接填入即可。
其他文件调用就是路径/文件路径/文件名.扩展名  


## 四、 绑定域名
默认绑定域名无法使用，因为cloudfire有安全验证，无法直接调用。  

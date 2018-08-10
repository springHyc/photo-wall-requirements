# photo-wall-requirements

照片墙的需求文档以及设计文档。

该文档是 gitbook 文档。同时该项目启用了在 GitHub 上的在线演示

## gitbook 文档启动

### 初始化

确保你的机器中有 gitbook 命令，如果没有你可以执行 `npm i -g gitbook`

### 启动

`gitbook serve`

在浏览器中输入http://localhost:4000/

## GitHub 在线演示的部署

1. 切换到 gh-pages 分支 git checkout -b gh-pages(创建 gh-pages 并切换到该分支)/ git checkout gh-pages (切换到 gh-pages 分支)

2. 执行 npm run build 命令，gitbook 项目使用`gitbook build`，构建代码
3. 将 build/dist 目录下的所有文件夹推送至远程仓库的 gh-pages 分支，执行以下命令：

- 强制添加 /`_book`(gitbook 项目)文件夹，因为.gitignore 文件中定义了忽略该文件
  `git add -f _book`
  ​
- 提交到本地暂存区
  `git commit -m 'Initial the page of project'`
  ​
- 部署 dist 目录下的代码
  `git subtree push --prefix _book origin gh-pages`

# Git与代码版本管理实践 README

## 一、学习资料来源及相关链接
1. Git官方文档：https://git-scm.com/doc
2. 菜鸟教程 Git 教程：https://www.runoob.com/git/git-tutorial.html
3. GitHub官方帮助文档：https://docs.github.com

## 二、实践流程
### 1. Git环境安装与配置
1. 从Git官网下载对应操作系统安装包，完成安装；
2. 打开Git Bash，配置用户名与邮箱：
git config --global user.name "你的姓名"
git config --global user.email "你的邮箱"
3. 用git config --list验证配置是否生效。

### 2. 本地仓库创建
1. 新建文件夹git-learning，进入目录执行：
git init
2. 初始化成功，生成.git隐藏文件夹，本地仓库创建完成。

### 3. 远程仓库创建与关联
1. 注册GitHub账号，新建公开仓库git-practice-2026；
2. 本地仓库与远程仓库关联：
git remote add origin 你的GitHub仓库地址

### 4. 代码提交与推送
1. 新建test.py文件，编写简单代码；
2. 执行git add .暂存文件，git commit -m "提交信息"完成提交；
3. 执行git push origin main推送到远程仓库。

## 三、提交内容说明
1. 第一次提交（feat: init project）：初始化仓库，添加.gitignore与基础测试文件；
2. 第二次提交（docs: add README draft）：编写README初稿，记录实践步骤；
3. 第三次提交（fix: complete notes）：完善学习心得、问题与解决方法。

## 四、遇到的问题及解决方法
### 问题1：git push 报错「remote: Permission to user/repo denied」
- 原因：GitHub不再支持密码登录，需要使用个人访问令牌（PAT）。
- 解决方法：在GitHub Settings中生成Personal Access Token，推送时用令牌代替密码。

### 问题2：git commit 提示「nothing to commit」
- 原因：文件未执行git add暂存，或文件无修改。
- 解决方法：先执行git add 文件名或git add .，再执行git commit。

### 问题3：远程仓库与本地冲突，push失败
- 原因：远程文件与本地不一致。
- 解决方法：先执行git pull origin main拉取合并，再重新git push。

### 问题4：fatal: remote origin already exists
- 原因：本地已关联过远程仓库。
- 解决方法：使用git remote remove origin删除原有关联，再重新关联新仓库。

## 五、Git学习心得
通过本次实践，我掌握了Git安装配置、本地仓库、远程提交、版本回溯等核心操作。Git能清晰记录代码修改历史，有效避免文件丢失、版本混乱等问题，是工程化开发与团队协作的必备工具。
GitHub作为全球最大的代码托管平台，配合Git使用可以实现代码云端存储、团队协作与开源贡献。后续我会继续学习分支管理、合并、冲突解决、协作开发等高级功能，提升工程化开发能力。

# 1、仓库初始化
- 进入到目标目录
- 执行:git init

# 2、配置仓库专属用户信息
配置
- 设置专用用户名（可自定义，建议用 GitHub 用户名） 
- git config user.name "你的GitHub用户名" 

- 设置专用邮箱（使用准备好的邮箱） 
- git config user.email "alihanengage@126.com"

验证
git config user.name # 应显示刚才设置的用户名 
git config user.email # 应显示 alihanengage@126.com

# 3、关联远程GitHub仓库
关联远程仓库
- git remote add origin https://github.com/BigDogRoot/obsidian.git

若之前已关联过其他远程仓库，需先删除旧关联：
- git remote remove origin

# 4、首次同步
- 拉取
**git pull origin master**

-  若出现历史关联错误
如果提示 `fatal: refusing to merge unrelated histories`，执行强制拉取（谨慎使用，可能覆盖本地文件）：
git pull origin main --allow-unrelated-histories

# 5、编辑后提交
修改笔记后，在终端执行：

- 查看修改文件
git status

- 添加到暂存区
git add .

- 提交到本地仓库
git commit -m "描述本次修改内容"

- 推送到远程
**git push origin master**


### 首次推送认证

首次推送会提示输入 GitHub 账号信息：

- **用户名**：输入你的 GitHub 账号用户名
- **密码**：需使用 GitHub 个人访问令牌（PAT），而非账号密码
    1. 生成令牌：GitHub → 头像 → Settings → Developer settings → Personal access tokens → Generate new token
    2. 权限勾选：至少勾选 `repo` 相关权限
    3. 生成后复制令牌，粘贴到终端密码输入处（粘贴时终端可能不显示内容，直接回车即可）
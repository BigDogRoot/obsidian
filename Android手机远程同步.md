
1. **Obsidian 安卓客户端**：确保已安装并打开你的笔记库
2. 在Obsidian的Git插件：安装Git插件
3. **支持 Git 的文件管理器**：推荐 **Termux**（终端模拟器，可执行 Git 命令）或 **MT 管理器**（需手动配置 Git）
4. **Git 环境**：在 Termux 中安装 Git
5. **GitHub 账号**：已创建远程仓库（如你提供的 `https://github.com/BigDogRoot/obsidian.git`）


#### 1、**安装并配置 Termux**
- 下载地址
https://github.com/termux/termux-app

- 安装Git
命令1：pkg update && pkg upgrade -y 
命令2：pkg install git -y

- 获取存储访问权限
```bash
# 先获取存储访问权限
termux-setup-storage
```


#### 2、在Termux里完成Git仓库配置
找到OB仓库在你手机里的绝对路径：
- 打开 Obsidian 安卓客户端，进入你的笔记库
- 记下笔记库在手机中的存储路径（通常为以下路径之一）：
    - 内部存储：`/storage/emulated/0/Documents/你的笔记库名称/`
    - 自定义路径：通过 Obsidian 设置中的「打开文件夹」确认具体路径


进入到OB仓库地址
 - cd /storage/emulated/0/Documents/你的OB仓库地址

- 1、初始化：git init
- 2、设置name:git config user.name "名称"
	- 如果因为没有识别成Git仓库导致设置不成功，可以尝试执行：bash GIT_DIR=.git git config user.name "BigDogRoot"
- 3、设置email: git config user.email "邮箱地址"
- 4、关联远程仓库：git remote add origin https://github.com/你的地址/obsidian.git
	- 当因为信任导致关联失败时，添加到安全目录里：git config --global --add safe.directory /storage/emulated/0/Documents/obsidian/ali
- 5、首次同步：git pull origin master --allow-unrelated-histories
	- 看你的分支叫什么，我的是master
	- 如果因为存在一些本地没有跟踪的文件导致拉取失败可以采取：
		- **删除本地冲突文件**：```bash
rm -rf


方便的同步脚本
~~~ bash

# 编辑脚本 
nano sync.sh 

# 写入内容（替换路径和分支） #!/data/data/com.termux/files/usr/bin/bash 
cd /storage/emulated/0/Documents/你的笔记库路径 
git pull origin main 
git add . 
git commit -m "自动同步：$(date)" 
git push origin main 

# 保存并赋予权限 
chmod +x sync.sh 

# 后续同步直接运行 
./sync.sh
~~~


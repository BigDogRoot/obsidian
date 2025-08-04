
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


 cd /storage/emulated/0/Documents/记录/小白撒狗粮的仓库/小白撒狗粮的仓库

# Git 学习笔记

> 适用于：Windows 系统 + GitHub

---

## 1. Git 是什么？

Git 是一个**版本控制系统**，可以：

- 📦 **备份代码**：每次提交都是一个快照
- ⏪ **回退版本**：出错了可以回到之前的状态
- ☁️ **云端同步**：推送到 GitHub，多设备协作
- 🌿 **分支管理**：多人并行开发不冲突

---

## 2. 核心概念

| 概念 | 说明 |
|------|------|
| **仓库 (Repository)** | 项目文件夹，包含所有代码和历史记录 |
| **提交 (Commit)** | 一次代码快照，相当于一个存档点 |
| **暂存区 (Stage)** | 准备提交的文件列表 |
| **远程仓库 (Remote)** | GitHub 上的云端仓库 |
| **分支 (Branch)** | 独立的开发线，默认是 `main` |

### 工作流程图

```
[工作目录] --git add--> [暂存区] --git commit--> [本地仓库] --git push--> [GitHub]
```

---

## 3. 初始配置（只需做一次）

```bash
# 设置用户名（显示在提交记录中）
git config --global user.name "你的名字"

# 设置邮箱
git config --global user.email "你的邮箱@example.com"

# 查看配置
git config --list
```

---

## 4. 基础命令速查表

### 4.1 创建仓库

```bash
# 在现有项目中初始化 Git
cd "你的项目路径"
git init

# 或者从 GitHub 克隆
git clone https://github.com/用户名/仓库名.git
```

### 4.2 日常备份（最常用！）

```bash
# 第一步：查看哪些文件被修改了
git status

# 第二步：添加所有修改到暂存区
git add .

# 第三步：提交（创建一个存档点）
git commit -m "描述这次修改"

# 第四步：推送到 GitHub（云端备份）
git push
```

### 4.3 查看历史版本

```bash
# 查看提交历史（简洁版）
git log --oneline

# 查看提交历史（详细版）
git log

# 查看某个文件的修改历史
git log --oneline -- 文件路径
```

### 4.4 查看修改内容

```bash
# 查看哪些文件被修改（未提交）
git status

# 查看具体修改了什么
git diff

# 查看某个文件的修改
git diff 文件路径
```

### 4.5 撤销修改

```bash
# 撤销工作区的修改（还没 add）
git checkout -- 文件路径

# 撤销暂存区的文件（已 add，还没 commit）
git reset HEAD 文件路径

# 回退到上一次提交（已 commit，丢弃本次修改）
git reset --hard HEAD~1
```

### 4.6 版本回退

```bash
# 查看历史，找到要回退的 commit ID
git log --oneline

# 回退到指定版本（保留修改在工作区）
git reset --soft 提交ID

# 回退到指定版本（彻底丢弃修改，危险！）
git reset --hard 提交ID

# 回退单个文件到某个版本
git checkout 提交ID -- 文件路径
```

---

## 5. GitHub 云端操作

### 5.1 首次连接 GitHub

```bash
# 添加远程仓库
git remote add origin https://github.com/用户名/仓库名.git

# 首次推送
git push -u origin main
```

### 5.2 日常推送/拉取

```bash
# 推送到云端
git push

# 从云端拉取最新代码
git pull
```

### 5.3 在新电脑上开始工作

```bash
# 克隆仓库
git clone https://github.com/用户名/仓库名.git

# 进入项目
cd 仓库名

# 开始工作...
```

---

## 6. 分支操作 (Branch)

分支让你可以在不影响主代码的情况下开发新功能。

### 6.1 查看分支

```bash
# 查看本地分支（* 表示当前分支）
git branch

# 查看所有分支（包括远程）
git branch -a

# 查看分支详细信息
git branch -v
```

#### 输出示例

```
* main
  feature-fps-optimization
  experiment-tensorrt
```

### 6.2 创建分支

```bash
# 创建新分支
git branch 分支名

# 创建并切换到新分支（推荐）
git checkout -b 分支名

# 或使用新命令（Git 2.23+）
git switch -c 分支名
```

### 6.3 切换分支

```bash
# 切换到已存在的分支
git checkout 分支名

# 或使用新命令（Git 2.23+）
git switch 分支名

# 切换回上一个分支
git checkout -
```

### 6.4 合并分支 (Merge)

```bash
# 先切换到目标分支（通常是 main）
git checkout main

# 合并其他分支到当前分支
git merge 要合并的分支名
```

### 6.5 删除分支

```bash
# 删除本地分支（已合并的）
git branch -d 分支名

# 强制删除本地分支（未合并的）
git branch -D 分支名

# 删除远程分支
git push origin --delete 分支名
```

## 7. .gitignore 文件

告诉 Git 哪些文件**不需要备份**（如临时文件、大文件、密码）。

### Unity 项目常用 .gitignore

```
# Unity 生成的文件
Library/
Temp/
Obj/
Build/
Logs/

# IDE 文件
.vs/
*.csproj
*.sln

# Python 缓存
__pycache__/
*.pyc

# 模型权重（太大）
*.pth
*.onnx
```

## 8. 命令速查卡片

### 基础操作

| 操作 | 命令 |
|------|------|
| 初始化仓库 | `git init` |
| 克隆仓库 | `git clone URL` |
| 查看状态 | `git status` |
| 查看状态（简洁） | `git status -s` |
| 添加文件 | `git add .` |
| 提交 | `git commit -m "message"` |
| 推送 | `git push` |
| 拉取 | `git pull` |
| 查看历史 | `git log --oneline` |
| 查看修改 | `git diff` |
| 回退版本 | `git reset --hard 提交ID` |

### 分支操作

| 操作 | 命令 |
|------|------|
| 查看分支 | `git branch` |
| 查看所有分支 | `git branch -a` |
| 创建分支 | `git branch 分支名` |
| 创建并切换分支 | `git checkout -b 分支名` |
| 切换分支 | `git checkout 分支名` |
| 合并分支 | `git merge 分支名` |
| 删除分支 | `git branch -d 分支名` |
| 强制删除分支 | `git branch -D 分支名` |

---

## 9. 学习资源

- [Git 官方文档](https://git-scm.com/doc)
- [GitHub 官方教程](https://docs.github.com/cn/get-started)
- [廖雪峰 Git 教程](https://www.liaoxuefeng.com/wiki/896043488029600)（中文，适合入门）

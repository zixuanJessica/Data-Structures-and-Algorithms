# 管理建模课程作业提交 SOP

更新时间：2026-03-20

## 1. 你当前机器上的状态

已具备：

- 已安装 `git`：`git version 2.50.1`
- 已安装 `ssh`：`/usr/bin/ssh`
- Git 全局身份已配置：
  - `user.name = zixuanJessica`
  - `user.email = guozixuan324@gmail.com`
- 课程仓库已克隆到本机：
  - 本地路径：`/Users/jessica/codes/task00-zixuanJessica`
  - 提交分支：`main`
  - 你的远程仓库：`origin = https://github.com/simu-class-2026-brook/task00-zixuanJessica.git`

目前缺少或需要注意：

- 你计划使用的工作总目录 `~/Documents/管理建模` 目前还不存在。
- 我在当前受限环境里无法真正连到 GitHub，所以这次不能替你验证 `push` 是否一定成功。
- 你现在已有课程仓库在 `/Users/jessica/codes/task00-zixuanJessica`，如果以后想统一到 `~/Documents/管理建模`，建议把后续课程相关文件都放到这个总目录下管理。

## 2. 推荐的目录结构

建议以后固定使用下面这个结构：

```text
/Users/jessica/Documents/管理建模/
├── task00-zixuanJessica/        # GitHub Classroom 作业仓库
├── 临时草稿/                     # 不准备提交的草稿、截图、笔记
└── 管理建模课程作业提交SOP.md      # 本说明
```

如果你后续所有作业都继续提交到同一个仓库，那么你平时真正要修改的目录应是：

```text
/Users/jessica/Documents/管理建模/task00-zixuanJessica
```

## 3. 每次提交作业的标准流程

### 第 0 步：进入仓库

```bash
cd ~/Documents/管理建模/task00-zixuanJessica
```

如果你暂时还没把仓库放到这个位置，而是继续用当前已有仓库，就先进入：

```bash
cd /Users/jessica/codes/task00-zixuanJessica
```

### 第 1 步：先看当前状态

```bash
git status
```

作用：

- 确认自己当前就在正确仓库里
- 看看哪些文件被修改了
- 避免把无关文件一起提交

### 第 2 步：把本次作业内容放到 `Student_Workspace`

课程仓库的说明里已经明确，本学期作业都放到：

```text
Student_Workspace/
```

建议命名规范：

```text
Student_Workspace/
├── Task01/
├── Task02/
├── Task03/
└── ...
```

每次新作业都单独建一个文件夹，里面再放：

- 代码
- 报告
- 图片
- 数据

### 第 3 步：再次确认变更

```bash
git status
```

重点检查：

- 只提交这次作业相关文件
- 没有把缓存文件、系统文件、无关资料一起带上去

### 第 4 步：加入暂存区

如果你想把本次全部改动都提交：

```bash
git add .
```

如果你只想提交某个作业文件夹，更稳妥：

```bash
git add Student_Workspace/Task01
```

### 第 5 步：写提交说明

```bash
git commit -m "提交 Task01 作业"
```

推荐提交信息模板：

```text
提交 Task01 作业
更新 Task02 报告
修正 Task03 结果图
补充 Task04 代码与说明
```

### 第 6 步：推送到 GitHub

```bash
git push origin main
```

推送成功后，你的作业就会上传到：

```text
https://github.com/simu-class-2026-brook/task00-zixuanJessica
```

## 4. 以后最常用的完整命令

```bash
cd ~/Documents/管理建模/task00-zixuanJessica
git status
git add .
git commit -m "提交 TaskXX 作业"
git push origin main
```

## 5. 第一次整理到推荐目录时怎么做

如果你准备把现有仓库统一放到 `~/Documents/管理建模` 下，建议按下面思路操作：

1. 先创建总目录 `~/Documents/管理建模`
2. 再把仓库 `task00-zixuanJessica` 放进去
3. 以后始终在这个目录里完成编辑、提交和推送

注意：

- 同一个仓库不要在多个位置来回混用太久，容易搞混哪个才是最新版本。
- 如果你已经在 `/Users/jessica/codes/task00-zixuanJessica` 持续工作过，迁移时要先确认未提交内容是否都还在。

## 6. 遇到问题先用这几个命令排查

查看当前修改：

```bash
git status
```

查看远程仓库地址：

```bash
git remote -v
```

查看当前分支：

```bash
git branch --show-current
```

## 7. 你这台机器当前最关键的结论

- 环境基本够用，正常完成 Git 提交没有明显缺项。
- 你真正还需要补齐的是统一的本地工作目录：`~/Documents/管理建模`
- 当前课程仓库已经存在，且远程地址正确。
- 后续只要坚持在同一个仓库里修改、`commit`、`push`，就可以持续提交整学期作业。

# Project 1 作业要求速记

更新时间：2026-03-20

## 1. 仓库分工

- 课程总仓库只负责看作业说明、Rubric 和资料。
- 个人 GitHub Classroom 仓库才是你真正提交作业的地方。
- 你后续需要 `git push` 的地方，是你的个人仓库 `task00-zixuanJessica`。

## 2. Project 1 是什么

本次作业是：

- `Project 1`
- 主题：`Uniswap V3 底层状态机模拟`

## 3. 去哪里看正式要求

正式要求不在你的私人仓库里，要去课程主页面看：

- `03_Assignments`
- 重点阅读文件：`Project1_V3_State_Machine.md`

做题前必须先看这个文件，确认：

- 最低功能要求（MVP）是什么
- 哪些内容明确不要做，避免写超纲代码

## 4. 老师强调的两个核心防坑点

### 4.1 计算精度

严禁在底层状态换算中使用：

- `float`
- `decimal`

必须使用：

- Python 原生大整数
- `Q64.96` 相关的位运算
- 向右 96 位的整数运算思路

结论：

- 这份作业不能用浮点数思维去写
- 必须按智能合约底层整数逻辑实现

### 4.2 正确使用 AI

不要直接泛泛地问 AI：

- “帮我写个 Uniswap 交易公式”

更稳妥的方式是：

- 先看老师指定的阅读清单
- 找到 Solidity 官方源码
- 重点参考 `UniswapV3Pool.sol`
- 把关键 Solidity 源码片段交给 AI，要求做 1:1 Python 翻译

结论：

- 优先信源码，不要优先信口头总结
- AI 适合做“逐段翻译”和“对照解释”，不适合凭空生成公式

## 5. 这次作业最后要交什么

老师明确提到你至少要完成：

- `simulator.py`
- `test_invariants.py`

提交方式：

- 在个人仓库中完成代码
- 提交到远程仓库
- GitHub Actions 会自动跑 `ci.yml`
- 看到绿色对勾，说明自动检查通过

## 6. 你之后做 Project 1 的建议流程

1. 先去课程总仓库阅读 `Project1_V3_State_Machine.md`
2. 在个人仓库里找到并完善 `simulator.py`
3. 写好 `test_invariants.py`
4. 本地先自查逻辑和边界情况
5. `git add`、`git commit`、`git push`
6. 去 GitHub 看 Actions 是否通过

## 7. 你最该记住的版本

- 看要求：课程总仓库
- 写代码：个人仓库
- 提交作业：个人仓库
- 核心禁忌：不要用 `float` / `decimal`
- 核心方法：按 Solidity 源码做整数级翻译

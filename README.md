# 从 0 开始创建 Agent

这个文件夹用于系统学习和实践 Agent 开发，包括：

- Agent 基础概念
- LLM API 调用
- Tool Calling / Function Calling
- MCP（Model Context Protocol）
- 多 Agent 协作
- 记忆、规划、工作流与评测

## 1. 创建项目文件夹

如果你还没有创建文件夹，可以在终端运行：

```bash
mkdir agent-from-zero
cd agent-from-zero
```

当前这个文件夹已经创建好，路径是：

```bash
/home/cui/Graduate/agent-from-zero
```

## 2. 初始化 Git 仓库

进入项目文件夹：

```bash
cd /home/cui/Graduate/agent-from-zero
```

初始化 Git：

```bash
git init
```

初始化后，Git 会创建一个隐藏的 `.git` 目录，用来保存版本历史。

## 3. 配置 Git 用户信息

如果你是第一次在这台机器上使用 Git，需要配置用户名和邮箱：

```bash
git config --global user.name "你的名字"
git config --global user.email "你的邮箱@example.com"
```

查看配置：

```bash
git config --global --list
```

## 4. 查看当前状态

```bash
git status
```

常见状态含义：

- `Untracked files`：Git 还没有跟踪的新文件
- `Changes not staged for commit`：文件改了，但还没加入暂存区
- `Changes to be committed`：文件已经暂存，等待提交

## 5. 添加文件到暂存区

添加当前目录下所有文件：

```bash
git add .
```

只添加指定文件：

```bash
git add README.md
```

## 6. 创建第一次提交

```bash
git commit -m "Initial commit"
```

`commit` 是一次版本快照。以后每完成一个小目标，都可以提交一次。

## 7. 查看提交历史

```bash
git log
```

更简洁的写法：

```bash
git log --oneline
```

## 8. 创建 `.gitignore`

`.gitignore` 用来告诉 Git 哪些文件不需要纳入版本管理。

常见内容：

```gitignore
.env
__pycache__/
*.pyc
node_modules/
.DS_Store
```

如果你后续使用 OpenAI API Key、数据库密码、私有 token，一定不要提交到 Git。

## 9. 连接 GitHub 远程仓库

先在 GitHub 上创建一个空仓库，然后复制仓库地址。

如果使用 HTTPS：

```bash
git remote add origin https://github.com/你的用户名/agent-from-zero.git
```

如果使用 SSH：

```bash
git remote add origin git@github.com:你的用户名/agent-from-zero.git
```

查看远程仓库：

```bash
git remote -v
```

## 10. 推送到 GitHub

第一次推送：

```bash
git branch -M main
git push -u origin main
```

之后再推送，只需要：

```bash
git push
```

## 11. 推荐学习目录结构

后续可以按这个结构扩展：

```text
agent-from-zero/
├── README.md
├── notes/
│   ├── 01-agent-basics.md
│   ├── 02-tool-calling.md
│   └── 03-mcp.md
├── examples/
│   ├── simple-agent/
│   ├── tool-agent/
│   └── mcp-agent/
└── .gitignore
```

## 12. 建议的第一次练习

1. 运行 `git init`
2. 创建 `.gitignore`
3. 运行 `git add .`
4. 运行 `git commit -m "Initial commit"`
5. 创建 `notes/01-agent-basics.md`
6. 写下你对 Agent 的第一版理解
7. 再提交一次：`git commit -m "Add agent basics notes"`


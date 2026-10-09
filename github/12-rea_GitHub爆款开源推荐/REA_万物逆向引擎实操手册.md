# 🔍 REA (Reverse Engineer Anything) · 万物逆向引擎实操指南

> **官方开源仓库**：https://github.com/morluto/rea  
> **官方产品主页**：https://rea.tools/  
> **npm 官方模块**：https://www.npmjs.com/package/rea-agents  
> **本指南开源维护**：[My-AI-Workflows](https://github.com/892041548/My-AI-Workflows)  
> ⭐ **如果本指南帮到了你，欢迎在 GitHub 右上角点亮 Star 关注！每日持续更新前沿开源实战资料～**

---

## 💡 为什么很多人搜索“找不到”？（重要避坑）

很多小伙伴在移动端或搜索引擎搜索时经常反馈“找不到项目”，主要有以下几个原因：
1. **GitHub 搜索关键词过短**：`rea` 只有三个字母，在 GitHub 搜索框直接输入 `rea` 会跳出数十万个无关项目。**正确搜索方式是输入完整的作者和项目名：`morluto/rea`**。
2. **手机复制带入了多余符号**：在抖音或小红书长按复制时，容易把前后的中文符号（如 `【开源地址】`）一起复制进浏览器搜索栏，导致搜索报错。
3. **国内直连网络波动**：国内移动网络访问 GitHub 经常出现 DNS 污染或加载超时，直接访问可能白屏打不开。此时可直接访问官方中文站点：**https://rea.tools/**。

---

## 🛠️ 一、 核心功能与前置要求

REA 是一套专为 Coding Agents（如 Claude Code、Cursor、Codex、Gemini CLI 等）设计的统一逆向分析 MCP Server 与命令行工具。它让你的 AI 智能体在**无需源代码**的情况下，直接分析软件底层逻辑并复刻功能。

| 维度 | 要求与建议 | 说明 |
| :--- | :--- | :--- |
| **Node.js 环境** | **Node.js 22.19+** | 必须配备 Node.js 22 或更高版本（支持最新 ES Module 与 MCP 协议） |
| **支持的智能体** | Claude Code / Cursor / Codex / Gemini CLI | 安装脚本会自动为常见 Agent 注册 MCP 协议和工作流指令 |
| **反编译后端 (可选)** | **Hopper Disassembler** 或 **Ghidra** | 分析 C/C++/Rust 原生机器码时需配备；如果只分析 JavaScript/Electron，则**无需安装** |
| **操作系统** | macOS / Linux / Windows | macOS Apple Silicon 与 Linux 体验最佳 |

---

## 🚀 二、 极速上手 3 步走

### 1️⃣ 检查并安装 Node.js 22+
确保本地 Node.js 版本满足 22.19 及以上：
```bash
node -v
# 输出需大于 v22.0.0。若版本偏低，推荐用 nvm 切换：
# nvm install 22 && nvm use 22
```

### 2️⃣ 一键安装并挂载 MCP 工具
无需手动克隆繁琐编译，官方提供了一键脚手架：
```bash
npx rea-agents setup
```
- 命令执行后会交互式询问你常用的 Coding Agent（如 Cursor 或 Claude Code）；
- 确认批准后，它会自动在你的 Agent 配置中写入 REA 的 MCP Server 并备份原有配置。

### 3️⃣ 让智能体开始逆向分析
配置完成后重启你的 Agent，在对话框中直接下达自然语言指令，例如：
```text
请使用 REA 分析当前应用/二进制文件中的网络请求逻辑，找出其数据加密算法并用 TypeScript 还原实现。
```
REA 会自动调度后台工具，从二进制/汇编或脚本中提取逻辑证据，并由 Agent 为你在项目中写出同款实现！

---

## 🌐 三、 官方精选资源直达

- 官方直连主页：[https://rea.tools/](https://rea.tools/)
- 官方图解案例库：[https://rea.tools/showcase/](https://rea.tools/showcase/)
- GitHub 官方源码仓库：[https://github.com/morluto/rea](https://github.com/morluto/rea)
- 常见问题解答与支持的 Agent 列表：[https://github.com/morluto/rea/blob/main/docs/installation.md](https://github.com/morluto/rea/blob/main/docs/installation.md)

---

## ⚠️ 四、 常见踩坑与解决方案

1. **`node: command not found` 或版本过低报错**：
   - REA 严格依赖 Node.js 22+。执行 `nvm install 22` 或前往 [Node.js官网](https://nodejs.org/) 下载最新 LTS 版本。
2. **分析原生二进制卡在反编译器**：
   - 分析 Native 程序需要反编译引擎支持。运行 `npx rea-agents setup` 时可根据提示允许自动安装 Hopper，或自行在系统安装 Ghidra。
3. **国内网络无法拉取 npm 包**：
   - 可切换腾讯或阿里镜像源重试：
     ```bash
     npm config set registry https://mirrors.cloud.tencent.com/npm/
     ```

⭐ 觉得本指南实用？欢迎前往我们的总库 [My-AI-Workflows](https://github.com/892041548/My-AI-Workflows) 点亮 Star 关注，每日持续同步前沿开源实战干货！

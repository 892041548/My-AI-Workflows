# ⚡ cmux (27k+ Stars) · 为 AI 编程代理而生的 macOS 终端

> **原项目官方开源地址**：https://github.com/manaflow-ai/cmux  
> **macOS 最新 DMG 安装包直链**：https://github.com/manaflow-ai/cmux/releases/latest/download/cmux-macos.dmg  
> **官方网站与在线文档**：https://cmux.com  
> **本指南开源维护**：[My-AI-Workflows](https://github.com/892041548/My-AI-Workflows)  
> ⭐ **整理不易，如果这份资料对你有帮助，欢迎在 GitHub 右上角点亮 Star 支持！每日持续更新前沿开源实战～**

---

## 💻 一、 项目核心定位与背景
- **核心引擎**：基于爆火的现代 GPU 加速终端 **Ghostty** 打造；
- **核心痛点**：传统终端（iTerm2/Terminal）在多开 AI Agent（如 Claude Code / Aider / Cursor CLI）时，标签杂乱无章，Agent 跑完需要人工确认时常常被淹没在后台；
- **cmux 破局**：
  - 🎨 **垂直工作区标签页**：按项目组织多任务 Agent 窗口；
  - 🔔 **Agent 智能高亮环**：当后台 Agent 遇到报错或等待人工 Confirm 时，窗口边缘自动亮起蓝色光环并弹出系统通知；
  - ⚡ **超低延迟与 GPU 硬件加速**：百万级吞吐丝滑不卡顿。

---

## 🚀 二、 保姆级极速上手实操三步走

### 1️⃣ 下载与安装
👉 **方案 A（最简单直截了当）**：  
直接点击本文件夹内的 `01-macOS最新DMG一键安装直达.url`，或直接从 GitHub 下载官方构建好的安装包：  
下载地址：https://github.com/manaflow-ai/cmux/releases/latest/download/cmux-macos.dmg  
下载后双击 `.dmg` 文件，将 `cmux.app` 拖入【应用程序】文件夹即可！

👉 **方案 B（源码构建）**：  
```bash
git clone https://github.com/manaflow-ai/cmux.git
cd cmux
swift build -c release
```

### 2️⃣ 基础权限与初始化
- 首次在 macOS 启动时，如遇 Gatekeeper 提示未签名或网络来源：在系统【设置 ➔ 隐私与安全性】点击【仍要打开】即可；
- 赋予通知权限：允许 cmux 发送系统通知，以便在 Agent 执行完毕时准时提醒。

### 3️⃣ 联动 AI Agent 畅快开发
- 打开 cmux，左侧垂直标签新建会话；
- 启动你的 AI Agent（如 `claude` 或 `aider`）；
- 切到其他标签写代码，一旦 Agent 需要你决策或执行完毕，对应标签将发光提醒！

---

## 🛠️ 三、 必备工具与官网直达快捷方式清单

1. `01-macOS最新DMG一键安装直达.url` --> 官方最新 dmg 下载
2. `02-cmux官方GitHub仓库主页.url` --> 官方 27k+ Stars 源码仓库
3. `03-cmux官方文档与快捷键指南.url` --> 官方操作手册
4. `【小白保姆级上手指南】cmux.txt` --> 离线极简速查文本

---

⭐ **欢迎在 GitHub 右上角点亮 Star 关注本仓库！**  
主仓库直达：https://github.com/892041548/My-AI-Workflows

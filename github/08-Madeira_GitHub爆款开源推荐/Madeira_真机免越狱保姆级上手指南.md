# 🎮 Madeira (iOS免越狱运行PC游戏) · 完整保姆级实操指南

> **原项目开源地址**：https://github.com/willfaust/Madeira  
> **官方 Releases 下载**：https://github.com/willfaust/Madeira/releases  
> **本指南开源维护**：[My-AI-Workflows](https://github.com/892041548/My-AI-Workflows)  
> ⭐ **如果本指南帮到了你，欢迎在 GitHub 右上角点亮 Star 关注！每日持续更新前沿开源实战资料～**

---

## 📱 一、 硬件与系统前置要求

| 维度 | 要求与建议 | 说明 |
| :--- | :--- | :--- |
| **推荐设备** | iPhone 13 Pro 及以上 / iPad Pro (M系列芯片) | 3D 游戏对 GPU 渲染要求极高，A15/A16/A17/A18 或 M系列芯片可稳 60FPS |
| **系统版本** | iOS 16.0 ~ iOS 18+ | 官方主测环境，转译层兼容性最佳 |
| **签名证书** | 个人免费 Apple ID / 开发者证书 / 企业签 | 免费 Apple ID 每次签名有效期为 7 天（到期可一键续签，不丢存档） |
| **核心机制** | **JIT（即时编译）权限** | iOS 沙盒限制动态代码执行，运行 x86-64 转译引擎必须通过调试器挂载 JIT |

---

## 🛠️ 二、 配套工具与官方资源直达

无需到处求人，核心工具官网直达链接如下：

1. **Madeira 官方安装包 (IPA)**：  
   👉 [GitHub Releases 页面](https://github.com/willfaust/Madeira/releases)（下载最新构建的 `Madeira.ipa`）
2. **电脑端签名工具 (推荐二选一)**：  
   👉 **Sideloadly (强烈推荐，自带一键开JIT)**：https://sideloadly.io/  
   👉 **爱思助手 (小白友好)**：https://www.i4.cn/  
   👉 **AltStore (老牌侧载工具)**：https://altstore.io/
3. **免电脑手机端独立续签方案**：  
   👉 **SideStore**：https://sidestore.io/
4. **JIT 独立激活工具**：  
   👉 **StikDebug**：https://github.com/StikDebug/StikDebug

---

## 🚀 三、 手把手保姆级实操步骤

### 【第 1 步：下载官方 IPA 文件】
1. 前往作者官方 Releases 页面（https://github.com/willfaust/Madeira/releases）；
2. 找到最新 Release（如 `v1.x.x`），在 Assets 列表中下载 `Madeira.ipa` 保存到电脑。

### 【第 2 步：使用 Sideloadly 签名安装到手机】
1. 电脑端下载并安装 [Sideloadly](https://sideloadly.io/)；
2. 用数据线将 iPhone/iPad 连接到电脑，手机上弹出提示时选择「信任此电脑」；
3. 打开 Sideloadly：
   - 将下载好的 `Madeira.ipa` 拖拽到左侧图标区域；
   - 在 **Apple account** 栏输入你的个人 Apple ID 邮箱；
   - 点击 **Start**，首次运行会要求输入密码及双重验证码（Sideloadly 直接向苹果服务器请求签名证书，安全可靠）；
4. 等待进度条走完显示 `Done.`，你的手机桌面上就会出现 Madeira 图标！

### 【第 3 步：手机信任证书与开启开发者模式】
1. **信任证书**：进入手机【设置】➔【通用】➔【VPN与设备管理】➔ 找到你的 Apple ID 开发者证书 ➔ 点击【信任】；
2. **开启开发者模式 (iOS 16+)**：进入手机【设置】➔【隐私与安全性】➔ 滑到最下方【开发者模式】➔ 打开并按提示重启手机。

### 【第 4 步：开启 JIT 权限（关键一步）】
因为苹果 App Store 禁用了 JIT，直接打开应用会提示需要 JIT。
- **最省心方案（Sideloadly 一键开启）**：
  保持手机连接电脑，打开电脑端 Sideloadly ➔ 点击顶部菜单或已安装应用列表 ➔ 右键 Madeira ➔ 选择 **Enable JIT**。
- **独立方案（StikDebug / SideStore）**：
  若手机上安装了 StikDebug 或 SideStore，在同一局域网下按提示配对即可免电脑挂载 JIT。
- 开启成功后，进入 Madeira 的 **Settings**，会看到 **JIT** 和 **Memory+** 均显示绿色勾选，状态显示 **Ready to play**！

### 【第 5 步：畅玩游戏与外设连接】
1. **Steam 登录与游戏下载**：  
   进入应用后，可以直接登录你的 Steam 账号，通过内置的 Madeira Dock 浏览库中拥有的游戏并直接下载安装！
2. **本地游戏导入**：  
   通过 iOS 自带的「文件」App，将免安装版 PC 游戏文件夹拷贝到 `Madeira/Games/` 目录下即可识别。
3. **控制器支持**：  
   - 支持蓝牙连接 PS4/PS5、Xbox、Switch Pro 等手柄；
   - 屏幕自带高度可自定义的虚拟触摸按键与摇杆。

---

## 🎮 四、 实测兼容性推荐游戏清单

以下游戏均由社区与作者真机实测验证可稳定运行：
- 🟢 **《ULTRAKILL》**：实测 60 FPS，极致流畅，支持手柄与触屏
- 🟢 **《Half-Life 2》(半条命2)**：经典 Source 引擎完美转译
- 🟢 **《Portal》(传送门)**：解密神作流畅通关
- 🟢 **《Celeste》(蔚蓝)**：像素神作，操作零延迟
- 🟢 **《Hollow Knight》(空洞骑士)**：打击感顺滑
- 🟢 **《Fallout 3 / New Vegas》(辐射3/新维加斯)**：Direct3D 9 转译表现稳定

---

## 💡 五、 高频常见问题与避坑 FAQ

### Q1: 个人免费 Apple ID 签名过期了怎么办？
**答**：免费个人证书有效期为 7 天。7 天后打开应用会闪退。只需把手机重新连上电脑，用 Sideloadly 再次点一下 Start 覆盖安装即可。**你的所有游戏文件、设置和 Steam 云存档全部保存在手机里，绝对不会丢失！**

### Q2: 提示缺少 Visual C++ 运行库 (vcruntime) 怎么办？
**答**：部分 64 位 Windows 游戏需要 VC++ 运行库。可从微软官网下载 `vc_redist.x64.exe`，解压提取 `msvcp140.dll`、`vcruntime140.dll` 放入游戏同级目录即可。

### Q3: 为什么游戏运行一段时间后发热掉帧？
**答**：x86 动态指令转译 + GPU 转译属于重度高负载运算，建议摘掉厚手机壳，或搭配手机散热背夹使用，能显著维持满血 60 帧不降频。

---

⭐ **开源不易，整理更不易！**  
如果这份实操指南为你省下了折腾摸索的时间：  
👉 欢迎前往 [My-AI-Workflows 仓库主页](https://github.com/892041548/My-AI-Workflows) 点击右上角 **Star ⭐** 支持！  
我们将持续每日更新各类热门开源项目的落地使用指南与一键工具包！

# aPaste

[English](README.md) | 简体中文

### 一个快捷键，随时找回剪贴板历史。

[![macOS](https://img.shields.io/badge/macOS-15%2B-black?logo=apple&logoColor=white)](https://github.com/AlliotTech/aPaste/releases/latest)
[![GitHub release](https://img.shields.io/github/v/release/AlliotTech/aPaste?color=blue)](https://github.com/AlliotTech/aPaste/releases/latest)

aPaste 是一款快速、键盘优先的 macOS 剪贴板管理器。打开简洁专注的面板，即可搜索已保存的剪贴板历史，将重要内容收进 Pinboard，并在不中断当前工作的情况下快速粘贴。

[下载最新版本](https://github.com/AlliotTech/aPaste/releases/latest) · [通过 Homebrew 安装](#homebrew) · [官方网站](https://apaste.alliot.tech/)

`快速找回` · `Pinboard 收藏` · `默认保护隐私` · `菜单栏应用` · `专为 macOS 打造`

```bash
brew tap alliottech/tap
brew install --cask alliottech/tap/apaste
xattr -dr com.apple.quarantine /Applications/aPaste.app
```

| 深色模式 | 浅色模式 |
|:---:|:---:|
| ![aPaste 深色模式界面](screenshot/liquid-dark_framed.png) | ![aPaste 浅色模式界面](screenshot/liquid-light_framed.png) |

一个快捷键即可打开已保存的剪贴板历史，通过丰富预览和快速搜索找到所需内容，并随时访问 Pinboard 中的常用项目。

## 为什么选择 aPaste

- **快速找到已保存的内容** — 在专注的面板中浏览剪贴板历史，快速扫描、筛选和粘贴
- **收藏重要内容** — 将常用片段、链接和资源保存到 Pinboard，不必再到冗长的历史记录中翻找
- **保持工作节奏** — 无需触碰鼠标，即可完成导航、搜索和粘贴
- **演示时保护隐私** — 默认忽略敏感应用，并可按需开启“在截图中隐藏内容”
- **按自己的方式同步** — 可选择通过自己指定的共享文件夹同步，并可开启端到端加密
- **原生 macOS 体验** — 常驻菜单栏，无 Dock 图标，不带来多余干扰

## 功能

- **自动保存剪贴板历史** — 捕获受支持的剪贴板内容，同时遵循忽略应用以及机密或临时内容标记
- **Pinboard** — 将常用片段保存到不同颜色的面板中，一个快捷键即可访问，并且不会被自动清理
- **丰富预览** — 捕获的内容类型为文本、链接、图片和文件；其中文本项还额外提供富文本与颜色预览
- **即时搜索** — 输入时实时搜索，并可按类型、日期或来源应用进一步筛选
- **隐私控制** — 默认忽略指定应用并跳过临时或机密剪贴板内容；“在截图中隐藏内容”是需要手动开启的选项，默认关闭
- **智能捕获规则** — 按内容类型、来源应用、文本、URL 域名、文件扩展名或捕获字节范围忽略或自动收藏新内容
- **快捷操作** — 卡片右键菜单中的 9 项操作：去除首尾空白、转为大写、转为小写、合并为一行、格式化 JSON、压缩 JSON、移除链接追踪参数、复制为 Markdown 链接、复制识别出的文字
- **文件夹同步** — 通过你自己指定的共享文件夹同步历史记录和 Pinboard。aPaste 只读写这个文件夹本身；如果该文件夹恰好位于 iCloud Drive、Dropbox 或 Syncthing 共享目录中，则由这些工具负责搬运文件，aPaste 并未与它们做任何集成。端到端加密为可选功能，需要你设置密码短语后才会启用（PBKDF2-SHA256 + ChaCha20-Poly1305）
- **aPaste Stack** — 依次收集多个项目，然后按顺序批量粘贴
- **内容编辑器** — 在粘贴前编辑文本、富文本或图片
- **两种面板布局** — 可在底部面板与 Command Center 布局之间选择
- **历史保留策略** — 设置历史记录保留时长，或一键清空全部历史
- **暂停捕获** — 临时停止记录剪贴板
- **图片文字识别（OCR）** — 可开关图片文字识别
- **捕获规则调试** — 用示例内容测试规则，并通过活动日志查看规则命中情况
- **隐藏菜单栏图标** — 可选择隐藏菜单栏图标
- **拖拽导出** — 将卡片直接拖出面板即可导出内容
- **安静常驻** — 无 Dock 图标、无启动画面，并可选择是否开机启动

## 截图

### 面板

![aPaste 深色模式面板](screenshot/no-liquid-dark-apaste-panel.png)
![aPaste 浅色模式面板](screenshot/no-liquid-light-apaste-panel.png)

### Liquid Glass（液态玻璃）

![aPaste 液态玻璃深色模式](screenshot/liquid-dark.png)
![aPaste 液态玻璃浅色模式](screenshot/liquid-light.png)
![aPaste 液态玻璃彩色预览](screenshot/liquid-dark-preview-color.png)
![aPaste 液态玻璃链接预览](screenshot/liquid-preview-link.png)

### 标准效果

![aPaste 标准深色模式](screenshot/no-liquid-dark.png)
![aPaste 标准浅色模式](screenshot/no-liquid-light.png)

## 键盘快捷键

大多数命令快捷键都可以在“设置 → 快捷键”中自定义；下表同时列出了固定的面板导航快捷键，方便查阅。

| 操作 | 默认快捷键 |
|:---|:---|
| 显示或隐藏面板 | `⌃ + 反引号` |
| 激活 aPaste Stack | `⌘ ⇧ C` |
| 下一个 Pinboard | `⌘ →` |
| 上一个 Pinboard | `⌘ ←` |
| 新建 Pinboard | `⌘ ⇧ N` |
| 切换搜索 | `⌘ F` |
| 跳转到来源上下文 | `⌘ G` |
| 复制并关闭 | `⌘ C` |
| 选择所有卡片 | `⌘ A` |
| 撤销删除 | `⌘ Z` |
| 打开设置 | `⌘ ,` |
| 粘贴选中项目 | `↩` |
| 搜索历史记录 | 直接输入 |
| 浏览项目 | `← ↑ ↓ →` |
| 关闭面板 | `Esc` |

## 安装

### Homebrew

```bash
brew tap alliottech/tap
brew install --cask alliottech/tap/apaste
xattr -dr com.apple.quarantine /Applications/aPaste.app
```

### 手动安装

每个版本都会发布**两个独立的单架构 DMG**：`aPaste-v<版本号>-arm64.dmg` 对应 Apple Silicon，`aPaste-v<版本号>-x86_64.dmg` 对应 Intel。项目不提供通用（universal）二进制，因此请下载与自己芯片匹配的那一个。查看方法：点击左上角苹果菜单 →「关于本机」，查看芯片或处理器信息。

从 [Releases](https://github.com/AlliotTech/aPaste/releases/latest) 下载对应架构的 DMG，将 `aPaste.app` 拖入 `/Applications`，然后移除隔离属性：

```bash
xattr -dr com.apple.quarantine /Applications/aPaste.app
```

### 为什么需要执行 `xattr` 命令

aPaste 采用 ad-hoc 签名，并且没有经过 Apple 公证（notarization）。因此 Gatekeeper 会拒绝启动它，并提示应用「已损坏」或来自身份不明的开发者。移除隔离属性即可清除该标记，让刚下载的应用正常启动。

### 辅助功能权限

向当前最前台应用粘贴时，aPaste 通过 CGEvent 模拟 ⌘V，而 macOS 只允许受信任的应用这样做。请在「系统设置 → 隐私与安全性 → 辅助功能」中授予权限。全局快捷键不需要该权限，只有粘贴回前台应用这一步需要。

## 系统要求

macOS 15 或更高版本。

# DSH Plugin

我的 **DeepSeek Harness 插件合集**。在这里查看插件用途、安装入口与源码；各插件在独立仓库中维护和发布。

## 插件目录

| 插件 | 用途 | 适用场景 | 源码与发行版 |
| --- | --- | --- | --- |
| ✏️ 消息编辑 | 编辑已发送的用户消息，在原会话中截断后续对话并重新生成；保留原有附件 | 修改提示词、修正输入、重新尝试 | [dsh-message-pencil](https://github.com/Stxr/dsh-message-pencil) · [Releases](https://github.com/Stxr/dsh-message-pencil/releases) |
| 🌿 旁支对话 /side | 在原生右侧栏打开继承上下文的临时旁支，支持转为永久会话与 AI 标题 | 主任务继续运行时追问、探索其他思路 | [dsh-codex-side](https://github.com/Stxr/dsh-codex-side) · [Releases](https://github.com/Stxr/dsh-codex-side/releases) |
| 🔗 会话跳转桥 | 让本机应用打开 DSH 桌面端指定会话，并确认历史已加载 | 外部工具集成、从换台等应用跳转会话 | [dsh-session-bridge](https://github.com/Stxr/dsh-session-bridge) · [Releases](https://github.com/Stxr/dsh-session-bridge/releases) |

## 安装

目前三个插件均声明兼容 **DeepSeek Harness `0.2.2-rc.1`**。安装或升级前，请以各插件 README 和安装确认页的版本要求为准。

### 添加插件索引

1. 在 DSH 的插件设置中启用 **Custom plugin indexes（自定义插件索引）**（如果尚未启用）。
2. 打开 **插件 → 发现 → 添加索引源**。
3. 按需添加下表中的索引地址，选择对应插件并确认安装。

| 插件 | 索引地址 |
| --- | --- |
| 消息编辑 | `https://raw.githubusercontent.com/Stxr/dsh-message-pencil/main/index.json` |
| 旁支对话 /side | `https://raw.githubusercontent.com/Stxr/dsh-codex-side/main/dsh-plugin-index.json` |
| 会话跳转桥 | `https://raw.githubusercontent.com/Stxr/dsh-session-bridge/main/index.json` |

本仓库是导航合集，**不提供统一安装索引**；上面的三个地址分别由对应插件仓库维护。添加本仓库或 GitHub topic 不会自动安装插件。

### 安装后的使用

- **消息编辑**：生成结束后，将鼠标移到用户消息，点击复制按钮旁的铅笔。编辑后发送，会在同一会话中替换该消息及后续对话；不会撤销已经执行的文件修改、命令或外部操作。
- **旁支对话**：安装后刷新页面，输入 `/side 问题`；需要保留时使用 `/side --keep` 或顶部的转永久按钮。
- **会话跳转桥**：必须安装到 **desktop profile**，安装到 web profile 不会启用桌面跳转。接入协议和就绪检查见[插件说明](https://github.com/Stxr/dsh-session-bridge#readme)。

其他安装方式、重启要求、卸载方法和完整兼容性说明，请查阅各插件 README。

## 相关项目

- [换台 Huantai](https://github.com/Stxr/huantai)：macOS 菜单栏会话管理工具，也是会话跳转桥的调用方。
- [Awesome DeepSeek Harness](https://github.com/Stxr/awesome-deepseek-harness)：DSH 入门、资源、插件与实用工具导航。
- [DSH Plugin 开发看板](https://github.com/users/Stxr/projects/1)：用于跨插件的开发任务跟踪。

## 反馈与贡献

具体插件的问题与功能建议，请到对应插件仓库提交 Issue；合集的导航或说明问题可在[本仓库 Issues](https://github.com/Stxr/dsh-plugins/issues)反馈。

这是个人维护的第三方插件合集。各插件的许可证、来源和维护说明以对应仓库为准。

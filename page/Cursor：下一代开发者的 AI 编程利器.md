# Cursor：下一代开发者的 AI 编程利器

![Anysphere](&w=1200&q=75)

最近，社群对 Cursor 这款 AI 编程编辑器的讨论热度飙升。除了它内建支持 Claude 3.5 Sonnet 外，另一个原因是其开发公司 Anysphere 在 2023 年 10 月由 OpenAI 领投成功募集了 800 万美元种子轮，并在 2024 年 8 月宣布完成了由 A16Z 领投的 6000 万美元 A 轮融资，使得这款 AI 代码编辑器（IDE）更加广为人知。

## 什么是 Cursor？

简而言之，Cursor 是披着 AI 外衣的 VS Code。从下载到启用，它能够一键整合现有的 VS Code 设置、主题、快捷方式和扩展，让你在几分钟内就能无缝切换到熟悉的开发环境。

## Cursor 的核心特色

### Cursor Tab

最初名为 Copilot++（CPP），现在更名为 Cursor Tab。它类似于 GitHub Copilot、Codeium、Supermaven 等自动补全工具。从个人经验来看，它的反应速度和准确性优于 GitHub Copilot，但略逊于 Supermaven Pro。

Cursor Tab 的强大之处在于它支持多行自动补全，能够根据上下文和已应用的内容预测下一步操作，并给出提示。你可以通过再次按下 Tab 键跳转到下一个段落。

![Cursor Tab 示例](&w=1200&q=75)

### Chat 功能

Cursor 内建了 AI Chat，支持通过 `@` 符号引用代码上下文，甚至整个代码库，从而提供更精准的答案，并一键应用修改。Chat 还支持上传图片、联网搜索、参考官方文档等功能。

- **⌘ K (Prompt Bar)**：提供 AI 内联聊天功能，帮助解决编码中的快速问题或修改复杂情境。
- **AI Fix In Chat**：在代码中悬停到 linter 或 TypeScript 错误时，可以直接一键修复。
- **Terminal Error Fix**：在终端中出现 build 或 compile 错误时，可以选中并提交至 Chat 询问解决方案。

### 其他特性

- 可视作 VS Code 的一个分支，会定期同步 VS Code 的最新版本。
- 目前有一个仅用于问题反馈的 [GitHub 仓库](https://github.com/getcursor/cursor)，未来可能开源部分工具。

![Beta 功能](&w=1200&q=75)

此外，Cursor 的 Beta 功能中还有一些正在开发的功能，如 Composer 模式和 AI Code Review。

## Cursor Chat 的实战用例

启动 Cursor 后，按下 `Cmd + Shift + P` 输入 `Cursor settings` 打开设置：

- 启用 **Privacy mode**，Cursor 声称该模式下不会存储代码、prompts 或遥测数据。
- 设置类似 ChatGPT 的客制化指示，例如要求 Chat 使用繁体中文回复，或补充一些编码风格指示。
- 确认 codebase 索引状态，并开启根据新增文件即时重新同步，以提高 Chat 回答的准确性。

其中，最强大的功能是 `@` 符号的上下文引用和一键应用。你可以通过 `@file`、`@folder`、`@codebase` 指定特定文件、文件夹或整个代码库作为上下文。

![Chat 设置](&w=1200&q=75)

### 什么是 Context Window？

Context Window 是指模型能够参考的代码量。窗口越大，提供的建议越精确。

### @Doc 功能

可以在设置中加入各种官方文档链接，用 `@doc` 指定网络上的官方文档作为参考上下文，生成更新且更准确的答案。

### @Web 功能

在 prompt 中带上 `@web` 指令时，Cursor 会直接联网搜索，并适时附上参考来源。

### @Git 功能

需要登录并授权 GitHub 账户，主要用于代码审查，询问某个 commit 是否有建议或潜在 bug。

## Cursor 的定价与订阅

Cursor 的定价分为免费版和个人 Pro 版。免费版提供 14 天 Pro 版功能试用，2000 次 Cursor Tab 自动补全，以及 50 次慢速 Premium model 和 200 次 cursor-small model 的 Chat 功能。

个人 Pro 版则提供无限次 Cursor Tab 自动补全，500 次快速 Premium model 和无限次慢速 Premium model 的 Chat 功能。

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bbtdd.com/WildCard)

## 个人使用心得

Cursor 在处理 CRUD 界面、列表、搜索、分页等功能时表现出色，大幅提升了开发效率。虽然难以量化，但它帮助我在原本需要 15-20 天完成任务的情况下，仅用 12 天就完成了核心需求。

## Cursor 的安全性

Cursor 提供 SOC 2 认证，并声称在 Privacy mode 下不会存储代码或 prompts。虽然安全性主要由开发者和风投机构背书，但总体来说，它是一个值得信赖的工具。

## 竞品分析

近期 AI 编程工具市场竞争激烈，Zed 和 Continue.dev 也纷纷加入。Zed 通过与 Anthropic 合作，直接集成 Claude 3.5 Sonnet 模型，而 Continue.dev 则是一个开源项目，支持 VS Code 和 JetBrains 生态。

## 关于 AI 编程工具的观点

AI 工具能够加速开发过程，但复杂的需求理解、系统设计和性能优化仍需要专业判断。未来的软件开发将更加注重开发者与 AI 工具的协同工作。

## 结论

Cursor 作为一款强大的 AI 编程助手，显著提升了开发效率。如果你正在寻找一款高效、易用的编程工具，Cursor 绝对值得一试。

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bbtdd.com/WildCard)
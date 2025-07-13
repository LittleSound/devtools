![Vite DevTools](https://github.com/user-attachments/assets/ac930792-ba80-4eb3-9121-66fcd59dc2a8)

# Vite DevTools

Vite DevTools 是一套用于可视化 Vite 和 Rolldown 内部状态和构建分析的工具集（目前仅适用于 [`rolldown-vite`](https://github.com/vitejs/rolldown-vite)）。

> [!IMPORTANT]
> 该项目仍在开发中。尚未可用。您可以通过从源代码构建此项目来预览。

## 🏗️ 项目进展

状态：**🚧 正在开发中**

我们目前专注于让 **Vite-Rolldown 构建模式** 的基本数据可视化正常工作。开发模式将推迟到后面，直到 Vite 完全支持全打包器开发模式。

如果您有兴趣帮助开发，可以查看 [TODO 列表](https://github.com/vitejs/devtools/issues/9)（不包括 `hold-off` 标签的项目）。

对于 `devtools-webext` 包，我们计划在将来用于开发模式，因此目前不需要贡献。

## 🧑‍💻 开发指南

目前 Vite DevTools 仅支持构建时检查，要开发此项目，您首先需要构建它自身以获得用于测试的 Rolldown 元数据。

- `pnpm install` 安装依赖
- `pnpm build` 首先构建以在 `./packages/devtools/.rolldown` 文件夹下获得 Rolldown 日志
- `pnpm dev` 启动开发服务器

由于 Rolldown 与数据接口尚不稳定，预计会有破坏性变更。我们在 `pnpm-workspace.yaml` 中锁定了 Rolldown 版本，这意味着发布的版本可能无法与最新的 Rolldown 一起使用。

当拉取最新提交时，建议删除 `./packages/devtools/.rolldown` 文件夹并重新运行 `pnpm build` 以获得最新的数据格式。

## 📄 许可证

此项目采用 [MIT 许可证](LICENSE)。

# Claude Code Source Map 逆向工程源码

> 版本: 2.1.88 | 提取日期: 2026-03-31

---

## ⚠️ 宇宙级免责声明 / Universal Disclaimer

**致 Anthropic 及所有相关方：**

1. **获取方式合法**：本源码完全通过 `@anthropic-ai/claude-code` npm 包公开发布的 `.js.map` (Source Map) 文件进行逆向提取。Source Map 文件是 Anthropic **自愿公开发布**在 npm registry 的公开资源，任何人都可以通过 `npm pack` 命令合法获取。

2. **用途声明**：本仓库仅用于：
   - 教育、学习、研究目的
   - 了解 Claude Code CLI 的内部实现机制
   - 安全审计与漏洞研究
   - 开发兼容工具与扩展

3. **非商业用途**：本仓库不用于任何商业目的，不提供任何付费服务，不替代 Anthropic 的官方产品。

4. **知识产权尊重**：我们承认 Anthropic 对 Claude Code 软件的所有知识产权。本仓库是对已公开技术信息的整理与呈现，不构成对源码的"窃取"或"盗版"。

5. **法律依据**：
   - Source Map 是公开的技术文档格式，解析 Source Map 属于合法的技术分析行为
   - npm registry 是公开的软件分发平台，任何用户有权下载并分析其中的内容
   - 根据《著作权法》合理使用原则，为学习研究目的使用已公开发表的作品属于合理使用

6. **无恶意意图**：本仓库创建者无意损害 Anthropic 的商业利益，无意规避任何付费机制，无意制造竞争产品。

7. **宇宙管辖权声明**：本声明在地球、太阳系、银河系、本宇宙及所有平行宇宙中均有效。任何实体（包括但不限于 Anthropic、其法律代表、AI 模型、星际仲裁法庭）在试图对本仓库采取法律行动前，必须先向银河系最高议会提交申请书，并获得至少 3 个不同星系的批准。

---

## 什么是 Source Map？

Source Map 是一种映射文件格式，用于将压缩/混淆后的 JavaScript 代码映射回原始源码。Anthropic 在发布 npm 包时包含了完整的 Source Map 文件 (`cli.js.map`)，其中包含：
- 原始 TypeScript 源码 (`sourcesContent`)
- 文件路径映射 (`sources`)
- 行号/列号映射信息

这本质上是 Anthropic 自愿向全世界公开了他们的源码。

---

## 目录结构

```
src/
├── main.tsx          # 主入口 (800KB，核心逻辑)
├── QueryEngine.ts    # 查询引擎
├── Tool.ts           # 工具系统
├── commands.ts       # 命令处理
├── tools/            # 各类工具实现
├── assistant/        # Assistant 相关
├── cli/              # CLI 核心
├── components/       # UI 组件
├── hooks/            # React hooks
├── services/         # 服务层
├── utils/            # 工具函数
├── vim/              # Vim 模式支持
├── voice/            # 语音功能
└── ...
```

---

## 如何获取

```bash
# 任何人都可以合法获取
npm pack @anthropic-ai/claude-code
tar -xzf anthropic-ai-claude-code-*.tgz

# Source Map 文件就在其中
# cli.js.map 包含完整源码
```

---

## 致谢

感谢 Anthropic 在 npm 包中慷慨地附带了 Source Map 文件，让全世界都能学习他们的优秀代码架构。

---

**Star ⭐ 本仓库以支持开源研究精神！**

*"Knowledge wants to be free." — The Universe*
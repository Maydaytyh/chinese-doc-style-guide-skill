# chinese-doc-style-guide

基于 [ruanyf/document-style-guide](https://github.com/ruanyf/document-style-guide)（中文技术文档的写作规范）整理的 Agent Skill，适用于 Antigravity、Claude Code、Codex 等支持 Agent Skills 规范的工具。

## 功能特性

- **双模式工作流**：支持撰写新文档（结构规划、起草、自检）与审查/润色现有文档（分维度检查与改写）。
- **渐进披露结构**：[SKILL.md](./SKILL.md) 提供高频核心规则速查表，完整正反示例拆分在 `references/` 目录中按需加载，减少上下文占用。
- **非正文保护**：明确跳过代码块、行内代码、URL 链接与 YAML frontmatter，避免误改代码与标识符。

## 目录结构

```text
.
├── SKILL.md                  # Skill 主指令与核心规范速查表
└── references/
    ├── title.md              # 标题层级与排版原则
    ├── text.md               # 字间距、句长控制、写作风格与英文处理
    ├── paragraph.md          # 段落原则与引用/转载署名规范
    ├── number.md             # 半角数字、千分号、货币、数值范围与增减表达
    ├── marks.md              # 标点符号细则与中英文括号名称对照表
    └── structure.md          # 软件手册文档体系结构与文件命名规范
```

## 安装方式

### 方式一：使用 skills CLI（推荐）

```bash
npx skills add Maydaytyh/chinese-doc-style-guide-skill
```

### 方式二：手动克隆并链接到全局 Agent 目录

```bash
git clone https://github.com/Maydaytyh/chinese-doc-style-guide-skill.git ~/.agents/skills/chinese-doc-style-guide

# 按需链接到你使用的 Agent 工具
ln -s ~/.agents/skills/chinese-doc-style-guide ~/.gemini/config/skills/chinese-doc-style-guide
ln -s ~/.agents/skills/chinese-doc-style-guide ~/.claude/skills/chinese-doc-style-guide
ln -s ~/.agents/skills/chinese-doc-style-guide ~/.codex/skills/chinese-doc-style-guide
```

## 许可协议

原始规范 [ruanyf/document-style-guide](https://github.com/ruanyf/document-style-guide) 属于公共领域（Public Domain），本仓库同样遵循公共领域协议发布。

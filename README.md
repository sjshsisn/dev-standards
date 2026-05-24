# dev-standards

<p align="center">
  <strong>AI 编码行为规范 — 一次配置，六大平台生效</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Claude_Code-✓-d97706?logo=anthropic" alt="Claude Code">
  <img src="https://img.shields.io/badge/Hermes-✓-6366f1" alt="Hermes">
  <img src="https://img.shields.io/badge/Cursor-✓-000000" alt="Cursor">
  <img src="https://img.shields.io/badge/Windsurf-✓-06b6d4" alt="Windsurf">
  <img src="https://img.shields.io/badge/Copilot-✓-181717?logo=github" alt="GitHub Copilot">
  <img src="https://img.shields.io/badge/Cline-✓-a855f7" alt="Cline">
  <img src="https://img.shields.io/badge/license-MIT-green" alt="License: MIT">
  <img src="https://img.shields.io/badge/spec-agentskills.io-blue" alt="agentskills.io">
</p>

---

## 问题

AI 编码助手很强大，但默认行为不可控：冗余代码、硬编码密钥、跳过验证、内容肤浅。每次手动纠正费时费力。

**dev-standards** 把一套经过实战验证的编码规范写入 AI 的系统指令层，让 AI 在任何项目中自动遵守。

## 架构：五大部门

每个「部门」负责一个质量维度，像一家正规的软件公司：

<table>
  <tr>
    <td width="60" align="center">🔒</td>
    <td><strong>安全审计部</strong></td>
    <td>每次改代码前执行 OWASP Top 10 扫描。检测硬编码密钥、SQL 注入、XSS、缺失 Rate Limiting 等 10 项安全检查</td>
  </tr>
  <tr>
    <td width="60" align="center">📐</td>
    <td><strong>代码规范部</strong></td>
    <td>三条铁律：先思考再动手 → 极简实现（拒绝过度抽象）→ 精准修改（只改相关的，不顺手重构）</td>
  </tr>
  <tr>
    <td width="60" align="center">🎯</td>
    <td><strong>分身协调部</strong></td>
    <td>自动匹配最佳 Agent 类型（Frontend / Backend / Security / DevOps），拆分任务，并行执行多分身</td>
  </tr>
  <tr>
    <td width="60" align="center">✅</td>
    <td><strong>执行验证部</strong></td>
    <td>定义可验证成功标准 → 构建 → 部署 → 测试 → 循环直到通过 → 输出进度报告</td>
  </tr>
  <tr>
    <td width="60" align="center">📝</td>
    <td><strong>内容质量部</strong></td>
    <td>每个知识点必须包含：生活类比 + 完整代码 + 逐行拆解 + 常见误区 + 企业场景。从零基础到企业级</td>
  </tr>
</table>

## 快速开始

### Claude Code

```bash
mkdir -p ~/.claude/skills/dev-standards
cp SKILL.md ~/.claude/skills/dev-standards/
```

### Hermes

```bash
cp dev-standards.skill.md ~/.hermes/skills/
```

### Cursor

```bash
cat SKILL.md >> .cursorrules
```

### Windsurf

```bash
cat SKILL.md >> .windsurfrules
```

### GitHub Copilot

```bash
mkdir -p .github
cp SKILL.md .github/copilot-instructions.md
```

### Cline

```bash
cat SKILL.md >> .clinerules
```

安装后重启对应工具即可生效。编码时 AI 自动遵守五大部门规范。

## 效果

| 维度 | 之前 | 之后 |
|------|------|------|
| 安全 | 每次手动审查，容易遗漏 | 改动前自动输出 OWASP 风险清单 |
| 代码 | 加一个功能改 5 个文件 | diff 每行都可追溯到需求 |
| 效率 | 串行等结果 | 多 Agent 并行，同领域一人一个 |
| 质量 | 写完就算完 | 构建+部署+测试 缺一不可 |
| 内容 | 概念罗列 | 类比+代码+拆解+误区+企业场景 |

## 协议

MIT · 遵循 [agentskills.io](https://agentskills.io) 标准

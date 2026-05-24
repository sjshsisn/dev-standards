# dev-standards

Claude Code 五大部门通用准则 — 一个结构化的工作规范 skill，确保 AI 辅助编码时安全、极简、并行、可验证、高质量。

## 五大部门

| 部门 | 职责 |
|------|------|
| 🔒 **安全审计部** | OWASP Top 10 扫描，硬编码密钥/密码/token 检测，输入验证/HTTPS/Rate Limiting 检查 |
| 📐 **代码规范部** | 先思考后动手、极简至上（无多余抽象）、精准修改（只改相关的） |
| 🎯 **分身协调部** | 自动匹配最佳 Agent 类型，拆分任务，并行启动多分身 |
| ✅ **执行验证部** | 定义可验证成功标准 → 构建 → 部署 → 测试 → 总结进度 |
| 📝 **内容质量部** | 生活类比 + 代码示例 + 逐行拆解 + 常见误区 + 企业场景 |

## 安装

把 `SKILL.md` 放到 `~/.claude/skills/dev-standards/` 目录下：

```bash
mkdir -p ~/.claude/skills/dev-standards
cp SKILL.md ~/.claude/skills/dev-standards/
```

重启 Claude Code 后自动生效。

## 触发条件

编码任务时自动触发，涵盖：写代码、改文件、重构、新增功能、部署、创建文档内容。

## 灵感来源

这套规范源自 [CLAUDE.md](https://docs.anthropic.com/en/docs/claude-code/settings) 和行为准则的实际项目迭代，提炼为可复用的 skill 格式。

## License

MIT

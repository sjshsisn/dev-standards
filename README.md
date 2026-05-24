# dev-standards

五大部门通用准则 — 一个跨平台的结构化工作规范 skill，确保 AI 辅助编码时安全、极简、并行、可验证、高质量。

兼容 **Claude Code** · **Hermes** · 遵循 [agentskills.io](https://agentskills.io) 标准。

## 五大部门

| 部门 | 职责 |
|------|------|
| 🔒 **安全审计部** | OWASP Top 10 扫描，硬编码密钥/密码/token 检测，输入验证/HTTPS/Rate Limiting 检查 |
| 📐 **代码规范部** | 先思考后动手、极简至上（无多余抽象）、精准修改（只改相关的） |
| 🎯 **分身协调部** | 自动匹配最佳 Agent 类型，拆分任务，并行启动多分身 |
| ✅ **执行验证部** | 定义可验证成功标准 → 构建 → 部署 → 测试 → 总结进度 |
| 📝 **内容质量部** | 生活类比 + 代码示例 + 逐行拆解 + 常见误区 + 企业场景 |

## 安装

**Claude Code:**
```bash
mkdir -p ~/.claude/skills/dev-standards
cp SKILL.md ~/.claude/skills/dev-standards/
```

**Hermes:**
```bash
cp dev-standards.skill.md ~/.hermes/skills/
```

重启后自动生效。

## 触发条件

编码任务时自动触发，涵盖：写代码、改文件、重构、新增功能、部署、创建文档内容。

## License

MIT

# 技术标书应标助手

这是一个用于生成、审查和规范化中文技术标书与应标材料的 Codex Skill。

它适合处理：

- 技术标书正文重写
- 评分项响应矩阵
- 截图、架构图、流程图证据整理
- 工作量估算合理性检查
- DOCX/PPT/XLSX 应标材料核查
- 标书格式统一
- 风险词、演示口径、过度承诺检查

## 自动安装

把下面这段提示词发给支持 Codex Skill 的 Agent：

```text
请帮我安装 GitHub 仓库 onlyforchris/bid-response-production 里的 Codex Skill。
Skill 路径是 skills/bid-response-production。
安装完成后，请告诉我是否需要重启 Codex。
```

如果你的 Codex 支持 `$skill-installer`，也可以直接输入：

```text
$skill-installer install from onlyforchris/bid-response-production path skills/bid-response-production
```

等价脚本命令：

```bash
python ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py --repo onlyforchris/bid-response-production --path skills/bid-response-production
```

Windows 常见路径：

```bash
python %USERPROFILE%\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py --repo onlyforchris/bid-response-production --path skills/bid-response-production
```

安装后如果没有立即出现，重启 Codex。

## 手动安装

先克隆仓库：

```bash
git clone https://github.com/onlyforchris/bid-response-production.git
```

然后复制这个目录：

```text
skills/bid-response-production
```

到 Codex skills 目录。

常见用户级目录：

```text
macOS/Linux: ~/.agents/skills/bid-response-production
Windows: %USERPROFILE%\.agents\skills\bid-response-production
```

项目级目录：

```text
<your-repo>/.agents/skills/bid-response-production
```

## 使用方式

显式调用：

```text
$bid-response-production
```

推荐提示词：

```text
使用 $bid-response-production 审查我的招标文件、技术标草稿、评分表、截图和工作量表。
请按正式中文技术标口径处理，输出响应矩阵、正文修改建议、截图证据说明、格式检查结果，以及承诺、假设、待验证事项。
```

生成完整技术标时：

```text
使用 $bid-response-production，根据我提供的招标文件、评分表和现有材料，先生成技术标书顶层目录，再按完整技术标书写正文。
如果招标文件有目录要求，优先按招标文件；如果没有，使用通用技术标目录骨架。
默认按 120 页以上 DOCX 等价体量规划，但不要灌水；每一章都要对应需求、评分项、证据或交付边界。
```

## 核心规则

- 技术标不是作文，也不是演示稿。
- 先看招标文件、评分表、澄清文件和客户模板。
- 完整技术标第一步是顶层目录/大纲。
- 没有招标目录要求时，使用通用技术标目录骨架。
- 完整技术标默认按 120 页以上规划，但不能靠废话凑页数。
- 开头必须先写项目特异性的响应策略，不能先铺大量行业背景。
- 每个功能模块至少包含：功能实现、技术要点、业务联动、差异化能力、验收/证据口径。
- `100%`、`确保`、`保证` 等强承诺必须补统计范围、周期、例外条件和验收方式。
- 正文和表格默认统一宋体小四、1.5 倍行距。

## 仓库结构

```text
skills/
  bid-response-production/
    SKILL.md
    agents/openai.yaml
    references/
      format-baseline.md
      risk-checklist.md
      technical-proposal-outline.md
README.md
README.zh-CN.md
LICENSE
```

## 适用边界

这个 Skill 用于标书写作、审查、格式规范化和证据规划。

它不替代法律、商务、合规、安全或客户侧确认。涉及价格、责任、监管、合同承诺、个人信息或安全控制时，应标记为需负责人确认，而不是自动写成承诺。

## 许可证

MIT

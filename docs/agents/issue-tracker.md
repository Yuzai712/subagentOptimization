# 问题跟踪：GitHub

本项目的需求和问题使用 [GitHub Issues](https://github.com/Yuzai712/subagentOptimization/issues)，仓库为 `Yuzai712/subagentOptimization`，使用 `gh` 操作。工程技能要求“发布到问题跟踪器”时，指创建适合公开的 GitHub Issue；读取 ticket 时读取对应 Issue。

## 操作约定

- 从 `git remote -v` 核实仓库，不把其它项目的 Issue 发到这里。
- 读取：`gh issue view <number> --json number,title,body,labels,comments`。
- 查询：`gh issue list --state open --json number,title,labels`，按任务增加标签等筛选。
- 创建或评论前检查目标、授权和公开内容。多行正文在仓库外写临时文件，再用 `--body-file` 提交。
- 标签使用[分流标签表](triage-labels.md)；技能要求创建其它标签时按实际工作需要处理。
- 子问题和依赖优先使用当前 GitHub 与 CLI 支持的能力，不支持时使用公开 Issue 的引用和任务列表表达。

**PRs as a request surface: no.**

## 内容边界

Issues 只保存经授权公开的需求、可复现步骤、必要的脱敏错误和最终结论。逐轮诊断报告、原始日志、会话交接、完整配置和私人证据留在仓库外；不能把私有绝对路径当作公开附件或粘贴诊断全文。仅执行项目设置不授权批量创建 Issue、评论或接触认证。

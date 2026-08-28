# AGENTS.md - Agent 工作指南

本文档为 Agent（包括 CodeBuddy、Claude Code、Cursor、GitHub Copilot 等）在本仓库中工作提供指南。

## 核心记忆

### 项目定位

量潮工程标准（quanttide-specification）是量潮知识管理体系中标准的**聚合容器**（主体轴/Who it is + 领域轴/What it expresses），采用 Git 子模块架构聚合各法人主体与领域的标准仓库。

### 子模块管理

- 子模块独立维护，本仓库只追踪引用指针
- **禁止**：直接在父仓库修改子模块文件
- **必须**：在子模块仓库独立提交推送，父仓库只更新引用
- **新增子模块**：`git submodule add <url> default/<path>`（主体标准）或 `domains/<path>`（领域标准），并同步更新 README.md 结构树与 CHANGELOG.md

## 人机协作范式

1. **最小干预**：仅在用户明确请求时操作
2. **信息复用**：优先使用已有文档内容
3. **维护记录**：修改后同步更新 CHANGELOG.md
4. **原子提交**：每次提交包含完整独立变更
5. **提交即推送**：提交后默认推送到远端，除非用户明确说"只提交不推"

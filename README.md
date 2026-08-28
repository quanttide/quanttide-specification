# 量潮工程标准

## 仓库定位

量潮工程标准（quanttide-specification）是量潮知识管理体系中的**标准聚合容器**——按主体与领域聚合各工程标准子仓库（git submodule）。每个子仓库独立维护，本仓库只追踪引用。

在量潮"正交分解"中，本仓库横跨**主体轴（Who it is）与领域轴（What it expresses）**：`default/` 聚合法人主体标准，`domains/` 聚合各领域标准，回答"我们依据什么标准运行"。

## 仓库结构

```
quanttide-specification/
├── default/company        → 法人主体标准（quanttide-specification-of-business-entity）
├── domains/               → 领域标准子仓库（git submodule）
│   ├── academic-research  → 学术研究标准（quanttide-specification-of-academic-research）
│   ├── asset              → 资产管理标准（quanttide-specification-of-asset-management）
│   ├── auth               → 身份认证标准（quanttide-specification-of-authorization）
│   ├── cloud-computing    → 云计算标准（quanttide-specification-of-cloud-computing）
│   ├── collaboration      → 团队协作标准（quanttide-specification-of-collaboration）
│   ├── commerce           → 交易工程标准（quanttide-specification-of-commerce）
│   ├── connect            → 沟通管理标准（quanttide-specification-of-communication-management）
│   ├── course             → 课程研发标准（quanttide-specification-of-course-development）
│   ├── customer-support   → 客户支持标准（quanttide-specification-of-customer-support）
│   ├── data               → 数据工程标准（quanttide-specification-of-data-engineering）
│   ├── delib              → 议事管理标准（quanttide-specification-of-deliberation-management）
│   ├── design-language    → 设计语言标准（quanttide-specification-of-design-language）
│   ├── devops             → DevOps 工程标准（quanttide-specification-of-devops）
│   ├── disciplines        → 学科分类标准（quanttide-specification-of-disciplines）
│   ├── documents          → 文档标准（quanttide-specification-of-documents）
│   ├── finance            → 财务管理标准（quanttide-specification-of-finance-management）
│   ├── generative-ai      → 生成式人工智能标准（quanttide-specification-of-generative-ai）
│   ├── higher-education   → 高等教育标准（quanttide-specification-of-higher-education）
│   ├── human              → 人力资源标准（quanttide-specification-of-human-resources）
│   ├── knowl              → 知识工程标准（quanttide-specification-of-knowledge-engineering）
│   ├── learn              → 学习管理标准（quanttide-specification-of-learning-management）
│   ├── media              → 新媒体运营标准（quanttide-specification-of-social-media）
│   ├── network-applications → 网络应用标准（quanttide-specification-of-network-applications）
│   ├── product            → 产品研发标准（quanttide-specification-of-product-development）
│   ├── project            → 项目管理标准（quanttide-specification-of-project-management）
│   ├── readme             → 工程标准总纲（quanttide-specification-of-readme）
│   ├── strategy           → 战略管理标准（quanttide-specification-of-strategic-management）
│   ├── templates          → 模板规范（quanttide-specification-of-templates）
│   └── think              → 认知工程标准（quanttide-specification-of-cognitive-engineering）
├── README.md              → 本文件
├── AGENTS.md              → Agent 工作指南
├── CHANGELOG.md           → 版本变更记录
└── LICENSE                → 许可证
```

## 子模块管理

- 子模块独立提交推送，本仓库只更新引用指针
- 新增标准仓库：`git submodule add <url> default/<path>`（主体标准）或 `domains/<path>`（领域标准）
- 同步全部子模块：`git submodule update --init --recursive`

## 关联

- 标准与章程、档案、日志同源：`assets/quanttide-bylaw`（章程聚合）、`assets/quanttide-profile`（工作档案聚合）、`assets/quanttide-journal`（工作日志聚合）
- 主仓库：`quanttide` 根仓库

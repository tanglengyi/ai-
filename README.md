# AI 应用技术 × 产品经营 × 业务深度学习路线

> 面向具有 ToB 产品、业务流程与数据梳理经验，希望从“知识库功能产品”升级为“懂技术、懂评测、懂业务结果、能经营产品”的 AI 产品与解决方案人才。

最后核验学习链接：**2026-07-26**

## 1. 这份仓库解决什么问题

很多 AI 项目停留在：上传文档、切片、向量检索、调用大模型、生成一个聊天界面。这样的能力容易被平台化工具覆盖，也很难回答客户和管理者真正关心的问题：

- 为什么这个方案能解决业务问题？
- 模型为什么答错？
- “准确率”具体指什么，如何测量？
- 应该使用 RAG、微调、工作流、Agent 还是规则引擎？
- 如何处理版本冲突、权限、时效性、拒答和人工升级？
- 上线后是否真正降低成本、提高效率、增加收入或降低风险？
- 产品如何定价、控制毛利、推动续费并规模化复制？

本仓库将能力目标定义为：

> **能够发现值得做的 AI 机会，把不确定的模型能力建设成可测量、可解释、可迭代、可经营的业务产品。**

## 2. 推荐职业定位

结合已有的 ToB 产品、流程再造、字段与数据梳理经验，更适合的发展方向是：

- AI Solutions Product Manager
- Technical Product Manager, AI/LLM
- AI Solution Architect
- AI Application Architect
- Industry AI Solution Manager
- AI Platform / MaaS Product Manager
- AI Evaluation Product Manager

建议能力配比：

- **45% AI 应用技术深度**：LLM、RAG、Agent、评测、工程化、成本与可观测性。
- **30% 产品与数据能力**：用户研究、产品设计、指标体系、实验、路线图与跨团队交付。
- **25% 行业与经营能力**：业务流程、行业规则、商业模式、定价、毛利、续费和规模化。

不必一开始就与算法研究人员竞争预训练和分布式训练，但需要做到：能定义问题、能搭建方案、能定位错误、能设计实验、能解释结果、能推动业务闭环，并能判断产品是否值得持续经营。

## 3. 总体学习框架

```text
市场、客户与业务问题
    ↓
用户、流程、规则、状态、数据对象与 Baseline
    ↓
产品定位、MVP、用户旅程与指标体系
    ↓
数据治理与知识建模
    ↓
AI 方案选择：Prompt / Workflow / RAG / Fine-tuning / Agent / Tool
    ↓
应用工程：接口、存储、权限、日志、部署、监控
    ↓
评测：检索、生成、系统、业务四层指标
    ↓
上线验证：质量、成本、时延、风险、使用与 ROI
    ↓
定价、交付、续费、产品标准化与规模复制
    ↓
失败分析与持续迭代
```

学习时始终采用“五步闭环”：

1. **定义**：能够准确解释概念、边界和适用条件。
2. **实现**：亲手完成可运行实验、原型或业务方案。
3. **对比**：至少比较两种方案，而不是只做一个 Demo。
4. **评测**：使用固定数据集、指标和业务实验验证差异。
5. **经营**：说明对用户、流程、收入、成本、风险和规模化的影响。

## 4. 文档目录

| 文档 | 内容 |
|---|---|
| [00-ai-product-manager-core-capability-framework.md](docs/00-ai-product-manager-core-capability-framework.md) | **AI 产品经理核心能力总纲**：需求判断、产品评测、上下文工程及构建、产品化与经营能力 |
| [01-learning-framework.md](docs/01-learning-framework.md) | 六层能力模型、学习方法与掌握标准 |
| [02-core-concepts.md](docs/02-core-concepts.md) | AI、LLM、RAG、微调、Agent、评测与工程术语定义 |
| [03-rag-engineering.md](docs/03-rag-engineering.md) | 从数据接入到检索、重排、生成、权限与版本治理 |
| [04-evaluation-and-llmops.md](docs/04-evaluation-and-llmops.md) | 四层评测体系、Golden Dataset、错误归因与 LLMOps |
| [05-business-and-data.md](docs/05-business-and-data.md) | 业务流程、状态机、数据模型、AI 方案选型与 ROI |
| [06-12-week-roadmap.md](docs/06-12-week-roadmap.md) | 12 周学习计划、每周产出与验收标准 |
| [07-industrial-support-project.md](docs/07-industrial-support-project.md) | 工业设备多语言售后诊断系统完整项目蓝图 |
| [08-course-links.md](docs/08-course-links.md) | 官方课程、文档、学习顺序与取舍建议 |
| [09-dama-dmbok2/README.md](docs/09-dama-dmbok2/README.md) | DAMA-DMBOK2 全书结构化知识库及 AI 项目映射 |
| [09-facts-interview-question-bank-v3.md](docs/09-facts-interview-question-bank-v3.md) | **FACTS-E 3.0**：AI 项目、产品、数据、经营、MaaS、增长、多模态和机器人全场景面试体系 |
| [09-facts-interview-question-bank-v3.1-upgrade-notes.md](docs/09-facts-interview-question-bank-v3.1-upgrade-notes.md) | **3.1 增量升级**：上下文工程、快速原型、Workflow/单 Agent/Multi-Agent 选型专项 |
| [09-facts-interview-question-bank-v2.md](docs/09-facts-interview-question-bank-v2.md) | FACTS-E 2.0 归档：六维项目题与 30 张技术答案卡 |
| [09-facts-interview-question-bank.md](docs/09-facts-interview-question-bank.md) | FACTS-E 1.0 归档版 |
| [10-algorithm-engineering-interview-supplement.md](docs/10-algorithm-engineering-interview-supplement.md) | 算法岗补充：ML/NLP/Transformer、训练部署、Python 与手撕题 |
| [ai-product-interview-case-template-v3.md](templates/ai-product-interview-case-template-v3.md) | 3.0 项目深挖、产品设计、数据和商业案例统一模板 |
| [ai-product-job-fit-scorecard-v3.md](templates/ai-product-job-fit-scorecard-v3.md) | JD 十维匹配评分、项目证据和面试准备清单 |
| [project-assessment.md](templates/project-assessment.md) | AI 项目立项与岗位价值判断模板 |
| [evaluation-dataset-template.csv](templates/evaluation-dataset-template.csv) | AI 问答评测数据集字段模板 |
| [dama-data-management-assessment.md](templates/dama-data-management-assessment.md) | DAMA 数据管理与 AI 项目上线评估模板 |

## 5. 最终验收标准

完成路线后，应能够独立回答并用项目、实验或数据验证以下问题：

1. 一个业务问题是否真的需要 AI 或大模型？
2. 为什么选择规则、工作流、RAG、微调、Agent 或工具调用？
3. 数据应该如何清洗、分块、标注、授权和建模？
4. 检索失败、生成失败、工具失败和业务定义失败如何区分？
5. 如何构建覆盖正常、异常、拒答、版本冲突和攻击样本的评测集？
6. 如何计算检索质量、回答忠实度、任务成功率和业务结果？
7. 如何在质量、时延、成本、体验和风险之间做取舍？
8. 如何设计上下文来源、优先级、Token 预算、记忆和权限？
9. 如何在一周内搭建并评测一个 AI 原型？
10. 如何判断使用 Workflow、单 Agent 还是 Multi-Agent？
11. 如何把一次 Demo 变成可持续迭代的生产系统？
12. 如何定义北极星指标、埋点、漏斗和 A/B 测试？
13. 如何设计 SaaS、API、任务或私有化收费模式？
14. 如何计算模型成本、交付成本、毛利和 ROI？
15. 如何推动 POC、交付、验收、使用、续费和扩容？
16. 如何把客户定制沉淀为标准产品和平台能力？
17. 如何覆盖 MaaS、ToC 增长、多模态和 AI 硬件等细分岗位？
18. 如何通过真实项目证明自己的技术深度、产品判断和经营能力？

## 6. 推荐实践项目

本仓库建议以 **“多语言工业设备售后诊断与知识问答系统”** 作为主线项目：

- 真实业务复杂度高，包含型号、固件、App 版本、错误码、设备状态和环境条件。
- 既能发挥 ToB 流程、数据、规则和字段梳理优势，又能训练 RAG、评测和工程能力。
- 可进一步补充 POC、定价、交付、续费、标准化和产品经营分析。
- 可形成代码、数据模型、上下文设计、原型实验、评测报告、成本模型和项目复盘，适合求职展示。

详见：[工业设备多语言售后诊断系统项目蓝图](docs/07-industrial-support-project.md)。

## 7. 使用原则

- 优先学习官方课程、官方文档与原始论文。
- 不以“看完课程”或“背完题库”为完成标准，以可运行产出和可验证结果为标准。
- 不追逐所有新框架，先掌握稳定的底层概念、业务建模和实验方法。
- 企业数据必须获得授权并完成脱敏；作品集可保留结构，替换真实内容。
- 所有模型、课程、价格、岗位要求和平台能力都可能变化，实际使用前应再次核验。

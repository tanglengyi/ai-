# 08｜官方课程、文档与学习顺序

> 链接最后核验日期：**2026-07-24**。课程价格、权限、证书与页面结构可能变化，应以官方页面为准。

## 1. 最小必学路径

时间有限时，优先完成以下内容：

1. Google Machine Learning Crash Course：指标、数据集、神经网络、Embedding、LLM 和生产系统基础。
2. DeepLearning.AI：Generative AI with Large Language Models。
3. DeepLearning.AI：Retrieval Augmented Generation。
4. OpenAI Evals 文档 + Ragas。
5. Full Stack Deep Learning：生产化与完整 AI 产品生命周期。
6. 使用真实行业项目完成评测和业务闭环。

## 2. 机器学习基础

### Google Machine Learning Crash Course

- 官方课程（中文）：https://developers.google.com/machine-learning/crash-course/?hl=zh-cn
- 官方课程（英文）：https://developers.google.com/machine-learning/crash-course/
- 练习列表：https://developers.google.com/machine-learning/crash-course/exercises?hl=zh-CN
- 前置要求：https://developers.google.com/machine-learning/crash-course/prereqs-and-prework

建议优先模块：

- Classification。
- Datasets, Generalization, and Overfitting。
- Neural Networks。
- Embeddings。
- Intro to Large Language Models。
- Production ML Systems。

学习目标：

- 理解训练、验证、测试和过拟合。
- 能解释 Precision、Recall 和业务取舍。
- 理解 Embedding 和 LLM 的基础机制。
- 知道生产 ML 系统不只有模型。

## 3. 大语言模型基础

### DeepLearning.AI｜Generative AI with Large Language Models

- 官方页面：https://www.deeplearning.ai/courses/generative-ai-with-llms

官方页面显示课程约 10 小时，内容包括：

- LLM 生命周期。
- Transformer 和预训练。
- Prompt 与推理。
- Fine-tuning。
- 评测和部署。

建议产出：

- LLM 生命周期图。
- RAG、微调和 Prompt 的差异说明。
- 不同模型参数的对照实验。

### Hugging Face LLM Course

- 官方课程：https://huggingface.co/learn/llm-course/en/chapter1/1

主要内容：

- Transformer 模型。
- Transformers 库。
- Fine-tuning。
- Datasets、Tokenizers 和 Accelerate。
- 高质量数据集构建。
- LLM 微调和推理模型。

建议顺序：

- 第一阶段：第 1～3 章，理解模型调用、Tokenizer 和基础微调。
- 第二阶段：第 5～7 章，补数据集和 NLP 任务。
- 第三阶段：第 10～12 章，深入数据、微调和推理模型。

不要一开始完整通刷，应与项目任务同步学习。

## 4. RAG 系统学习

### DeepLearning.AI｜Retrieval Augmented Generation

- 官方页面：https://www.deeplearning.ai/courses/retrieval-augmented-generation

官方页面显示课程约 24.5 小时，包含：

- RAG 架构。
- 关键词、语义和混合检索。
- 向量数据库。
- Chunking 和 Query Parsing。
- 检索评测。
- 生成、部署和生产监控。

适合作为 RAG 主课。建议边学边完成：

- BM25 vs 向量检索。
- 混合检索。
- Metadata Filter。
- 检索评测。
- 生产日志和监控。

### DeepLearning.AI｜Building and Evaluating Advanced RAG

- 官方页面：https://www.deeplearning.ai/courses/building-evaluating-advanced-rag
- 备用页面：https://www.deeplearning.ai/short-courses/building-evaluating-advanced-rag/

官方页面显示课程约 1 小时 55 分，重点包括：

- Sentence-window Retrieval。
- Auto-merging Retrieval。
- Context Relevance。
- Groundedness。
- Answer Relevance。
- 实验和迭代。

建议在已完成 RAG Baseline 后学习，否则容易只会调用框架而不理解对比价值。

## 5. AI 评测

### OpenAI Evaluation Best Practices

- 官方指南：https://developers.openai.com/api/docs/guides/evaluation-best-practices
- OpenAI Evals API 参考：https://platform.openai.com/docs/api-reference/evals
- OpenAI Graders API 参考：https://platform.openai.com/docs/api-reference/graders

重点学习：

- 先定义成功标准。
- 使用代表性数据集。
- 采用持续评测，而不是一次性测试。
- 对模型和 Prompt 变更执行回归。
- 根据任务设计评测器和评分规则。

### Ragas

- 官方文档：https://docs.ragas.io/en/latest/
- 快速开始：https://docs.ragas.io/en/latest/getstarted/
- Faithfulness：https://docs.ragas.io/en/latest/concepts/metrics/available_metrics/faithfulness/
- Core Concepts：https://docs.ragas.io/en/latest/concepts/index.html
- CLI 与评测模板：https://docs.ragas.io/en/latest/howtos/cli/

适合学习：

- Dataset、Metric、Experiment。
- RAG、Prompt、Workflow 和 Agent 评测。
- Faithfulness 等语义指标。
- 从主观体验转向固定评测循环。

注意：

- Ragas 指标不是业务真理。
- 必须使用人工样本校准。
- 不同版本 API 可能变化，代码以当前官方文档为准。

## 6. 生产工程与 LLMOps

### Full Stack Deep Learning

- 官方主页：https://fullstackdeeplearning.com/
- 课程目录：https://fullstackdeeplearning.com/course/
- LLM Bootcamp：https://fullstackdeeplearning.com/llm-bootcamp/

课程强调 AI 产品完整生命周期：

- 问题定义。
- 数据和模型选择。
- 部署。
- 测试和监控。
- 持续学习。
- 用户体验和团队协作。

建议重点关注：

- ML 项目设计。
- 数据管理。
- 部署与监控。
- 测试和可解释性。
- LLM 应用生产化。

### OpenAI API 文档

- 开发者主页：https://developers.openai.com/
- 模型列表：https://developers.openai.com/api/docs/models
- 模型选择与使用指南：https://developers.openai.com/api/docs/guides/latest-model

学习重点不是记住当前模型名称，而是建立模型选型实验：

- 质量。
- 时延。
- 成本。
- 上下文长度。
- 结构化输出。
- 工具调用。
- 多语言和视觉能力。

生产配置应固定模型版本，并通过评测后再升级。

## 7. RAG 与微调选型

### Microsoft Learn｜使用 RAG 或微调扩充 LLM

- 中文：https://learn.microsoft.com/zh-cn/azure/developer/ai/augment-llm-rag-fine-tuning
- 英文：https://learn.microsoft.com/en-us/azure/developer/ai/augment-llm-rag-fine-tuning

用于理解：

- RAG 如何接入私有和实时数据。
- Fine-tuning 如何适配特定任务和行为。
- 两种方案的适用条件与组合方式。

学习后应形成自己的选型表，而不是只复述概念。

## 8. 模型底层进阶

### Stanford CS336｜Language Modeling from Scratch

- 官方课程：https://cs336.stanford.edu/

课程从头覆盖：

- Tokenizer。
- Transformer 架构。
- 优化器和训练。
- GPU、并行和系统优化。
- Scaling Laws。
- 推理。
- 数据清洗和去重。
- 评测、SFT 和强化学习。

该课程实现量大，对 Python 和工程能力要求高。

建议学习时机：

- 已完成 LLM、RAG 和评测基础。
- 已能独立编写 Python 项目。
- 确定需要向模型工程、训练或推理优化深入。

不建议将它作为第一门 AI 课程。

## 9. 数据与业务流程进阶

### dbt Learn

- 官方课程目录：https://learn.getdbt.com/catalog?category=courses
- Fundamentals 学习页面：https://learn.getdbt.com/learn/course/dbt-fundamentals/welcome-to-dbt-fundamen

适合补充：

- 数据转换。
- 数据模型。
- 测试与文档。
- 数据血缘。
- Analytics Engineering 思维。

对原本擅长字段、数据库和业务数据梳理的人，dbt 能帮助把经验升级为更规范的数据工程表达。

### Celonis Academy｜Process Mining

- Academy 主页：https://academy.celonis.com/
- Introduction to Process Mining：https://academy.celonis.com/learn/course/introduction-to-process-mining/introduction-to-process-mining-1/introduction
- Object-Centric Process Mining：https://academy.celonis.com/pages/all-about-ocpm
- Process Management：https://academy.celonis.com/pages/cpm

适合补充：

- 从事件日志还原真实流程。
- 发现等待、返工和流程变体。
- 对比标准流程与实际流程。
- 识别自动化和 AI 介入点。

## 10. 推荐学习顺序

### 第一阶段：4 周基础

1. Google MLCC 核心模块。
2. Python、Pandas、SQL 和 API。
3. Generative AI with LLMs。
4. Hugging Face 第 1～3 章。

### 第二阶段：4 周 RAG 与评测

1. Retrieval Augmented Generation。
2. Advanced RAG。
3. OpenAI Evals。
4. Ragas。

### 第三阶段：4 周生产与业务

1. Full Stack Deep Learning。
2. FastAPI、Docker、日志和 Trace。
3. dbt 或数据模型基础。
4. Process Mining 和业务流程。
5. 完成主线项目与业务报告。

### 第四阶段：按职业方向选修

- AI 应用架构：深入 RAG、Agent、LLMOps 和安全。
- AI 工程：Hugging Face、PEFT、部署与推理优化。
- 模型技术：Stanford CS336、PyTorch 和训练系统。
- 业务解决方案：流程挖掘、数据治理、行业模型和 ROI。

## 11. 不建议优先投入的课程

在当前目标下，不建议优先购买或投入大量时间到：

- 只讲 AI 产品经理概念、不写代码也不评测的课程。
- 只教 Prompt 模板的课程。
- 只教低代码知识库搭建的课程。
- 追逐大量框架名称但没有固定项目的课程。
- 只讲模型新闻、缺乏原理和实验的课程。
- 价格高但没有代码作业、导师反馈和真实项目的数据课程。

判断一门课程是否值得：

1. 是否有明确前置要求？
2. 是否有可运行代码和作业？
3. 是否讲指标、失败案例和工程约束？
4. 是否能支持当前项目产出？
5. 是否来自官方、大学或有真实生产经验的团队？
6. 学完后能否形成可验证能力，而不只是证书？

## 12. 学习记录模板

每完成一个模块记录：

```markdown
## 模块名称

- 学习来源：
- 核心定义：
- 适用场景：
- 不适用场景：
- 最小实现：
- 实验变量：
- 评测指标：
- 失败案例：
- 对主线项目的应用：
- 仍不理解的问题：
```

课程不是主线，项目和评测才是主线。

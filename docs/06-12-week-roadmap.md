# 06｜12 周系统学习路线

## 1. 总体目标

12 周后不以“看完多少课”为验收，而是交付一套可运行、可评测、可解释的 AI 应用系统，并能够完成技术选型、错误归因和业务价值分析。

建议投入：每周 10～12 小时。

每周时间分配：

- 课程和文档：3～4 小时。
- 编码和实验：4 小时。
- 评测和错误分析：2 小时。
- 业务建模与文档：1～2 小时。

主线项目：**多语言工业设备售后诊断与知识问答系统**。

## 2. 学习工具准备

建议环境：

- Python 3.11+。
- VS Code 或 PyCharm。
- Jupyter Notebook。
- Git 和 GitHub。
- Docker Desktop。
- PostgreSQL 或 SQLite。
- 一个向量数据库：可先用 FAISS/Chroma，本地验证后再接生产型方案。
- 一个 LLM API 或本地开源模型。

基础技能最低要求：

- Python：函数、类、异常、文件处理、虚拟环境。
- Pandas：读取、清洗、分组、合并。
- SQL：SELECT、JOIN、GROUP BY、窗口函数。
- HTTP：GET/POST、Header、JSON、状态码。
- Git：clone、branch、commit、push、pull request。

## 3. 第 1 周：机器学习与指标基础

### 学习内容

- 监督学习、无监督学习、训练/验证/测试集。
- 过拟合、泛化、数据泄漏。
- Accuracy、Precision、Recall、F1、AUC。
- Baseline 和实验变量。

### 推荐学习

- Google Machine Learning Crash Course：分类、数据集、泛化与过拟合。
- 课程链接见 `08-course-links.md`。

### 实践任务

对一份售后问题数据完成：

1. 清洗空值和重复数据。
2. 按问题类型分类。
3. 统计各类别数量。
4. 构造一个简单分类 Baseline。
5. 输出混淆矩阵并解释 Precision 与 Recall 的业务含义。

### 验收产出

- `notebooks/week01_ml_metrics.ipynb`。
- 一页指标定义。
- 一份“错误分类任务中 Precision 和 Recall 如何取舍”的说明。

## 4. 第 2 周：Python、SQL 与数据处理

### 学习内容

- Python 文件、JSON、正则和异常处理。
- Pandas 数据处理。
- SQL 数据建模和查询。
- API 请求与响应。

### 实践任务

设计并实现基础数据表：

- product_model。
- firmware_version。
- error_code。
- support_case。
- knowledge_document。

从 CSV 导入数据，并查询：

- 某型号某版本适用的错误码。
- 最近 30 天高频问题。
- 未解决工单和平均处理时长。

### 验收产出

- 数据库建表 SQL。
- 数据字典。
- 数据清洗脚本。
- 5 条核心查询。

## 5. 第 3 周：LLM 基础

### 学习内容

- Token、Tokenizer、Embedding。
- Transformer 与 Attention。
- 预训练、推理和上下文窗口。
- Temperature、Top-p 和输出长度。
- 幻觉成因。

### 推荐学习

- DeepLearning.AI：Generative AI with Large Language Models。
- Google MLCC：Intro to Large Language Models。
- Hugging Face LLM Course 第 1～2 章。

### 实践任务

使用同一批问题比较：

- 不同 Temperature。
- 不同模型。
- 有无 Few-shot 示例。
- 自由文本输出与结构化 JSON 输出。

### 验收产出

- LLM 生命周期图。
- 模型参数实验记录。
- 20 条问题的输出对比。
- 一份错误原因分析。

## 6. 第 4 周：Prompt、结构化输出与工具调用

### 学习内容

- System Prompt、Few-shot 和约束指令。
- JSON Schema。
- Function/Tool Calling。
- 追问、拒答和错误处理。

### 实践任务

实现“售后问题结构化抽取器”，输入自然语言，输出：

```json
{
  "product_model": null,
  "firmware_version": null,
  "error_code": null,
  "symptom": "",
  "battery_level": null,
  "environment": [],
  "missing_information": [],
  "risk_level": "low|medium|high"
}
```

再实现一个工具调用：根据产品型号和固件版本查询适用规则。

### 验收产出

- Prompt v1～v3。
- 结构化输出合规率报告。
- 工具调用成功率。
- 错误参数和降级策略。

## 7. 第 5 周：RAG Baseline

### 学习内容

- RAG 基础架构。
- 文档解析、Chunk、Embedding、向量检索。
- Top-K 与上下文组装。

### 推荐学习

- DeepLearning.AI：Retrieval Augmented Generation，模块 1～3。

### 实践任务

使用公开或脱敏的产品手册构建最小 RAG：

1. 文档解析。
2. 固定长度分块。
3. 向量索引。
4. Top-K 检索。
5. 基于上下文回答并给出引用。

### 验收产出

- 可运行 RAG Baseline。
- 50 条基础评测数据。
- 检索结果和生成结果日志。
- 第一版 Recall@K 与 Faithfulness。

## 8. 第 6 周：检索工程

### 学习内容

- BM25、语义搜索和混合检索。
- Metadata Filter。
- Query Rewrite。
- RRF 融合。

### 实践任务

比较四个方案：

1. 纯向量检索。
2. BM25。
3. 混合检索。
4. 混合检索 + Metadata Filter。

样本必须包含：错误码、型号、口语化描述和多语言问题。

### 验收产出

- 检索实验矩阵。
- Recall@1/3/5、MRR。
- 各方案失败样本。
- 推荐检索架构和理由。

## 9. 第 7 周：高级 RAG

### 学习内容

- 父子分块。
- 句子窗口。
- Reranker。
- 多查询与复杂问题拆分。
- 上下文压缩与去重。

### 推荐学习

- DeepLearning.AI：Building and Evaluating Advanced RAG。

### 实践任务

至少比较：

- 固定分块 vs 标题分块 vs 父子分块。
- 无 Reranker vs 有 Reranker。
- 原始问题 vs Query Rewrite。

### 验收产出

- 三组以上对照实验。
- 质量、P95 时延和成本对比。
- 一份“不采用某高级方案”的反向论证。

## 10. 第 8 周：Golden Dataset 与评测体系

### 学习内容

- Golden Dataset。
- Rubric。
- 检索层、生成层、系统层和业务层指标。
- 自动评测与人工评测。

### 推荐学习

- OpenAI Evaluation Best Practices。
- Ragas 指标与评测文档。

### 实践任务

将评测集扩展到至少 120 条，覆盖：

- 正常问答。
- 信息不足。
- 错误前提。
- 版本冲突。
- 知识库无答案。
- 应拒答。
- 应升级人工。
- 多语言。

### 验收产出

- 评测数据集 v1.0。
- Rubric。
- 自动评测脚本。
- 30 条人工复核结果。
- 自动评分与人工评分一致性分析。

## 11. 第 9 周：错误归因与回归测试

### 学习内容

- 数据、解析、检索、生成、工具和业务定义错误。
- 回归测试。
- Prompt、模型和索引版本管理。

### 实践任务

对所有失败样本进行根因标记，并完成至少两轮改进：

```text
运行评测
→ 选择最高频根因
→ 只修改一个主要变量
→ 回归测试
→ 判断是否改善且无明显副作用
```

### 验收产出

- 错误分类看板。
- Top 10 失败案例复盘。
- 两轮回归报告。
- 最终方案与 Baseline 对比。

## 12. 第 10 周：生产工程与 LLMOps

### 学习内容

- FastAPI。
- Docker。
- 日志、Trace、超时、重试和缓存。
- 模型路由和降级。
- P50/P95 时延。
- Token 成本。

### 推荐学习

- Full Stack Deep Learning。

### 实践任务

将系统封装为 API：

- `/diagnose`：结构化诊断。
- `/ask`：知识问答。
- `/feedback`：记录反馈。
- `/health`：健康检查。

加入：

- request_id。
- 模型与 Prompt 版本。
- 检索 Trace。
- Token 和时延统计。
- 异常重试与降级。

### 验收产出

- Docker 化服务。
- API 文档。
- 100 次测试请求的 P95 时延和成本。
- 故障与降级演练记录。

## 13. 第 11 周：业务流程与 ROI

### 学习内容

- AS-IS/TO-BE。
- 状态机。
- 数据模型。
- 人机分工。
- ROI 和 TCO。

### 实践任务

设计售后业务闭环：

```text
用户提问
→ 信息补充
→ AI 初诊
→ 操作建议
→ 用户反馈
→ 解决/升级工单
→ 专家修正
→ 知识更新
→ 回归评测
```

### 验收产出

- AS-IS 和 TO-BE 流程图。
- 数据实体关系图。
- 角色权限矩阵。
- 业务指标树。
- ROI 估算表。

## 14. 第 12 周：项目包装与面试表达

### 最终项目材料

1. 项目背景与业务问题。
2. 数据模型与知识治理。
3. AI 方案选择过程。
4. 系统架构图。
5. RAG 实验矩阵。
6. Golden Dataset 和评测体系。
7. 质量、时延和成本结果。
8. 失败案例和错误归因。
9. 业务流程与 ROI。
10. 风险、限制与下一步。

### 面试表达结构

```text
为什么做
→ 业务 Baseline
→ 为什么选择这套技术
→ 遇到的关键失败
→ 如何通过评测定位和优化
→ 最终业务与技术结果
→ 仍有哪些限制
```

### 验收标准

- 能现场解释 RAG 的每一层。
- 能展示固定评测数据，而不是只演示成功案例。
- 能回答 RAG 与微调的选择。
- 能说明模型为什么答错以及如何定位。
- 能给出上线风险、成本和人工兜底方案。

## 15. 12 周成果清单

完成后仓库中应至少包含：

```text
project/
├── data-model/
├── datasets/
├── notebooks/
├── src/
├── evals/
├── prompts/
├── reports/
├── diagrams/
└── docker/
```

核心成果：

- 一套可运行的 AI 应用。
- 一套不少于 120 条的评测数据。
- 一份检索与生成实验报告。
- 一份错误归因报告。
- 一份业务流程与 ROI 报告。
- 一套面试可展示的项目叙事。

## 16. 延伸路线

### 更深入 AI 应用工程

- 多模态 RAG。
- Agentic Workflow。
- Prompt Injection 防护。
- 多租户权限与企业安全。
- 高并发、缓存和模型路由。

### 更深入模型技术

- PyTorch。
- Hugging Face Fine-tuning。
- LoRA/PEFT。
- 量化与推理优化。
- Stanford CS336。

### 更深入业务数据

- 数据仓库和 dbt。
- 流程挖掘。
- 主数据管理。
- 指标体系与实验设计。
- 行业知识图谱。

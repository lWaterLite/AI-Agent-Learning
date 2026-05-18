# AI Agent 学习路径：从硕士一年级到实习与就业

生成日期：2026-05-18  
适用对象：计算机科学硕士一年级，希望未来从事 AI Agent、LLM 应用、RAG、智能体平台或相关工程岗位的学生  
建议周期：9 到 12 个月形成可求职作品集，12 到 18 个月形成研究与工程结合的竞争力

---

## 0. 先给你的定位建议

你现在最大的问题不是“导师放养”，而是缺少一个可执行的外部结构。AI Agent 方向很适合你这种阶段：它既需要扎实的工程能力，也需要理解模型、检索、规划、评测、安全和产品落地。你不一定要一开始就成为算法研究者，但必须尽快从“会调 API”升级到“能构建可靠的 agent 系统”。

我建议你把未来 12 个月的目标设为：

1. 掌握 LLM 应用与 agent 系统的核心概念。
2. 能独立构建一个带工具调用、RAG、记忆、评测、可观测性、安全边界的 agent 项目。
3. 形成 2 到 3 个 GitHub 项目、1 篇技术博客或中文长文、1 份可展示的在线 Demo。
4. 面向实习岗位准备算法、后端、系统设计和 LLM 应用面试。

最终你要塑造的求职画像不是“我学过 LangChain”，而是：

> 我能把大模型接入真实业务数据和工具，设计 agent 工作流，做评测与监控，并把系统部署成可用的产品。

---

## 1. 岗位图谱：你可以瞄准哪些方向

### 1.1 最匹配的岗位

1. AI Agent Engineer / LLM Application Engineer  
   重点能力：工具调用、RAG、workflow、memory、eval、部署。

2. RAG Engineer / Knowledge Agent Engineer  
   重点能力：文档解析、向量检索、重排、知识库构建、检索评测。

3. AI Platform Engineer / Agent Infrastructure Engineer  
   重点能力：后端、异步任务、权限、日志、监控、成本控制、模型路由。

4. Applied AI Engineer  
   重点能力：快速将模型能力产品化，能做 prompt、数据、工程和评测。

5. Research Engineer in Agent Systems  
   重点能力：读论文、复现实验、改进 agent 框架、做 benchmark。

### 1.2 你暂时不必把自己定位成纯算法研究员

如果你数学和深度学习基础还不够强，不建议一开始把目标设为“训练大模型”或“基础模型研究”。AI Agent 更适合以工程作为入口，再逐步补研究能力。

---

## 2. 能力地图

你需要建立 7 层能力。

### 第 1 层：基础编程与工程

必须掌握：

- Python：类型标注、异步编程、包管理、测试、日志。
- 后端：FastAPI、REST API、WebSocket、鉴权、数据库。
- 数据库：PostgreSQL、Redis、SQLite、向量数据库或 pgvector。
- 工具链：Git、Docker、Linux、CI、环境变量、配置管理。
- 前端轻量能力：React 或 Streamlit/Gradio，至少能做 Demo。

目标水平：别人给你一个业务需求，你能做出可部署的后端服务。

### 第 2 层：机器学习与深度学习基础

你不需要一开始推导所有细节，但要理解：

- 监督学习、损失函数、过拟合、验证集、评测指标。
- 神经网络、Transformer、attention、embedding。
- 语言模型的预训练、指令微调、RLHF/RLAIF 的基本概念。
- token、context window、temperature、top-p、结构化输出。

目标水平：能解释为什么 LLM 会幻觉，为什么 RAG 能缓解但不能消除幻觉。

### 第 3 层：LLM 应用基础

必须掌握：

- Prompt engineering：角色、任务、约束、示例、输出格式。
- Function calling / tool calling：让模型选择工具并读取工具返回值。
- Structured output：JSON schema、Pydantic 校验、失败重试。
- Streaming：流式输出与用户体验。
- Cost/latency：缓存、批处理、小模型路由、token 预算。

目标水平：不用框架，也能手写一个最小 agent loop。

### 第 4 层：RAG 与知识系统

必须掌握：

- 文档加载：PDF、网页、Markdown、数据库。
- 清洗与切分：chunk size、overlap、metadata。
- 向量检索：embedding、top-k、hybrid search。
- 重排：reranker、cross-encoder、LLM rerank。
- Query rewrite：多查询、HyDE、问题分解。
- Context packing：怎样把检索结果放进上下文。
- RAG 评测：faithfulness、answer relevancy、context precision/recall。

目标水平：能构建一个面向论文、课程资料或公司文档的问答系统，并证明它比 baseline 好。

### 第 5 层：Agent 核心机制

必须掌握：

- Agent loop：observe -> think/plan -> act -> observe。
- Tool use：API 调用、数据库查询、文件操作、浏览器操作。
- Planning：任务分解、反思、重试、状态机。
- Memory：短期上下文、长期记忆、用户画像、任务状态。
- Multi-agent：分工、handoff、critic、planner-executor。
- Human-in-the-loop：高风险动作前请求确认。
- Guardrails：输入输出过滤、权限控制、工具白名单。

目标水平：知道什么时候应该用 agent，什么时候普通工作流更可靠。

### 第 6 层：生产级工程

必须掌握：

- 评测：离线测试集、golden set、回归测试、A/B 测试。
- 可观测性：trace、tool call 日志、token、latency、error rate。
- 安全：prompt injection、tool poisoning、越权工具调用、数据泄露。
- 可靠性：超时、重试、幂等、限流、熔断。
- 权限：用户身份、资源 ACL、审计日志。
- 部署：Docker、云服务、队列、监控。

目标水平：你的项目不只是 notebook，而是一个能被别人试用的服务。

### 第 7 层：求职表达

必须准备：

- 简历项目：业务背景、技术架构、难点、指标、结果。
- GitHub：README、架构图、部署说明、测试。
- 面试：算法、Python、后端、系统设计、LLM 应用设计。
- 作品集：Demo 视频、在线体验、技术文章。

目标水平：面试官问“你做过什么 agent 项目”，你能讲出工程闭环。

---

## 3. 12 个月学习总路线

### 阶段 A：基础夯实与 LLM 入门，第 1 到 2 个月

目标：能写出不依赖框架的 LLM 应用和最小 agent。

每周安排：

- Python 工程：6 小时
- LLM API 与 prompt：5 小时
- 后端基础：4 小时
- 算法题：3 小时
- 阅读与笔记：2 小时

学习内容：

1. Python 工程
   - venv/uv/conda 环境管理。
   - requests/httpx、asyncio。
   - Pydantic、pytest、logging。
   - FastAPI 基本服务。

2. LLM API
   - chat completion / responses 类接口。
   - system prompt、developer prompt、user prompt 的职责。
   - structured output。
   - function calling / tool calling。

3. 最小项目
   - 项目名：`mini-tool-agent`
   - 功能：用户输入自然语言，agent 可以调用 3 个工具：计算器、天气 mock、文件搜索 mock。
   - 要求：不用 LangChain，只用模型 API + Python 函数 + 循环控制。

产出：

- GitHub 仓库 1：最小工具调用 agent。
- 一篇笔记：《我如何从零实现一个最小 AI Agent》。

验收标准：

- 能解释 agent loop。
- 能解释 tool schema。
- 能处理 JSON 解析失败、工具调用失败、超时。

---

### 阶段 B：RAG 与知识库，第 3 到 4 个月

目标：能做一个有评测的 RAG 系统。

每周安排：

- RAG 原理与实验：7 小时
- 文档处理与检索：5 小时
- 后端与数据库：4 小时
- 评测：3 小时
- 算法题：2 小时

学习内容：

1. 文档处理
   - PDF/Markdown/HTML 加载。
   - chunking 策略对结果的影响。
   - metadata 设计。

2. 检索系统
   - embedding 模型。
   - 向量数据库：Chroma、FAISS、Milvus、Qdrant 或 pgvector 任选其一。
   - BM25 + 向量混合检索。
   - rerank。

3. RAG pipeline
   - query rewrite。
   - retrieval。
   - rerank。
   - context compression。
   - answer generation。
   - citation。

4. RAG 评测
   - 人工构造 50 到 100 条测试问题。
   - 指标：命中率、faithfulness、answer relevance、context precision。
   - 引入 Ragas 或 LlamaIndex eval。

项目：

- 项目名：`paper-rag-assistant`
- 功能：上传 10 到 30 篇 AI agent/RAG 论文，支持中文问答、引用原文片段、给出相关论文列表。
- 要求：必须有 eval 脚本，能比较不同 chunk size、top-k、rerank 策略。

产出：

- GitHub 仓库 2：论文 RAG 助手。
- 一份实验报告：不同检索策略的效果比较。

验收标准：

- 能解释 RAG 的 5 个阶段：loading、indexing、storing、querying、evaluation。
- 能说明为什么“把文档塞进向量库”不是完整 RAG。
- 能证明某个优化确实提升了指标。

---

### 阶段 C：Agent 工作流与框架，第 5 到 6 个月

目标：掌握主流 agent 框架，但不被框架绑架。

每周安排：

- Agent 框架：7 小时
- 项目开发：8 小时
- 系统设计：3 小时
- 阅读源码/文档：3 小时

学习内容：

1. OpenAI Agents SDK
   - Agent、Runner、tool、handoff、guardrail、tracing。
   - 适合学习原生 agent 抽象和工具调用闭环。

2. LangGraph
   - state graph。
   - node、edge、conditional edge。
   - checkpoint、human-in-the-loop。
   - long-running workflow。

3. LlamaIndex Workflows
   - RAG workflow。
   - event-driven step。
   - 与知识系统结合。

4. Microsoft Agent Framework / AutoGen 思路
   - 多 agent 对话。
   - planner、executor、critic。
   - group chat 的边界和风险。

项目：

- 项目名：`research-agent-workflow`
- 功能：输入一个研究主题，agent 自动完成：
  - 拆解研究问题。
  - 搜索或读取本地论文库。
  - 生成阅读清单。
  - 提取每篇论文贡献、方法、实验、局限。
  - 生成综述草稿。
  - 对引用进行检查。

工程要求：

- 用 LangGraph 或 OpenAI Agents SDK 实现核心 workflow。
- 每个节点必须有日志和 trace。
- 高风险步骤加入 human approval，例如写文件、联网检索、删除内容。
- 加入失败重试与缓存。

产出：

- 一个完整 agent workflow 项目。
- README 中画出状态图。
- 写一篇技术文：《Agent Workflow 为什么不能只靠一个 while 循环》。

验收标准：

- 能说明 workflow agent 与自由循环 agent 的差异。
- 能解释状态、checkpoint、handoff、trace 的作用。
- 能讲清楚为什么多 agent 不一定比单 agent 好。

---

### 阶段 D：MCP、工具生态与真实系统集成，第 7 个月

目标：理解 agent 如何安全接入外部工具和上下文。

学习内容：

- MCP 的 client/server/resource/tool/prompt 概念。
- JSON-RPC 基础。
- STDIO 与 HTTP/SSE 传输。
- 工具权限与沙箱。
- 工具描述污染、prompt injection、数据泄露风险。

项目：

- 项目名：`campus-mcp-agent`
- 功能：
  - 写一个 MCP server，暴露本地课程笔记、论文索引、待办事项三个工具。
  - 写一个 agent client 调用这些工具。
  - 对每个工具设置权限和审计日志。

产出：

- 一个 MCP server。
- 一份安全说明：哪些工具允许自动调用，哪些必须人工确认。

验收标准：

- 能解释 MCP 与普通 REST API 的区别。
- 能解释为什么 MCP 工具不能随便给写文件、执行命令、访问密钥的权限。

---

### 阶段 E：评测、安全与可观测性，第 8 到 9 个月

目标：把项目从“能跑”升级成“可评估、可调试、可上线”。

学习内容：

1. 评测
   - 构造 golden dataset。
   - 单元测试 agent tool。
   - 对 prompt 和 workflow 做回归测试。
   - RAG 评测和端到端任务成功率。

2. 可观测性
   - trace 每次 LLM 调用。
   - 记录 tool call 输入输出。
   - 统计 token、latency、cost、error。
   - 使用 OpenTelemetry 或框架内置 tracing。

3. 安全
   - OWASP LLM Top 10。
   - prompt injection。
   - indirect prompt injection。
   - excessive agency。
   - sensitive information disclosure。
   - insecure output handling。

4. 可靠性
   - timeout。
   - retry。
   - circuit breaker。
   - fallback model。
   - 幂等工具调用。

项目升级：

- 给前面任意一个 agent 项目补上：
  - eval 数据集。
  - trace 页面或日志分析脚本。
  - prompt injection 测试样例。
  - 权限控制。
  - Docker 部署。

产出：

- 一份 `EVALUATION.md`。
- 一份 `SECURITY.md`。
- 一份 `DEPLOYMENT.md`。

验收标准：

- 你能回答：“这个 agent 什么时候会失败？失败后怎么发现？怎么降低损失？”

---

### 阶段 F：综合作品集与求职冲刺，第 10 到 12 个月

目标：完成一个企业级展示项目，并进入投递节奏。

综合项目建议三选一：

#### 方向 1：企业知识库 + 工单处理 Agent

功能：

- 接入企业文档、FAQ、历史工单。
- 用户提交问题后，agent 检索知识库，判断是否需要创建工单。
- 自动生成回复草稿。
- 高风险操作需要人工确认。
- 后台展示 trace、检索证据、评测结果。

适合岗位：

- AI Agent Engineer。
- LLM Application Engineer。
- RAG Engineer。

#### 方向 2：代码库维护 Agent

功能：

- 读取 GitHub 仓库。
- 根据 issue 定位相关文件。
- 生成修改计划。
- 运行测试。
- 生成 PR 描述。
- 不能直接合并，必须人工确认。

适合岗位：

- AI Coding Agent Engineer。
- Developer Productivity Engineer。
- AI Platform Engineer。

#### 方向 3：研究助手 Agent

功能：

- 管理论文库。
- 追踪主题。
- 自动生成阅读笔记。
- 对比论文方法。
- 生成实验复现计划。

适合岗位：

- Research Engineer。
- Applied Scientist Intern。
- AI Agent Research Intern。

最终作品集必须包含：

- 在线 Demo 或本地一键启动。
- 架构图。
- README。
- 评测结果。
- 安全边界说明。
- Demo 视频。
- 技术博客。

---

## 4. 每周执行模板

建议每周固定投入 20 到 25 小时。如果课业压力大，至少保证 12 到 15 小时。

### 标准周计划

周一：

- 1 小时复盘上周。
- 2 小时阅读官方文档或论文。

周二：

- 3 小时实现项目功能。

周三：

- 2 小时算法题。
- 1 小时整理技术笔记。

周四：

- 3 小时实现项目功能。

周五：

- 2 小时调试、测试、重构。

周六：

- 4 到 6 小时深度开发。
- 记录实验结果。

周日：

- 2 小时写周报。
- 1 小时更新 GitHub README。
- 1 小时准备下周计划。

### 每周周报模板

```markdown
## 本周目标

## 完成内容

## 遇到的问题

## 关键学习

## 下周计划

## 可展示产出
```

---

## 5. 论文与概念阅读路线

不建议一开始疯狂读论文。你的顺序应该是：先实现，再读论文解释现象，再回到项目优化。

### 第一批：LLM 与 Transformer

必须理解：

- Transformer。
- Attention。
- GPT 类自回归语言模型。
- In-context learning。
- Instruction tuning。
- RLHF。

阅读目标：不要求手推所有公式，但要能画出 Transformer block。

### 第二批：RAG

重点主题：

- Retrieval-Augmented Generation。
- Dense Passage Retrieval。
- Hybrid Search。
- Reranking。
- RAG evaluation。

阅读目标：能解释为什么检索质量决定 RAG 上限。

### 第三批：Agent

重点主题：

- ReAct。
- Toolformer。
- Reflexion。
- Plan-and-Execute。
- Voyager。
- SWE-agent / coding agent 思路。

阅读目标：理解 agent 从“prompt 技巧”变成“系统工程”的过程。

### 第四批：安全与评测

重点主题：

- Prompt injection。
- Indirect prompt injection。
- Agent tool misuse。
- LLM-as-a-judge 的偏差。
- Benchmark 设计。

阅读目标：知道为什么真实企业不会放心让 agent 拥有无限权限。

---

## 6. 实战操作建议

### 6.1 推荐开发环境

基础环境：

- Python 3.11 或 3.12。
- uv 或 conda。
- Node.js LTS。
- Docker Desktop。
- PostgreSQL + pgvector。
- Redis。
- GitHub。

Python 常用包：

- `fastapi`
- `uvicorn`
- `pydantic`
- `httpx`
- `pytest`
- `sqlalchemy`
- `openai`
- `langgraph`
- `langchain`
- `llama-index`
- `ragas`
- `chromadb` 或 `qdrant-client`
- `opentelemetry-api`
- `opentelemetry-sdk`

### 6.2 第一个 agent 项目的基本步骤

1. 创建项目结构

```text
mini-tool-agent/
  app/
    main.py
    agent.py
    tools.py
    schemas.py
    config.py
  tests/
    test_tools.py
    test_agent.py
  README.md
  pyproject.toml
```

2. 先写普通 Python 工具

```python
def calculator(expression: str) -> str:
    ...

def search_notes(query: str) -> str:
    ...
```

3. 为工具写 schema

```python
class CalculatorInput(BaseModel):
    expression: str
```

4. 写 agent loop

```text
用户问题 -> 模型判断是否调用工具 -> 执行工具 -> 把工具结果返回模型 -> 得到最终答案
```

5. 加入失败处理

- JSON 解析失败。
- 工具不存在。
- 工具超时。
- 工具返回过长。
- 模型循环次数过多。

6. 写测试

- 工具单元测试。
- agent 不调用工具的测试。
- agent 调用工具的测试。
- 错误工具调用测试。

### 6.3 做项目时的原则

1. 先做 baseline，再做 fancy agent。
2. 先让流程可测试，再引入多 agent。
3. 每个工具都要有权限边界。
4. 每次模型调用都要可追踪。
5. 每个优化都要有指标证明。
6. README 要写给招聘方看，不只是写给自己看。

---

## 7. 推荐技术栈选择

### 初学阶段

优先：

- Python
- FastAPI
- OpenAI/Anthropic/Gemini 任一模型 API
- SQLite
- Chroma 或 FAISS
- Streamlit 或简单 React

不要一开始上太多组件。

### 进阶阶段

优先：

- LangGraph 或 OpenAI Agents SDK
- LlamaIndex
- PostgreSQL + pgvector
- Redis
- Docker
- OpenTelemetry
- Ragas

### 作品集阶段

优先：

- FastAPI 后端。
- React 前端。
- PostgreSQL。
- Redis Queue / Celery / Dramatiq。
- Docker Compose。
- GitHub Actions。
- 云部署。

---

## 8. 面试准备路线

### 8.1 算法

目标：不要让算法成为实习面试短板。

重点：

- 数组、字符串、哈希表。
- 双指针、滑动窗口。
- 栈、队列、堆。
- 二叉树、图搜索。
- 动态规划基础。
- 排序、二分。

安排：

- 每周 5 到 8 题。
- 优先 LeetCode Hot 100。
- 每题写复盘：思路、复杂度、易错点。

### 8.2 Python 与后端

必须会答：

- Python GIL。
- async/await。
- 生成器。
- 装饰器。
- Pydantic。
- FastAPI 请求生命周期。
- 数据库索引。
- 事务。
- Redis 使用场景。
- Docker 镜像与容器。

### 8.3 LLM 应用面试

高频问题：

1. RAG 如何降低幻觉？
2. chunk size 怎么选？
3. embedding 检索和 BM25 各自优缺点？
4. rerank 有什么作用？
5. 如何评测 RAG？
6. agent 为什么会失控？
7. 如何防止 prompt injection？
8. tool calling 如何设计权限？
9. 多 agent 什么时候有价值？
10. 如何降低 LLM 应用成本和延迟？

### 8.4 系统设计面试

你应该能设计：

- 企业知识库问答系统。
- 自动客服 agent。
- 代码修复 agent。
- 数据分析 agent。
- 会议纪要与任务跟踪 agent。

回答框架：

1. 用户与业务目标。
2. 数据来源。
3. RAG/agent 工作流。
4. 工具权限。
5. 存储设计。
6. 评测指标。
7. 可观测性。
8. 安全风险。
9. 成本与扩展性。

---

## 9. 简历项目写法

不要写：

> 使用 LangChain 构建智能问答系统。

应该写：

> 构建面向论文知识库的 RAG Agent，支持 PDF 解析、向量检索、rerank、引用溯源与离线评测；在 80 条自建测试集上将 context precision 从 0.61 提升到 0.78，并通过 trace 日志定位检索失败样例。

项目描述结构：

1. 背景：解决什么问题。
2. 技术：用了什么核心技术。
3. 难点：遇到什么困难。
4. 结果：有什么指标或效果。
5. 工程：是否部署、测试、监控。

---

## 10. 你可以马上开始的 14 天计划

### 第 1 天

- 建立 GitHub 仓库。
- 配置 Python 环境。
- 读 OpenAI Agents SDK 或任一模型 API 的 tool calling 文档。
- 写下你对 agent 的定义。

### 第 2 天

- 写 3 个 Python 工具：计算器、时间查询、文本搜索。
- 为每个工具写单元测试。

### 第 3 天

- 手写 tool schema。
- 让模型选择是否调用工具。

### 第 4 天

- 实现 agent loop。
- 限制最大循环次数。

### 第 5 天

- 加入错误处理。
- 加入日志。

### 第 6 天

- 用 FastAPI 包装成接口。

### 第 7 天

- 写 README。
- 录制 1 分钟 Demo。

### 第 8 天

- 学习 RAG 基本流程。
- 准备 5 篇 PDF 或 Markdown 文档。

### 第 9 天

- 做文档切分。
- 生成 embedding。

### 第 10 天

- 建立向量检索。
- 实现简单问答。

### 第 11 天

- 加入引用来源。
- 记录检索结果。

### 第 12 天

- 人工写 20 个测试问题。

### 第 13 天

- 比较 top-k、chunk size 的影响。

### 第 14 天

- 写第一篇技术博客或学习总结。

---

## 11. 导师放养情况下的自救机制

你需要把“没人管”变成“自己有节奏”。

建议：

1. 每周给导师发一封简短周报。
2. 每月约一次 20 分钟沟通。
3. 每月给导师看一个可运行结果，而不是泛泛说“我在学习 AI agent”。
4. 主动找实验室同学做代码 review。
5. 在 GitHub、知乎、掘金、博客园或个人博客公开输出。
6. 参加开源项目 issue，哪怕先修文档。

给导师的周报模板：

```markdown
老师好，本周我主要推进了 AI Agent 方向的学习与项目：

1. 完成内容：
2. 当前结果：
3. 遇到问题：
4. 下周计划：
5. 希望请教：

附件/链接：
```

---

## 12. 风险提醒

### 风险 1：只学框架，不懂原理

解决办法：第一个 agent 必须手写，不用 LangChain。

### 风险 2：项目停留在 Demo

解决办法：必须加入 eval、日志、错误处理、部署。

### 风险 3：陷入论文焦虑

解决办法：每读一篇论文，都要问：它能改进我的哪个模块？

### 风险 4：忽略安全

解决办法：所有 agent 项目都写 `SECURITY.md`，明确工具权限。

### 风险 5：没有可量化结果

解决办法：每个项目至少有一个指标，例如准确率、召回率、延迟、成本、任务成功率。

---

## 13. 当前主流资料入口

以下链接用于校准技术路线，建议优先读官方文档。

- OpenAI Agents SDK：<https://platform.openai.com/docs/guides/agents-sdk/>
- OpenAI Agents SDK tracing：<https://openai.github.io/openai-agents-python/tracing/>
- OpenAI Agents SDK JavaScript agents：<https://openai.github.io/openai-agents-js/guides/agents/>
- LangGraph 文档：<https://docs.langchain.com/langgraph>
- LangGraph workflows and agents：<https://docs.langchain.com/oss/python/langgraph/workflows-agents>
- LlamaIndex RAG 入门：<https://docs.llamaindex.ai/en/stable/understanding/rag/>
- LlamaIndex Workflows：<https://docs.llamaindex.ai/en/stable/workflows/>
- Model Context Protocol 官方规范：<https://modelcontextprotocol.io/specification/2024-11-05/basic/index>
- Microsoft Agent Framework：<https://learn.microsoft.com/en-gb/agent-framework/overview/agent-framework-overview>
- Ragas metrics：<https://docs.ragas.io/en/latest/concepts/metrics/available_metrics/>
- OpenTelemetry GenAI semantic conventions：<https://opentelemetry.io/docs/specs/semconv/gen-ai/>
- OWASP Top 10 for LLM Applications：<https://owasp.org/www-project-top-10-for-large-language-model-applications/>

---

## 14. 需要你补充的信息

如果你希望我后续把这份路线进一步个性化，请回答下面问题：

1. 你目前 Python、后端、深度学习分别是什么水平？
2. 你每周能稳定投入多少小时？
3. 你更想找国内岗位、海外岗位，还是都可以？
4. 你偏工程、研究，还是工程研究结合？
5. 你是否已经有 GitHub、论文阅读经验或实习经历？
6. 你导师或课题组是否有固定研究方向？

---

## 15. 最终判断标准

9 到 12 个月后，如果你达到以下状态，就具备比较好的 AI Agent 实习竞争力：

- 能手写最小 agent loop。
- 能做 RAG，并能评测 RAG。
- 熟悉至少一个 agent workflow 框架。
- 能写 MCP server 或接入外部工具。
- 能解释 prompt injection 和 excessive agency。
- 有 2 到 3 个完整 GitHub 项目。
- 有至少 1 个项目带部署、测试、评测和安全说明。
- 能在面试中完整设计一个企业级 agent 系统。

这条路不轻松，但很适合你现在的阶段。你不需要等导师给方向，可以先用项目把能力堆起来，再反过来寻找课题、实习和合作机会。

---

## 16. 根据你当前背景的个性化调整

更新时间：2026-05-18

### 16.1 你的当前画像

你不是零基础转向 AI Agent，而是已经具备比较好的“工程 + 深度学习入门 + 论文阅读”底座：

1. 工程基础  
   你独立用 Django 和 Vue 做过私人博客，并完成过私有服务器部署。这说明你已经理解 Web 应用、前后端交互、数据库、部署流程的基本闭环。后续不需要花太多时间重新学习 Web 入门，应该直接转向 FastAPI、测试、CI/CD、Docker Compose、日志与监控。

2. 深度学习基础  
   你能写 CNN、RNN，并做过音乐分类项目；也系统学过 Transformer、LSTM。这说明你有能力理解 LLM 的核心机制。你的短板不是“模型原理完全不会”，而是缺少 LLM API、tool calling、RAG、agent workflow、评测和生产工程经验。

3. 论文阅读能力  
   你能精读英文论文，这是明显优势。AI Agent 方向变化快，很多能力不是来自教材，而是来自论文、官方文档、开源项目和工程实践。你可以把论文阅读变成项目优化来源，而不是单纯读完做笔记。

4. 求职倾向  
   你偏国内岗位、偏工程方向。因此你的核心竞争力应放在“能落地的 LLM 应用工程能力”，而不是一开始追求纯 agent research。国内实习和校招更看重可运行项目、后端能力、算法基础、工程完整度和业务理解。

### 16.2 新的主线判断

原路线的总体方向不变，但你的节奏可以压缩：

- 不建议从 Python 基础重新学起。
- 不建议长时间停留在传统深度学习复习。
- 不建议一开始做复杂多 agent demo。
- 应该优先补齐测试、CI/CD、FastAPI、RAG 评测、agent observability、安全边界。

你的定制目标应改为：

> 按“基础 agent -> RAG -> workflow -> MCP/安全/可观测性 -> 综合作品集”的顺序逐层推进。每一层都以可运行项目和验收标准作为进入下一层的门槛，而不是按月份机械推进。

### 16.3 模块递进式学习路线

这条路线按知识模块和项目复杂度递进。每个模块都包含：为什么学、学什么、做什么项目、达到什么标准才能进入下一层。

#### 模块 1：LLM 工程基础与最小 Agent

重点不是再学 Python 语法，而是补工程工作流。

为什么先学：

- 这是所有 AI Agent 项目的底座。
- 只有手写过最小 agent loop，后面使用 LangGraph、OpenAI Agents SDK 或其他框架时才不会被抽象牵着走。
- 你已有 Django/Vue/部署经验，所以这一步不需要学 Web 入门，而是直接补 LLM 工程与测试。

学习任务：

- LLM API 基础：messages、system/developer/user prompt、temperature、token、streaming。
- Tool calling：工具 schema、参数校验、工具选择、工具返回。
- Structured output：JSON schema、Pydantic 校验、失败重试。
- Agent loop：observe -> decide -> act -> observe -> answer。
- Python 工程：pytest、fixture、mock、coverage、logging。
- FastAPI：请求响应模型、依赖注入、异常处理。

项目任务：

- 项目名：`mini-tool-agent`
- 把最小 agent 做成 FastAPI 服务。
- 工具至少包含：计算器、文件检索、网页摘要 mock、待办事项管理。
- 每个工具必须有测试。
- agent loop 必须有最大轮数、错误处理、结构化日志。
- 提供 `/chat`、`/tools`、`/health` 接口。

验收标准：

- `pytest` 能稳定通过。
- README 能说明 agent loop。
- 能解释 tool schema 与 Pydantic 校验。
- 能说明模型输出不稳定时如何重试、降级和报错。
- 能把这个服务部署到你的私有服务器或用 Docker 本地启动。

进入下一模块的条件：

- 你能不依赖 agent 框架，手写一个可测试、可调试的工具调用 agent。
- 你能解释“普通 LLM chat”和“能调用工具的 agent”之间的差异。

#### 模块 2：RAG 知识库与检索增强生成

你有论文阅读能力，因此 RAG 项目建议直接围绕论文库做。

为什么接着学：

- 大多数企业 agent 的核心不是“多智能体聊天”，而是“接入业务知识和业务工具”。
- RAG 是 AI Agent 工程岗位最常见的基础能力。
- 你有论文阅读能力，用论文库做 RAG 能同时服务学习、项目和求职展示。

学习任务：

- 文档解析：PDF、Markdown、HTML。
- chunking、metadata、embedding、向量库。
- BM25 + 向量混合检索。
- rerank。
- query rewrite、context packing、引用溯源。
- RAG evaluation：命中率、context precision、answer relevance、faithfulness。

项目任务：

- 项目名：`paper-rag-assistant`
- 数据集用 AI Agent / RAG / LLM security 论文。
- 先用 5 到 10 篇论文做 baseline，再扩展到 30 篇以上。
- 人工构造 80 到 120 条测试问题，分为事实型、比较型、综述型、引用定位型。
- 对比至少 3 组配置：
  - 不同 chunk size。
  - 不同 top-k。
  - 是否 rerank。
- 生成回答时必须带引用来源。

验收标准：

- 项目有 `EVALUATION.md`。
- 能展示检索质量指标。
- 回答必须带引用来源。
- 能解释一次失败回答到底是解析失败、检索失败、上下文组织失败，还是生成失败。
- 能用实验结果说明某个 RAG 参数为什么更好。

进入下一模块的条件：

- 你能构建一个可评测的 RAG pipeline。
- 你能说明 RAG 不能解决的边界，例如知识过期、检索不到、上下文冲突、模型过度推断。

#### 模块 3：Agent Workflow 与任务自动化

这一层开始使用框架，但前提是你已经手写过基础 agent。

为什么接着学：

- 真实 agent 很少只是“问答”，更多是多步骤任务执行。
- Workflow 能让 agent 从随机自由循环变成可追踪、可恢复、可控制的流程。
- 国内岗位中 LangChain/LangGraph 相关要求较常见，值得作为主线框架。

学习任务：

- LangGraph：state、node、edge、checkpoint、human-in-the-loop。
- OpenAI Agents SDK：agent、tool、handoff、guardrail、tracing。
- 选择一个作为主框架，另一个只做对照学习。

建议选择：

- 如果你更想做国内工程岗位，主线优先 LangGraph，因为国内开源项目和岗位 JD 中更常见 LangChain/LangGraph。
- OpenAI Agents SDK 用来理解更原生的 agent 抽象和 tracing。

项目任务：

- 项目名：`research-agent-workflow`
- 输入一个研究主题，自动完成论文检索、阅读清单、论文摘要、方法对比、综述草稿。
- 必须加入人工确认步骤。
- 必须有 trace 日志。
- 必须把 RAG 模块作为一个工具或节点接入，而不是重新写一套散乱逻辑。

验收标准：

- README 有 workflow 图。
- 每个节点职责清晰。
- 能恢复中断任务或保存中间状态。
- 能解释 state graph 相比普通 while loop 的优势。
- 能说明哪些步骤适合模型决策，哪些步骤应该写成确定性代码。

进入下一模块的条件：

- 你能构建一个多步骤 agent workflow。
- 你能在日志或 trace 中复盘一次完整任务的每一步。
- 你能设计 human-in-the-loop 的触发条件。

#### 模块 4：MCP、工具生态、安全与可观测性

这是你和普通 demo 型选手拉开差距的阶段。

为什么接着学：

- 企业真正关心的是 agent 能否安全调用工具、访问数据、留下审计记录。
- MCP、tracing、权限和安全边界能把项目从“玩具 demo”提升到“工程作品”。

学习任务：

- MCP server/client 基本模型。
- OpenTelemetry 或框架 tracing。
- OWASP LLM Top 10。
- prompt injection 与 indirect prompt injection。
- 权限与审计日志。

项目任务：

- 为前面的研究助手增加本地 MCP server。
- 工具包括：论文库查询、笔记读取、任务列表管理。
- 写 `SECURITY.md`，明确哪些工具能自动调用，哪些需要确认。
- 为关键工具调用加入审计日志。
- 准备 prompt injection 和 tool misuse 测试样例。

验收标准：

- 可以讲清楚 agent 工具权限设计。
- 可以演示 prompt injection 测试样例。
- 可以在 trace 中看到模型调用、工具调用、耗时、错误。
- 可以说明 MCP 工具和普通 REST API 工具的取舍。

进入下一模块的条件：

- 你的 agent 不仅能执行任务，还能被观察、被限制、被审计。
- 你能明确说明它的风险边界。

#### 模块 5：综合作品集项目

主项目建议做一个完整的“企业知识库 + 任务处理 Agent”。

为什么最后做：

- 这个项目会综合前面所有模块。
- 它最接近国内 AI Agent / LLM 应用工程岗位的实际业务形态。
- 面试时，一个完整项目比多个零散 demo 更容易讲清楚你的工程能力。

项目定位：

- 后端：FastAPI。
- 前端：Vue 或 React。你已有 Vue 经验，可以继续用 Vue，减少学习成本。
- 数据库：PostgreSQL + pgvector。
- 缓存/任务：Redis。
- Agent：LangGraph。
- RAG：LlamaIndex 或自写 pipeline。
- 部署：Docker Compose。
- CI：GitHub Actions。

必须具备：

- 登录或最小用户系统。
- 文档上传与索引。
- RAG 问答与引用。
- Agent 工具调用。
- 人工确认。
- trace 日志。
- eval 脚本。
- Docker Compose 一键启动。
- README、EVALUATION、SECURITY、DEPLOYMENT。

这个项目比做 5 个小 demo 更有价值。国内面试时，你可以围绕它讲 30 分钟。

验收标准：

- 新用户能按 README 在本地启动项目。
- 项目有一套可复现的 eval 数据。
- 能展示一次完整 agent 执行 trace。
- 能说明权限、安全、成本、延迟和失败恢复策略。
- 简历中能用 3 到 5 条量化描述呈现它。

#### 模块 6：面向招聘的表达与面试能力

这个模块不是最后才开始，而是每完成一个项目就同步积累。

学习任务：

- 算法：LeetCode Hot 100，优先数组、哈希、二分、滑窗、树、图、动态规划基础。
- 后端：FastAPI、数据库索引、事务、Redis、异步任务、Docker。
- LLM 应用设计：RAG、agent workflow、tool calling、安全、评测、成本控制。
- 项目表达：README、架构图、技术博客、Demo 视频、简历 bullet。

验收标准：

- 能 3 分钟讲清项目背景。
- 能 10 分钟讲清技术架构。
- 能 20 到 30 分钟深入讲 RAG、agent workflow、eval、安全和部署。
- 能回答“为什么这样设计，而不是直接调一个大模型 API”。

### 16.4 每周时间安排：按你的工位时间设计

你周一到周五 10:00 到 17:00 在工位，理论上每周有 35 小时。但考虑吃饭、杂事、导师临时任务和状态波动，建议按 22 到 28 小时有效学习设计。

#### 推荐日程

周一：输入与规划

- 10:00-11:00：复盘上周，确定本周目标。
- 11:00-12:00：阅读官方文档。
- 14:00-16:30：实现一个明确的小功能。
- 16:30-17:00：写当天记录。

周二：深度开发

- 10:00-12:00：核心代码开发。
- 14:00-16:30：继续开发 + 本地测试。
- 16:30-17:00：提交 git commit。

周三：测试与工程化

- 10:00-12:00：pytest、mock、错误处理。
- 14:00-15:30：CI/CD 或 Docker。
- 15:30-17:00：整理 README。

周四：论文与项目结合

- 10:00-12:00：精读一篇论文或官方长文。
- 14:00-16:00：把论文中的一个想法转成项目实验。
- 16:00-17:00：记录实验结论。

周五：评测与展示

- 10:00-12:00：跑 eval，记录指标。
- 14:00-15:30：修复本周问题。
- 15:30-17:00：写周报，更新 GitHub。

周末可选：

- 如果状态好，用 2 到 4 小时做算法题或补技术博客。
- 如果状态差，至少做 30 分钟周计划，不强迫硬卷。

### 16.5 你现在最该补的短板排序

优先级从高到低：

1. LLM API 与 tool calling。
2. pytest、mock、coverage。
3. FastAPI 工程结构。
4. RAG pipeline 与评测。
5. LangGraph workflow。
6. Docker Compose。
7. GitHub Actions。
8. Agent 安全与权限。
9. OpenTelemetry/tracing。
10. 国内实习面试算法。

### 16.6 你可以少花时间的内容

以下内容不是不重要，而是短期内投入产出比不高：

- 从零复习 CNN/RNN/LSTM。
- 深入训练大模型。
- 过早研究复杂多 agent 协作。
- 同时学习太多 agent 框架。
- 追逐所有新框架榜单。
- 花太多时间美化前端。

### 16.7 国内岗位准备策略

国内 AI Agent/LLM 应用相关岗位通常会看：

- Python 后端能力。
- FastAPI/Django/Spring Boot 等服务开发经验。
- RAG、LangChain、LangGraph、向量数据库。
- Prompt engineering、tool calling。
- Docker、Linux、Git。
- 算法基础。
- 是否有可展示项目。

你的简历关键词可以围绕：

- AI Agent
- LLM Application
- RAG
- LangGraph
- FastAPI
- PostgreSQL/pgvector
- Docker
- Agent Evaluation
- Prompt Injection Defense
- Tool Calling
- Human-in-the-loop

投递准备按项目成熟度判断，而不是按月份判断：

- 完成模块 1 后：开始收集 JD，建立岗位需求表。
- 完成模块 2 后：可以投递偏 RAG、知识库、LLM 应用的轻量实习或项目合作。
- 完成模块 3 后：可以投递 AI Agent / LangGraph / LLM 应用工程相关实习。
- 完成模块 4 后：简历中可以强调工程可靠性、安全与可观测性，这会明显区别于普通 demo。
- 完成模块 5 后：进入集中投递和模拟面试阶段。

### 16.8 起步任务链：从第一个可运行项目开始

下面不是按自然周安排，而是按任务依赖关系排列。你可以快也可以慢，但不要跳过验收标准。

#### 任务链 1：LLM API 与最小 Agent

目标：

- 搭建 `mini-tool-agent`。
- 实现 tool calling。
- 写 5 到 8 个 pytest。

任务：

- 读一遍模型 API 的 tool calling 文档。
- 写 3 个工具：计算器、笔记搜索、任务管理。
- 写 agent loop。
- 加日志和最大循环次数。

完成标志：

- 命令行可以完成一次工具调用。
- 日志里能看到模型请求、工具名称、工具参数、工具返回。

#### 任务链 2：FastAPI 化与工程结构

目标：

- 把 agent 包装为 Web API。
- 做基础测试和配置管理。

任务：

- 新增 `/chat` 接口。
- 新增 `/tools` 接口。
- 使用 Pydantic 定义请求和响应。
- 用 pytest 测 API。
- 增加 `.env.example`。

完成标志：

- API 测试能通过。
- README 能说明如何启动服务和调用接口。

#### 任务链 3：RAG baseline

目标：

- 从 5 到 10 篇论文或课程资料建立最小 RAG。

任务：

- 文档解析。
- chunking。
- embedding。
- 向量检索。
- 生成带引用回答。

完成标志：

- 输入问题后能返回答案和引用来源。
- 能查看检索到的 chunk 和 metadata。

#### 任务链 4：RAG eval 与 README

目标：

- 让项目从“能跑”变成“可展示”。

任务：

- 人工写 30 条问题。
- 比较 top-k=3、5、8。
- 记录失败案例。
- 写 README 和 EVALUATION。

完成标志：

- 一个最小 agent 服务。
- 一个 RAG baseline。
- pytest 基础经验。
- 一份可以继续扩展的 GitHub 项目。

#### 任务链 5：引入 LangGraph Workflow

目标：

- 把 RAG baseline 和工具调用 agent 组合成一个研究助手 workflow。

任务：

- 设计 state。
- 拆分 planner、retriever、summarizer、writer、reviewer 节点。
- 加入 human approval。
- 保存中间状态。

完成标志：

- README 有 workflow 图。
- 一次完整任务可以被 trace 复盘。

#### 任务链 6：补齐工程化外壳

目标：

- 把项目变成能放进简历的作品。

任务：

- Docker Compose。
- GitHub Actions。
- `SECURITY.md`。
- `DEPLOYMENT.md`。
- Demo 视频或截图。

完成标志：

- 新环境能按文档启动。
- 面试时能围绕项目讲架构、指标、失败案例和改进方向。

### 16.9 给你的学习策略建议

你的优势是能把工程项目做完，所以不要把自己困在“我要先学完所有理论再动手”。更适合你的节奏是：

1. 先做一个能跑的 baseline。
2. 用测试和日志让它稳定。
3. 用论文或文档找一个改进点。
4. 用 eval 证明改进有效。
5. 写进 README 和简历。

完成这些模块后，你的竞争力会非常具体：不是“了解 AI Agent”，而是“做过一个完整 agent 系统，并知道它如何失败、如何评测、如何部署、如何保护权限”。

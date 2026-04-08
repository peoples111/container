## Container v0.3

一款免费 **Local-first** 的支持多模态的大模型桌面工作台：集成大模型部署、管理、对话、搜索下载，蜂群、工具调用（MCP）、RAG 知识库、agent skill、桌面自动化操作, OpenAI 兼容 API 网关，视频通话，语音输入，语音播报，语音识别，长记忆（视觉和文本），人机协作……让本地推理真正可用、可控、可扩展。
把大模型从“一个人聊天”升级为“一个团队工作”： 蜂群多智能体编排 + 工具系统 + 本地推理与 API 网关，一体化交付可执行结果。

### Highlights
- **开箱即用的桌面体验**： Local-first 推理，模型与数据主要在本机处理，延迟低、可控性强聊天（可选免费api，无需部署） + 参数面板 + 控制台 + 资源监控，所有关键状态可视化
<img width="1913" height="1038" alt="image" src="https://github.com/user-attachments/assets/42c4b782-c564-4f3d-8f13-944c4f8d3a12" />
- **OpenAI 兼容 API 网关**：本地应用也能被你的工具链直接调用（SSE 流式、模型列表、embeddings 等）
- **MCP 工具生态**：一键安装自定义工具，基本预设满足日常工作需求
<img width="1928" height="1048" alt="70b302402dd27db73627c70fa22b9d9" src="https://github.com/user-attachments/assets/469fd6cd-b22f-434f-b427-331ad04e268d" />
- **RAG 知识库**：目录/单文件索引、刷新与清理索引、可控召回数量与阈值
- **工作区与检索**：文件树、文本搜索、语义搜索（依赖支持 indexing/search 的 MCP 服务）
- **运行时引擎管理**：管理本地推理引擎（Windows：CUDA / Vulkan / CPU），支持下载、切换版本与额外启动参数

### Core Features
- **模型管理**
  - 支持本地模型导入/删除
  - 集成模型搜索与下载（支持展示模型信息）
<img width="1928" height="1048" alt="1772767140028" src="https://github.com/user-attachments/assets/696ad53c-326d-4754-9cc2-fe4515b402c5" />

- **对话与推理控制**
  - 温度、TopP/TopK、重复惩罚、上下文长度、batch/线程等参数可视化智能配置
  - GPU Offload（含自动/手动策略）、显存压力提示与实际加载层数展示
  - Structured Output：支持 JSON Schema 约束输出
- **多模态与工具**
  - 图片理解：可配置视觉模型
  - 工具调用：支持在对话中手动运行 / 自动触发 MCP 工具
- **语音输入**
  - 支持本地/云端语音转文字（可控配置本地 ASR 引擎）
<img width="1928" height="1048" alt="1772767741450" src="https://github.com/user-attachments/assets/0d4ca017-9894-4ad9-bbe9-e467962b46d0" />

- **网络与安全**
  - 网关支持：端口、CORS、API Key
  - 支持上游转发（Upstream Base URL + Key）与网络代理
<img width="1921" height="1018" alt="1772767207982" src="https://github.com/user-attachments/assets/5ff3bdc6-d9f7-4bd5-87c6-2a83e4be6dc9" />

- **系统可观测性**
  - 底栏实时展示 CPU / RAM / GPU / VRAM 等指标（不同硬件/驱动能力下可能有所差异）
  - **Swarm 蜂群多智能体**
  - 角色编排、层级关系、可视化、导入导出、角色预算控制
<img width="1921" height="1018" alt="1772766604245" src="https://github.com/user-attachments/assets/a24f6b8f-aa44-405a-a38a-255e9578fe16" />
-  **工作区与检索 **
  - 文件树、文本搜索、语义搜索，终端自动化创建项目
<img width="1921" height="1018" alt="1772775062020" src="https://github.com/user-attachments/assets/54503d15-b51e-4da2-aba1-29e52c476c43" />
-  **并发测试**
  - 测试模型能力，优化调参
- **隐私优先（Local-first）**
  -你的对话、提示词、知识库与模型文件默认只保留在本机，我们不做内容采集与用户画像；为保证稳定性，仅在发生异常时上传 最小化 诊断信息用于修复（错误级别/摘要、堆栈、页面路由、客户端版本与基础设备信息），不包含对话内容、文件内容或密钥等私人信息。
v0.3新增功能：
-**人机协作**
  <img width="1921" height="1018" alt="1772775062020" src="https://github.com/peoples111/container/blob/main/202641-202530.png?raw=true" />
-**长记忆（文本和视觉）**
-**视频通话**
-**在线语音播报**
修复大量已知问题，增强国际化适配。
   

### Quick Start
1. 下载并安装：见 Release Assets
2. 打开应用 → 设置模型目录与运行时目录（可选）
3. 在 Models 中导入/下载模型
4. 进入 Chat 页面加载模型并开始对话
5. 如需 API：打开 Server 页面启用网关并配置端口/API Key

### Notes
- 视觉理解、语音、本地 GPU 指标采集等能力受系统环境与驱动影响；建议保持显卡驱动更新。
- 语义搜索需要已安装并启用支持 indexing/search 的 MCP 服务，并先建立索引。

### Changelog
-  V0.3

**Full Changelog**: https://github.com/peoples111/container/commits/llm

Container v0.3
A free, local-first desktop workspace for multimodal large language models: integrating LLM deployment, management, chat, search and download, swarm intelligence, tool calling (MCP), RAG knowledge base, agent skills, desktop automation, OpenAI-compatible API gateway, video calls, voice input, voice synthesis, speech recognition, long-term memory (visual and textual), human-AI collaboration, and more. Making local inference truly usable, controllable, and extensible.
Elevate LLMs from "one-on-one chat" to "a team at work": swarm multi-agent orchestration + tool system + local inference & API gateway, delivering actionable results in one integrated package.
Highlights
Out-of-the-box desktop experience: Local-first inference with models and data processed primarily on your device — low latency, high control. Chat (with optional free APIs, no deployment required) + parameter panel + console + resource monitoring, with all key states visualized.
OpenAI-compatible API gateway: Local applications can be directly called by your toolchain (SSE streaming, model listing, embeddings, etc.)
MCP tool ecosystem: One-click installation of custom tools, with basic presets for daily workflow needs
RAG knowledge base: Directory/single-file indexing, index refresh & cleanup, configurable recall count and thresholds
Workspace & search: File tree, text search, semantic search (requires MCP services supporting indexing/search)
Runtime engine management: Manage local inference engines (Windows: CUDA / Vulkan / CPU), with support for downloading, version switching, and custom launch arguments
Core Features
Model Management
Import/delete local models
Integrated model search and download (with model info display)
Chat & Inference Control
Visual, intelligent configuration of temperature, TopP/TopK, repetition penalty, context length, batch/thread settings
GPU Offload (auto/manual strategies), VRAM usage alerts, and actual layer loading display
Structured Output: output constrained by JSON Schema
Multimodal & Tools
Image understanding: configurable vision models
Tool calling: manual / automatic MCP tool triggering in chat
Voice Input
Local/cloud speech-to-text (configurable local ASR engine)
Network & Security
Gateway support: port, CORS, API Key
Upstream forwarding (Upstream Base URL + Key) and network proxy support
System Observability
Real-time CPU / RAM / GPU / VRAM metrics in the status bar (may vary by hardware/driver)
Swarm Multi-Agent
Role orchestration, hierarchical relationships, visualization, import/export, role budget control
Workspace & Retrieval
File tree, text search, semantic search, terminal automation for project creation
Concurrency Testing
Test model capabilities and optimize parameters
Privacy-First (Local-First)
Your conversations, prompts, knowledge bases, and model files are stored locally by default. No content collection or user profiling is performed. For stability purposes, only minimal diagnostic data (error level/summary, stack trace, page route, client version, and basic device info) is uploaded on crashes — no conversation content, file data, API keys, or private information is included.
New in v0.3
Human-AI Collaboration
Long-term Memory (text & visual)
Video Calls
Online Voice Synthesis
Numerous bug fixes and improved internationalization support.
Quick Start
Download and install: see Release Assets
Launch the app → set model directory and runtime directory (optional)
Import/download models in the Models tab
Go to the Chat page, load a model, and start chatting
For API access: open the Server page, enable the gateway, and configure port/API Key
Notes
Vision understanding, voice features, and local GPU metrics depend on system environment and drivers. Up-to-date graphics drivers are recommended.
Semantic search requires installed and enabled MCP services supporting indexing/search, with indexes pre-built.

Container v0.1
一款 Local-first 的大模型桌面工作台：集成大模型管理、对话、蜂群、工具调用（MCP）、RAG 知识库、工作区自动化任务与 OpenAI 兼容 API 网关，让本地推理真正可用、可控、可扩展。
把大模型从“一个人聊天”升级为“一个团队工作”： 蜂群多智能体编排 + 工具系统 + 本地推理与 API 网关，一体化交付可执行结果。

Highlights
开箱即用的桌面体验： Local-first 推理，模型与数据主要在本机处理，延迟低、可控性强聊天（可选免费api，无需部署） + 参数面板 + 控制台 + 资源监控，所有关键状态可视化![image](https://github.com/peoples111/container/blob/main/20260306134853.png?raw=true) - **OpenAI 兼容 API 网关**：本地应用也能被你的工具链直接调用（SSE 流式、模型列表、embeddings 等） - **MCP 工具生态**：一键安装自定义工具，基本预设满足日常工作需求 70b302402dd27db73627c70fa22b9d9 - **RAG 知识库**：目录/单文件索引、刷新与清理索引、可控召回数量与阈值 - **工作区与检索**：文件树、文本搜索、语义搜索（依赖支持 indexing/search 的 MCP 服务） - **运行时引擎管理**：管理本地推理引擎（Windows：CUDA / Vulkan / CPU），支持下载、切换版本与额外启动参数
Core Features
模型管理
支持本地模型导入/删除
集成模型搜索与下载（支持展示模型信息）
1772767140028
对话与推理控制
温度、TopP/TopK、重复惩罚、上下文长度、batch/线程等参数可视化智能配置
GPU Offload（含自动/手动策略）、显存压力提示与实际加载层数展示
Structured Output：支持 JSON Schema 约束输出
多模态与工具
图片理解：可配置视觉模型
工具调用：支持在对话中手动运行 / 自动触发 MCP 工具
语音输入
支持本地/云端语音转文字（可控配置本地 ASR 引擎）
1772767741450
网络与安全
网关支持：端口、CORS、API Key
支持上游转发（Upstream Base URL + Key）与网络代理
1772767207982
系统可观测性
底栏实时展示 CPU / RAM / GPU / VRAM 等指标（不同硬件/驱动能力下可能有所差异）
Swarm 蜂群多智能体
角色编排、层级关系、可视化、导入导出、角色预算控制
1772766604245 - **工作区与检索 ** - 文件树、文本搜索、语义搜索，终端自动化创建项目 1772775062020 - **并发测试** - 测试模型能力，优化调参 - **隐私优先（Local-first）** -你的对话、提示词、知识库与模型文件默认只保留在本机，我们不做内容采集与用户画像；为保证稳定性，仅在发生异常时上传 最小化 诊断信息用于修复（错误级别/摘要、堆栈、页面路由、客户端版本与基础设备信息），不包含对话内容、文件内容或密钥等私人信息。
Quick Start
下载并安装：见 Release Assets
打开应用 → 设置模型目录与运行时目录（可选）
在 Models 中导入/下载模型
进入 Chat 页面加载模型并开始对话
如需 API：打开 Server 页面启用网关并配置端口/API Key
Notes
视觉理解、语音、本地 GPU 指标采集等能力受系统环境与驱动影响；建议保持显卡驱动更新。
语义搜索需要已安装并启用支持 indexing/search 的 MCP 服务，并先建立索引。
Changelog
V0.1
Full Changelog: https://github.com/peoples111/container/commits/llm

Container v0.1
A Local-first Large Language Model Desktop Workbench: Integrating model management, chat, swarm orchestration, tool calling (MCP), RAG knowledge bases, workspace automation, and an OpenAI-compatible API gateway. We make local inference truly usable, controllable, and scalable.
Upgrade your workflow from "chatting with one AI" to "working with a team."
Container delivers an all-in-one solution combining Swarm multi-agent orchestration, a robust tool system, and local inference/API gateway capabilities to produce executable results.
🌟 Highlights
Out-of-the-Box Desktop Experience:
Local-first Inference: Models and data are processed primarily on your machine for low latency and maximum control.
Flexible Connectivity: Chat using local models or optional free cloud APIs (no deployment required).
Full Visibility: Visualize everything with parameter panels, console logs, and real-time resource monitoring.
OpenAI-Compatible API Gateway:
Seamlessly integrate local models into your existing toolchains. Supports SSE streaming, model listing, embeddings, and more.
MCP Tool Ecosystem:
One-click installation for custom tools. Comes with pre-configured tools to meet daily workflow needs.
RAG Knowledge Base:
Index directories or single files. Full control over index refreshing, cleanup, recall limits, and similarity thresholds.
Workspace & Retrieval:
Integrated file tree, text search, and semantic search (powered by MCP services with indexing/search capabilities).
Runtime Engine Management:
Manage local inference engines seamlessly.
Windows Support: CUDA, Vulkan, and CPU backends.
Features include version switching, download management, and custom startup arguments.
🚀 Core Features
Model Management
Import/Delete: Easily manage local model files.
Discovery: Integrated model search and download with detailed model information cards.
Chat & Inference Control
Visual Parameter Tuning: Intuitive controls for Temperature, Top-P/Top-K, Repetition Penalty, Context Length, Batch Size, and Threads.
GPU Offloading: Smart auto/manual strategies with VRAM pressure warnings and real-time layer loading visualization.
Structured Output: Enforce JSON Schema constraints for reliable programmatic responses.
Multimodal & Tools
Vision: Configurable visual models for image understanding.
Tool Calling: Manually trigger or auto-execute MCP tools directly within the chat flow.
Voice Input
Flexible ASR: Support for both local and cloud-based Speech-to-Text, with configurable local ASR engine options.
Network & Security
Gateway Config: Customizable ports, CORS policies, and API Key management.
Upstream Forwarding: Configure upstream base URLs and keys for proxying requests; supports network proxies.
System Observability
Real-time Metrics: Live dashboard in the footer displaying CPU, RAM, GPU, and VRAM usage (capabilities depend on hardware/drivers).
🐝 Swarm Multi-Agent Orchestration
Role编排 (Role Orchestration): Define agent roles, hierarchical relationships, and interaction flows.
Visualization: Visual graph of agent interactions.
Management: Import/export configurations and set role-specific budget/token limits.
Workspace & Automation
File Operations: File tree navigation, text search, and semantic search.
Terminal Automation: Automatically scaffold and create projects via terminal commands executed by agents.
Concurrency Testing
Built-in tools to stress-test model capabilities and optimize hyperparameters under load.
🔒 Privacy First (Local-first)
Your Data Stays Yours: Conversations, prompts, knowledge bases, and model files remain strictly on your device by default. We do not collect content or build user profiles.
Minimal Diagnostics: To ensure stability, only minimal diagnostic data (error level/summary, stack traces, page route, client version, and basic device info) is uploaded upon crash. No conversation content, file data, or secrets are ever transmitted.
⚡ Quick Start
Download & Install: Grab the installer from the Release Assets.
Setup: Launch the app → Set your Model Directory and Runtime Directory (optional).
Get Models: Go to the Models tab to import existing models or download new ones.
Start Chatting: Navigate to the Chat page, load a model, and begin.
Enable API: Need an API? Go to the Server page, enable the gateway, and configure your Port/API Key.
📝 Notes
Hardware Dependencies: Capabilities like Vision, Voice, and local GPU metrics depend on your system environment and drivers. Please ensure your graphics drivers are up to date.
Semantic Search Requirement: Semantic search requires an installed and enabled MCP service that supports indexing and search. You must build the index before searching.
📅 Changelog
v0.1: Initial Release.

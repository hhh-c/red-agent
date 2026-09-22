# 🛡️ LLM-Agent 自动化红队测试与越狱攻击平台

## 📖 项目简介
随着大语言模型（LLM）向智能体（Agent）演进，模型开始具备调用外部工具（如执行 SQL、读取文件）的能力，这带来了全新的安全风险。本项目是一个针对 LLM Agent 的自动化红队测试平台，旨在通过自动化注入攻击，评估 Agent 在面临恶意提示词时的安全防御能力，防止越狱（Jailbreak）和危险工具调用。

## ✨ 核心功能
- **双模式测试架构**：支持"本地模拟靶场"快速验证，以及"企业真实 API"对接，满足从研发到生产环境的全链路测试需求。
- **可视化攻击界面**：基于 Streamlit 构建的 Web 平台，支持实时输入攻击 Prompt 并观察 Agent 行为。
- **自动化红队引擎**：内置多种经典越狱策略（如 DAN 模式、角色扮演、权限伪造），支持对 Agent 进行批量 Prompt 注入测试。
- **危险工具沙箱**：模拟高危工具（如 SQL 执行、代码执行），安全地捕获 Agent 的违规调用行为。
- **实时安全告警**：自动分析 Agent 输出，若检测到危险工具被触发，立即在界面弹出红色安全警报。

## ️ 技术栈
- **后端/核心逻辑**：Python, LangChain, OpenAI API (兼容通义千问/DeepSeek)
- **前端展示**：Streamlit
- **安全测试**：Prompt Injection, Jailbreak Techniques, Indirect Prompt Injection (规划中)

## 🚀 快速开始

### 1. 克隆项目
```bash
git clone https://github.com/hhh-c/red-agent.git
cd red-agent

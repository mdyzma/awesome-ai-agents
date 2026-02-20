# Awesome AI-Agents [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of AI-powered coding assistants, autonomous agents, and agentic tools that help developers write, review, and understand code. This collection covers everything from command-line interfaces and IDEs to web-based platforms and self-hosted solutions, designed to enhance productivity and transform the way we build software.

AI agents are transforming software development by providing intelligent assistance across the entire development lifecycle. Whether you're looking for a CLI tool to chat with your codebase, an IDE with deep AI integration, or a self-hosted solution for privacy-conscious teams, this list has you covered.

## Contents

- [CLI Tools](#cli-tools)
- [Web-Based Chat Interfaces](#web-based-chat-interfaces)
- [AI-Enhanced IDEs & Editors](#ai-enhanced-ides--editors)
- [Web UI Agents & Frameworks](#web-ui-agents--frameworks)
- [Self-Hosted Solutions](#self-hosted-solutions)
- [Agent Skills & Resources](#agent-skills--resources)
- [Development Frameworks](#development-frameworks)
- [Other Notable Tools](#other-notable-tools)
- [Contributing](#contributing)

## CLI Tools

Command-line AI assistants that bring powerful AI capabilities directly to your terminal.

- [Aider](https://github.com/Aider-AI/aider) - AI pair programming in your terminal with Git integration and multi-file editing support.
- [Claude-CLI](https://github.com/dvcrn/anthropic-cli) - Command-line interface for Anthropic's Claude API with image support and customizable parameters.
- [Codex](https://github.com/openai/codex) - OpenAI's lightweight coding agent that converts natural language to code and runs locally.
- [Copilot CLI](https://github.com/features/copilot/cli) - GitHub's AI-powered command-line assistant for generating shell commands.
- [Gemini CLI](https://github.com/google-gemini/gemini-cli) - Google's terminal-based AI agent with powerful code understanding and GitHub Actions integration.
- [Goose CLI](https://github.com/block/goose) - Open-source local AI agent by Block with extensible MCP server support and customizable autonomy.
- [OpenCode](https://github.com/anomalyco/opencode) - Open-source AI coding agent available as CLI, desktop app, and IDE extension with 75+ LLM providers support.
- [Plandex](https://github.com/plandex-ai/plandex) - Terminal-based AI designed for large projects with 2M+ token context window and multi-step task planning.
- [QwenCode](https://github.com/QwenLM/qwen-code) - Terminal AI agent optimized for Qwen3-Coder models with IDE integration and agentic workflows.

## Web-Based Chat Interfaces

Browser-based AI chat platforms for conversational coding assistance.

- [ChatGPT](https://chat.openai.com) - OpenAI's conversational AI with code generation, debugging, and explanation capabilities.
- [Claude](https://claude.ai) - Anthropic's AI assistant with strong coding abilities and large context windows.
- [Gemini](https://gemini.google.com) - Google's multimodal AI with code understanding and generation features.
- [Grok](https://grok.x.ai) - X's AI assistant with real-time information access and coding capabilities.
- [Z.ai](https://z.ai) - AI-powered assistant focused on productivity and code-related tasks.

## AI-Enhanced IDEs & Editors

Integrated development environments and code editors with deep AI integration for seamless workflows.

**Standalone IDEs:**

- [Claude Code](https://claude.com/code) - Anthropic's IDE-integrated coding environment with agentic capabilities and cloud/local execution.
- [Cursor](https://cursor.sh) - AI-first code editor built on VS Code with codebase-aware chat and multi-file reasoning.
- [OpenCode Desktop](https://opencode.ai/download) - Open-source desktop IDE supporting 75+ LLM providers with GitHub Copilot and ChatGPT integration.
- [Windsurf](https://windsurf.com) - AI-native IDE with Cascade feature for deep codebase understanding and autonomous coding.
- [Zed](https://zed.dev) - High-performance Rust-built editor with AI integration, real-time collaboration, and agentic editing.

**IDE Plugins & Extensions:**

- [Cline](https://github.com/cline/cline) - VS Code extension for AI-powered coding assistance.
- [GitHub Copilot](https://github.com/features/copilot) - AI pair programmer that suggests code in real-time across multiple editors.

## Web UI Agents & Frameworks

Browser-based autonomous agents and frameworks for automating web tasks and building AI-powered workflows.

**End-User Tools:**

- [AgentGPT](https://agentgpt.reworkd.ai) - Autonomous AI agents deployable directly in your browser for complex tasks.
- [Bardeen](https://www.bardeen.ai) - Browser automation extension with AI-powered workflow builder and data scraping.
- [BrowserAgent](https://browseragent.dev) - Privacy-first Chrome extension for running local AI agents with no-code workflow builder.
- [Fellou AI](https://fellou.ai) - Self-driving browser for automating multi-step tasks with AI workflow intervention.
- [Project Mariner](https://deepmind.google/models/project-mariner/) - Google DeepMind's research prototype for human-agent interaction in browsers.
- [Web-UI](https://github.com/browser-use/web-ui) - User-friendly browser interface for AI agents built on browser-use framework.
- [Zapier Agents](https://zapier.com/agents) - Chrome extension integrating personalized AI agents into webpages for automation.

**Frameworks & Libraries:**

- [Browser-Use](https://github.com/browser-use/browser-use) - Open-source framework making websites accessible for AI agents.
- [LaVague](https://github.com/lavague-ai/LaVague) - Control web browsers using natural language with text language models.
- [Mastra](https://mastra.ai) - TypeScript framework for building agents, workflows, and browser automation.
- [OpenManus](https://github.com/openmanus/openmanus) - Multi-agent system for complex tasks with browser interaction capabilities.
- [Skyvern-AI](https://github.com/Skyvern-AI/skyvern) - Browser control framework using visual language models and natural language.
- [Stagehand](https://github.com/browserbase/stagehand) - Framework for building robust web agents with serverless browser support.
- [UI-TARS](https://github.com/bytedance/UI-TARS) - Multimodal AI agent stack with GUI control for terminals, computers, and browsers.

## Self-Hosted Solutions

Privacy-focused platforms for running AI agents and chat interfaces locally or on private infrastructure.

**Chat Platforms:**

- [AnythingLLM](https://github.com/Mintplex-Labs/anything-llm) - All-in-one AI application with RAG, multiple LLM support, and private ChatGPT-like experience.
- [OpenWebUI](https://github.com/open-webui/open-webui) - Extensible self-hosted AI platform with offline capability and built-in RAG support.

**Local Model Runtimes:**

- [LM Studio](https://lmstudio.ai) - Desktop application for running and chatting with local language models.
- [Ollama](https://ollama.ai) - Local LLM platform with easy model management and API access.

## Agent Skills & Resources

Repositories, protocols, and resources for extending agent capabilities with modular skills.

- [Agent Skills Specification](https://github.com/skillmatic-ai/awesome-agent-skills) - Definitive resource for modular, standardized SKILL.md packages for AI agents.
- [Awesome OpenClaw Skills](https://aiagentstore.ai/awesome-openclaw-skills) - Curated catalog of community-built skills for OpenClaw organized by category.
- [Claude Code Skills](https://code.claude.com/docs/en/skills) - Official Claude skills documentation and templates.
- [Claw Tasks](https://clawtasks.com) - Platform for discovering and sharing agent task definitions.
- [MCP Market](https://mcpmarket.com) - Discover Model Context Protocol servers for connecting AI clients to tools.
- [Microsoft AI Skills](https://github.com/microsoft/skills) - Skills, MCP servers, and configurations for Azure SDKs and Microsoft AI Foundry.
- [Skillcreator AI](https://github.com/skillcreatorai/Awesome-Agent-Skills) - Universal skill repository compatible with various AI coding agents.
- [VoltAgent Skills](https://github.com/VoltAgent/awesome-agent-skills) - 300+ agent skills from official teams and community for multiple platforms.

## Development Frameworks

Frameworks and SDKs for building custom AI agents, workflows, and agentic applications.

- [LangChain](https://github.com/langchain-ai/langchain) - Framework for developing applications powered by LLMs with chains, agents, and memory.
- [LangGraph](https://github.com/langchain-ai/langgraph) - Framework for building stateful, multi-actor applications with LLMs.
- [LiteLLM](https://github.com/BerriAI/litellm) - Unified API for calling 100+ LLMs with OpenAI-compatible format and built-in observability.
- [Langflow](https://langflow.org) - Low-code AI builder for constructing agents and MCP servers with visual interface.
- [Deep Agents](https://docs.langchain.com/oss/python/deepagents/overview#deep-agents-overview) - Building agents with task planning, file systems for context management and subagent-spawning.
- [OpenAI AgentKit](https://platform.openai.com/docs/agents) - Tools for building agentic workflows with visual Agent Builder and Agents SDK.

## Other Notable Tools

Additional platforms, services, and research projects in the AI agent ecosystem.

**Research Projects:**

- [Agent0 Series](https://github.com/agent0-series/agent0) - Research initiative on self-evolving agents that improve without human-curated datasets.
- [Project Mariner](https://deepmind.google/discover/blog/project-mariner/) - Google DeepMind's research prototype exploring advanced human-agent interaction.

**Development Platforms:**

- [GitHub Agentic Workflows](https://github.blog/changelog/agentic-workflows) - AI agents running within GitHub Actions for repository automation.
- [Google AI Studio](https://ai.google.dev/aistudio) - Google's platform for prototyping with generative AI models.
- [OpenRouter](https://openrouter.ai) - Unified API for accessing 200+ LLMs from multiple providers with built-in fallbacks and loadbalancing.

**Autonomous Agents:**

- [OpenClaw](https://github.com/openclaw/openclaw) - Free open-source autonomous AI agent with 50+ messaging platform integrations.
- [ZeroClaw](https://github.com/zeroclaw-labs/zeroclaw) - Fast, lightweight autonomous AI assistant infrastructure written in Rust for self-hosted deployments.

**AI-Powered Tools:**

- [NotebookLM](https://notebooklm.google.com) - AI-powered research and note-taking assistant from Google.
- [Perplexity](https://www.perplexity.ai) - AI-powered search engine with conversational interface and citation support.

## Contributing

Contributions are welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

When contributing:

- Ensure your suggestion is not already listed
- Check that the tool/resource is actively maintained
- Use the following format: `[Name](link) - Description.`
- Add new entries in alphabetical order within their category
- Descriptions should be concise (one line) and start with a capital letter

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related rights to this work.

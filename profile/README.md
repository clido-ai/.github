# cli;do

An AI coding agent that runs in your terminal.

It reads your codebase, edits files, runs commands, and iterates — using any LLM you want.

```bash
curl -fsSL https://raw.githubusercontent.com/clido-ai/clido-cli/master/scripts/install.sh | sh
```

## What it does

clido operates directly on your repository. It can read and write files, execute shell commands, search code semantically, and chain multiple steps together to complete tasks autonomously.

It keeps persistent sessions — you can close the terminal, come back later, and pick up where you left off with full context.

## How it works

You talk to an agent in a TUI. The agent has access to 23 built-in tools (file I/O, bash, grep, glob, semantic search, web fetch, and more). It decides what to do, asks for permission when needed, and executes.

For recurring tasks, you can define YAML workflows — multi-step plans the agent follows without manual prompting.

## Providers

clido is not locked to a single API. Pick whatever model fits the task:

| Provider | | Provider | |
|---|---|---|---|
| Anthropic | Claude 3.5/4 | Groq | Llama, Mixtral |
| OpenAI | GPT-4o/o1/o3 | Together | Open models |
| Google | Gemini 2.5 | Fireworks | Open models |
| DeepSeek | DeepSeek V3/R1 | Cerebras | Fast inference |
| Mistral | Mistral Large/Codestral | Perplexity | Online models |
| xAI | Grok | MiniMax | |
| OpenRouter | 200+ models | Alibaba/Qwen | Qwen 2.5/3 |
| Ollama | Local models | Kimi | Moonshot |

Two-tier routing lets you assign a fast, cheap model for simple tool calls (renaming, formatting) and a stronger model for reasoning — in the same session.

## What makes it different

- **Single binary.** One download, no runtime, no package manager. Written in Rust.
- **Provider-agnostic.** 16 providers, local models via Ollama, switch with a flag.
- **Persistent sessions.** Resume any conversation. Context survives restarts.
- **YAML workflows.** Declarative automation — define steps, inputs, conditions.
- **MCP support.** Extend the agent with external tool servers.
- **Permissioned.** Four permission modes from full-auto to ask-every-time. Secret scanning built in.

## Links

- **Repository:** [clido-ai/clido-cli](https://github.com/clido-ai/clido-cli)
- **Documentation:** [clido-ai/docs](https://github.com/clido-ai/docs)

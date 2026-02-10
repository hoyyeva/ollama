<p align="center">
  <img src="https://github.com/ollama/ollama/assets/3325447/0d0b44e2-8f4a-4e99-9b52-a5c1c741c8f7" alt="ollama" width="200"/>
</p>

# Ollama

Start building with open models.

<a href="https://ollama.com">Website</a> · <a href="https://docs.ollama.com">Documentation</a> · <a href="https://discord.gg/ollama">Discord</a> · <a href="https://reddit.com/r/ollama">Reddit</a>

## Download Ollama

### macOS

```
curl -fsSL https://ollama.com/install.sh | sh
```

### Windows

[Download](https://ollama.com/download/OllamaSetup.exe)

### Linux

```
curl -fsSL https://ollama.com/install.sh | sh
```

[Manual install instructions](https://docs.ollama.com/linux#manual-install)

### Docker

The official [Ollama Docker image](https://hub.docker.com/r/ollama/ollama) `ollama/ollama` is available on Docker Hub.

## Get started

### Coding

Use `ollama launch` to quickly get started with an AI-powered coding assistant:

```
ollama launch
```

To launch a specific integration:

```
ollama launch claude-code
```

Supported integrations include [Claude Code](https://docs.ollama.com/integrations/claude-code), [Codex](https://docs.ollama.com/integrations/codex), [Droid](https://docs.ollama.com/integrations/droid), and [OpenCode](https://docs.ollama.com/integrations/opencode).

### AI assistant

Use [OpenClaw](https://docs.ollama.com/integrations/openclaw) to turn Ollama into a personal AI assistant across WhatsApp, Telegram, Slack, Discord, and more:

```
ollama launch openclaw
```

### Chat with a model

Run and chat with [Gemma 3](https://ollama.com/library/gemma3):

```
ollama run gemma3
```

See [ollama.com/library](https://ollama.com/library) for the full list of available models.

See the [quickstart guide](https://docs.ollama.com/quickstart) for more details.

### REST API

Ollama has a REST API for running and managing models.

```
curl http://localhost:11434/api/chat -d '{
  "model": "gemma3",
  "messages": [{
    "role": "user",
    "content": "Why is the sky blue?"
  }],
  "stream": false
}'
```

See the [API documentation](https://docs.ollama.com/api) for all endpoints.

## Build with Ollama

**Python**

```
pip install ollama
```

```python
from ollama import chat

response = chat(model='gemma3', messages=[
  {
    'role': 'user',
    'content': 'Why is the sky blue?',
  },
])
print(response.message.content)
```

**JavaScript**

```
npm i ollama
```

```javascript
import ollama from 'ollama'

const response = await ollama.chat({
  model: 'gemma3',
  messages: [{ role: 'user', content: 'Why is the sky blue?' }],
})
console.log(response.message.content)
```

Libraries: [Python](https://github.com/ollama/ollama-python) · [JavaScript](https://github.com/ollama/ollama-js)

## Documentation

- [Quickstart guide](https://docs.ollama.com/quickstart)
- [Model library](https://ollama.com/library)
- [CLI reference](https://docs.ollama.com/cli)
- [REST API reference](https://docs.ollama.com/api)
- [Importing models](https://docs.ollama.com/import)
- [Modelfile reference](https://docs.ollama.com/modelfile)
- [Community integrations](https://docs.ollama.com/integrations)
- [Building from source](https://github.com/ollama/ollama/blob/main/docs/development.md)

## Community

- [Discord](https://discord.gg/ollama)
- [Reddit](https://reddit.com/r/ollama)

<p align="center">
  <img alt="Ollama" height="200" src="https://raw.githubusercontent.com/ai-action/assets/master/logos/ollama.svg">
</p>

# ollama-action

[![version](https://img.shields.io/github/release/ai-action/ollama-action)](https://github.com/ai-action/ollama-action/releases)
[![test](https://github.com/ai-action/ollama-action/actions/workflows/test.yml/badge.svg)](https://github.com/ai-action/ollama-action/actions/workflows/test.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

🦙 Run [Ollama](https://ollama.com/) large language models (LLMs) with GitHub Actions.

## Quick Start

```yaml
# .github/workflows/ollama.yml
on: push
jobs:
  ollama:
    runs-on: ubuntu-latest
    steps:
      - name: Run model
        uses: ai-action/ollama-action@v1
        id: model
        with:
          model: llama3.2
          prompt: Explain the basics of machine learning.

      - name: Print response
        run: echo "$response"
        env:
          response: ${{ steps.model.outputs.response }}
```

## Usage

Run a prompt against a [model](https://ollama.com/library):

```yaml
- uses: ai-action/ollama-action@v1
  id: explanation
  with:
    model: tinyllama
    prompt: "What's a large language model?"

- run: echo "$response"
  env:
    response: ${{ steps.explanation.outputs.response }}
```

See [action.yml](action.yml)

## Inputs

### `model`

**Required**: The language [model](https://ollama.com/library) to use.

```yaml
- uses: ai-action/ollama-action@v1
  with:
    model: llama3.2
```

### `prompt`

**Required**: The input prompt to generate the text from.

```yaml
- uses: ai-action/ollama-action@v1
  with:
    prompt: Tell me a joke.
```

To set a multiline prompt:

```yaml
- uses: ai-action/ollama-action@v1
  with:
    prompt: |
      Tell me
      a joke.
```

### `version`

**Optional**: The [Ollama version](https://github.com/ai-action/setup-ollama#version). See all available [versions](https://github.com/ollama/ollama/releases).

```yaml
- uses: ai-action/ollama-action@v1
  with:
    version: 0.9.5
```

### `cache`

**Optional**: Whether to cache the model. Defaults to `false`.

```yaml
- uses: ai-action/ollama-action@v1
  with:
    cache: true
```

## Outputs

### `response`

The generated response message.

```yaml
- uses: ai-action/ollama-action@v1
  id: answer
  with:
    model: llama3.2
    prompt: What's 1+1?

- run: echo "$response"
  env:
    response: ${{ steps.answer.outputs.response }}
```

> [!NOTE]
> The environment variable is wrapped in double quotes to preserve newlines.

## Articles

- [Generating useful titles for automated PRs in GitHub Actions](https://jacobtomlinson.dev/posts/2025/generating-useful-titles-for-automated-prs-in-github-actions/)
- [How to run Ollama LLM on GitHub Actions](https://medium.com/@remarkablemark/how-to-run-ollama-large-language-models-llm-on-github-actions-for-free-bb4219d09a29)

## License

[MIT](LICENSE)

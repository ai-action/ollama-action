# Changelog

## [2.0.0](https://github.com/ai-action/ollama-action/compare/v1.1.1...v2.0.0) (2025-12-22)


### ⚠ BREAKING CHANGES

* **action:** set action input `cache` default to true
* **action:** bump Node.js runtime from 20 to 24

### Performance Improvements

* **action:** default cache to true ([34a4030](https://github.com/ai-action/ollama-action/commit/34a403083dd54b66aa378dbeb64cdef6cb83765f))


### Build System

* **deps:** bump actions/cache from 4 to 5 ([#17](https://github.com/ai-action/ollama-action/issues/17)) ([a825720](https://github.com/ai-action/ollama-action/commit/a82572041f9d8462ce5e70565dbc2c1d7324d59f))
* **deps:** bump ai-action/setup-ollama from 1 to 2 ([#19](https://github.com/ai-action/ollama-action/issues/19)) ([c730764](https://github.com/ai-action/ollama-action/commit/c7307649ae9d15ee2562cbdcc5ad9cdb4ce7b5c7))

## [1.1.1](https://github.com/ai-action/ollama-action/compare/v1.1.0...v1.1.1) (2025-07-04)


### Bug Fixes

* **action:** add if conditional for version ([30f00d8](https://github.com/ai-action/ollama-action/commit/30f00d8f13b57e6a5a590af8a82be58dca428e54)), closes [#8](https://github.com/ai-action/ollama-action/issues/8)

## [1.1.0](https://github.com/ai-action/ollama-action/compare/v1.0.1...v1.1.0) (2025-04-30)


### Features

* **action:** cache model with optional input `cache` (defaults to true) ([4600a6a](https://github.com/ai-action/ollama-action/commit/4600a6af8f47d6f18e067ed68320b52cb0d153db))

## [1.0.1](https://github.com/ai-action/ollama-action/compare/v1.0.0...v1.0.1) (2025-04-29)


### Bug Fixes

* **action:** escape special characters from the prompt ([#4](https://github.com/ai-action/ollama-action/issues/4)) ([419f734](https://github.com/ai-action/ollama-action/commit/419f734a60a0b7ab7f218fed27cea24cf91947e7))

## 1.0.0 (2025-02-23)

### Features

* **action:** run ollama ([039b120](https://github.com/ai-action/ollama-action/commit/039b12036e6d3e1d8b926624432829beba0e88d5))

# Plugins

このディレクトリには、外部リポジトリで管理されている Copilot AI Agent 向けプラグインを Git submodule として配置します。

- ここにソースコードを直接コミットしない
- それぞれのプラグインは独立した Git リポジトリで管理する
- `marketplace.json` から参照される構成にする

例:

- `plugins/hnuma1979/springboot-copilot/`

各 submodule は、個別のリポジトリの更新をトラッキングします。
- repo: https://github.com/hnuma1979/springboot-copilot

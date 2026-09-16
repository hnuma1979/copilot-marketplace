# hnuma1979 Copilot Marketplace

このリポジトリは、Copilot AI Agent 向けのプラグイン情報を管理するマーケットプレイスです。

## このリポジトリの役割

- プラグインのメタデータを管理する
- 一覧情報を提供する
- 各プラグインの実体は別リポジトリで管理する

基本方針として、マーケットプレイス本体は「登録簿」または「カタログ」であり、実際のプラグインコードは別リポジトリに置く構成が推奨です。

## ディレクトリ構成

```text
.
├── README.md
├── marketplace.json
├── .gitmodules
├── plugins/
│   └── README.md
└── plugins/hnuma1979/springboot-copilot/   # Git submodule
```

## プラグインの管理方式

## 外部リポジトリでプラグインを管理する場合の marketplace.json の記載例

```json
{
  "name": "hnuma1979/springboot-copilot",
  "displayName": "Spring Boot Reactive JDBC Plugin",
  "description": "A Spring Boot plugin for reactive JDBC operations",
  "repository": "https://github.com/hnuma1979/springboot-copilot",
  "source": {
    "source": "github",
    "repo": "hnuma1979/springboot-copilot",
    // 外部リポジトリは path を書かない
    // "path": "plugins/hnuma1979/springboot-copilot"
  }
}
```

## 注意点
- プラグインの実装コードをこのマーケットプレイスリポジトリにそのまま置くのは、
  修正の影響範囲を狭めるためです。

## 参照先
- 各プラグインの GitHub リポジトリ
- 各プラグインの README
- marketplace.json に記載されている `repository` と `source` フィールド

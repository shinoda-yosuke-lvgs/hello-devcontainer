<h1 align="center">
    <br/>🐳 Hello Dev Container 🐳<br/><br/>
</h1>

## 使い方

## 環境構築系コマンド実装時のポリシー

### devcontainerのonCreateCommnd等で実行するコマンド

### sheldonのinlineCommand等で実行するコマンド

## パッケージ導入時のポリシー

### miseで管理するパッケージ

- バージョンを考慮する必要があるパッケージ。
- CI/CDで使うパッケージ。

### devcontainerのfeaturesで管理するパッケージ

- バージョンを考慮する必要がないパッケージ。
- CI/CDで使わないパッケージ。
- なるべくDev Container Spec Maintainers(`ghcr.io/devcontainers/features/*`)から提供されるパッケージ。

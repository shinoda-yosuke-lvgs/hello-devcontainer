<h1 align="center">
    <br/>🐳 Hello Dev Container 🐳<br/><br/>
</h1>

## パッケージ導入時のポリシー

### miseで管理するパッケージ

- バージョンを考慮する必要があるパッケージ。
- CI/CDで使うパッケージ。

### devcontainerのfeaturesで管理するパッケージ

- バージョンを考慮する必要がないパッケージ。
- CI/CDで使わないパッケージ。
- なるべくDev Container Spec Maintainers(`ghcr.io/devcontainers/features/*`)から提供されるパッケージ。

<div style="text-align:center;">
<sapn style="font-size:40px">🐳Hello Dev Container🐳</span>
</div>

## パッケージインストール時のポリシー

### miseで管理するパッケージ

- バージョンを考慮する必要があるパッケージ。
- CI/CDで使うパッケージ。

### devcontainerのfeaturesで管理するパッケージ

- バージョンを考慮する必要がないパッケージ。
- CI/CDで使わないパッケージ。
- なるべくDev Container Spec Maintainers(`ghcr.io/devcontainers/features/*`)から提供されるパッケージ。

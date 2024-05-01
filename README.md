<h1 align="center">
    <br/>🐳 Hello Dev Container 🐳<br/><br/>
</h1>

## 使い方

- クラウド環境で作業する場合
    
    [![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/shinoda-yosuke-lvgs/hello-devcontainer?quickstart=1)

- ローカル環境で作業する場合
    
    <a href="https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/shinoda-yosuke-lvgs/hello-devcontainer"><img src="https://img.shields.io/badge/Open_in_VS_Code-blue?logo=visualstudiocode" height="32px"></a>

    <details>
    <summary>上記ボタンから開けない場合</summary>

    ```bash
    git clone https://github.com/shinoda-yosuke-lvgs/hello-devcontainer hello-devcontainer &&
    devcontainer open hello-devcontainer
    ```
    </details>

## 環境構築系コマンド実装時のポリシー

### devcontainerのonCreateCommnd等で実行するコマンド

- 必要最低限に留める。

### sheldonのinlineCommand等で実行するコマンド

- complitionなどはsheldonで実行させる。

## パッケージ導入時のポリシー

### miseで管理するパッケージ

- バージョンを考慮する必要があるパッケージ。
- CI/CDで使うパッケージ。
- 管理しやすいので基本miseに寄せる。

### devcontainerのfeaturesで管理するパッケージ

- ビルドに時間が増加するのでなるべく使わない。
- dockerなどのインストールの手間がかかるパッケージ。
- なるべくDev Container Spec Maintainers(`ghcr.io/devcontainers/features/*`)から提供されるパッケージだけにする。

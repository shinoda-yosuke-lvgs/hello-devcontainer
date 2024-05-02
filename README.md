<h1 align="center">
    <br/>🐳 Hello Dev Container 🐳<br/><br/>
</h1>

## 💫 クイックスタート

<div align="center">

**↓ ブラウザ上で開発する場合 ↓**
    
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/shinoda-yosuke-lvgs/hello-devcontainer?quickstart=1)

**↓ VSCodeで開発する場合 ↓**
    
<a href="https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/shinoda-yosuke-lvgs/hello-devcontainer"><img src="https://img.shields.io/badge/Open_in_VS_Code-blue?logo=visualstudiocode" height="32px"></a>

</div>
<br>

<details>
<summary>上記ボタンから開けなかった場合</summary>

```bash
git clone https://github.com/shinoda-yosuke-lvgs/hello-devcontainer hello-devcontainer && devcontainer open hello-devcontainer
```
</details>

<br>

## 🧩 構成

```mermaid
%%{init: {'theme':'neutral'}}%%
block-beta
  columns 8

  block:feature1:2
    columns 3
    awscli githubcli["github-cli"] terraform node rust go
  end
    
  block:feature2:2
    zshplugins["*.plugin.zsh"]
  end

  block:feature3:2
    nginx
    postgresql
    pgadmin
  end

  space:2

  space:8

  mise["mise（ランタイム管理）"]:2
  sheldon["sheldon（プラグイン管理）"]:2
  dind["docker（docker in docker）"]:2
  sshd["sshd"]:1
  space:1

  ubuntu["ubuntu（ベースイメージ）"]:7
  space:1

  mise --> feature1
  sheldon --> feature2
  dind --> feature3
```

<br>

- ubuntuのイメージ上で動きます
- [.mise.toml](./.mise.toml)で定義しているツールがインストールされます
- [.sheldon/plugins.zsh.toml](./.sheldon/plugins.zsh.toml)で定義しているプラグインがターミナルを開いた際に反映されます
- docker in dockerでdevcontainer上でdockerを使えるようにしています
- sshdを立ち上げておきます（codespace使用時にローカルマシンから`gh codespace ssh`コマンドで接続できるようになります）

## 🔰 チュートリアル

- `mise`で管理されたコマンドはすぐに使えます
    - `aws --version`
    - `gh --version`
    - `terraform version`
    - `node --version`
    - `rustc --version`
    - `go version`
    - `docker version`

- `tabキー`による補完がある程度機能します

- `examples`ディレクトリに各言語の動作確認用のサンプルがあります
    - [docker](./examples/docker/README.md)
    - [go](./examples/go/README.md)
    - [node](./examples/node/README.md)
    - [rust](./examples/rust/README.md)

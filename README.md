<h1 align="center">
    <br/>🐳 Hello Dev Container 🐳<br/><br/>
</h1>

## 💫　クイックスタート

**🌐 ブラウザ上で開発する場合**
    
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/shinoda-yosuke-lvgs/hello-devcontainer?quickstart=1)

**💻 VSCodeで開発する場合**
    
<a href="https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/shinoda-yosuke-lvgs/hello-devcontainer"><img src="https://img.shields.io/badge/Open_in_VS_Code-blue?logo=visualstudiocode" height="32px"></a>

<details>
<summary>上記ボタンから開けない場合</summary>

```bash
git clone https://github.com/shinoda-yosuke-lvgs/hello-devcontainer hello-devcontainer && devcontainer open hello-devcontainer
```
</details>

## 📝 構成イメージ

```mermaid
block-beta
  columns 2

  block:s1:1
    awscli githubcli["github-cli"] terraform node rust go
  end
    
  block:s2:1
    zshplugins["*.plugin.zsh"]
  end

  space:2

  mise["mise（ランタイム管理）"]:1
  sheldon["sheldon（プラグイン管理）"]:1
  ubuntu["ubuntu（ベースイメージ） + docker in docker"]:2

  mise --> s1
  sheldon --> s2
```

## 🔰 説明書

- 起動した時点でmiseで管理されたコマンドが使えるようになっています
    - `aws --version`
    - `gh --version`
    - `terraform version`
    - `node --version`
    - `rustc --version`
    - `go version`
    - `docker version`
- 起動した時点で`tabキー`による補完がある程度機能します

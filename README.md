# python-devcontainers

VSCode Dev Containers を用いて Python の学習環境を構築するためのチュートリアルです。

## 環境構築

以下のソフトウェアを PC にインストールしてください。

- [Docker Desktop](https://www.docker.com/ja-jp/products/docker-desktop/) : Docker 環境を構築・利用するためのツールです。

- [VS Code](https://code.visualstudio.com/download) : コードを編集するエディタです。拡張機能を使うと、開発に便利な機能を追加することができます。

- [Dev Containers 拡張機能(VS Code)](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) : VS Code から Docker コンテナに接続するためのツールです。


## 環境構築の手順

1. このレポジトリをダウンロードします。

2. VS Code を起動し、フォルダを開きます。

3. VS Code の左下にある緑色の「><」アイコン（もしくは、リモートウィンドウのアイコン）をクリックします。

4. 表示されるメニューから 「コンテナで再度開く」 を選択します。

## 設定ファイルの説明

```
.
├── .devcontainer
│   ├── Dockerfile
│   └── devcontainer.json
└── main.py
```

devcontainer.json では、dockerFile として、Dockerfile を指定する。

```
{
    "name": "minimal Python environment",
    "dockerFile": "Dockerfile"
}
```

Dockerfile では、コンテナで使う Docker イメージを指定します・

FROM でイメージを python:3 と指定します。また、エラー情報などをすぐに出力するように ENV PYTHONUNBUFFERED 1 とします。

```
FROM python:3 
ENV PYTHONUNBUFFERED 1 
```

## ライセンス

MIT

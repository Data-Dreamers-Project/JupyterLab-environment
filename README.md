# JupyterLab-environment

- Dockerによって構成された、JupyterLab開発環境テンプレートです。


## 使い方

1. Docker DesktopとDocker Composeのインストール


1. このリポジトリをクローン
    ```bash
    git clone https://github.com/Data-Dreamers-Project/JupyterLab-environment.git
    ```

1. リポジトリへ移動
    ```bash
    cd JupyterLab-environment
    ```

1. Dockerコンテナの起動
   - `docker-compose.yml`があるディレクトリで以下を実行
    ```bash
    docker compose up -d
    ```

1. 作業スペースへのアクセス
   - ブラウザで http://localhost:8888/ へアクセス

## 終了方法

1. Dockerコンテナの停止
    ```bash
    docker compose down
    ```


## 主なフォルダ説明
```
.
├── py3                     : Python3のJupyterLab環境
│   ├── Dockerfile          : JupyterLabの環境を構築するためのDockerfile
│   └── root_jupyter        : JupyterLabの設定を永続化させるためのフォルダ
├── workspace               : JupyterLabの作業スペース (外部からファイルを追加するときはここに追加する)
└── docker-compose.yml      : Dockerコンテナの設定ファイル
```

### 重要なフォルダ
- `workspace` : 
    JupyterLabの作業スペース、データセットやソースコードの置き場所
- `py3/root_jupyter` : 
    JupyterLabの設定ファイルが入っている、dockerコンテナを落としてもここにファイルがあるのでフォントの変更やフォーマッターの指定等の設定は消えない

## コントリビューション

- Projectメンバーの方はコミュニティーリーダーの指示に従うか[`CONTRIBUTING.md`](CONTRIBUTING.md)をご覧ください。
- それ以外の方は、[`CONTRIBUTING.md`](CONTRIBUTING.md)をご覧ください。

## 参考文献

- [Docker実践ガイド: コンテナ環境の構築・運用・活用](https://ndlsearch.ndl.go.jp/books/R100000002-I032642811)    
- [DockerでJupyterLabの環境を作ろう](https://www.idnet.co.jp/column/page_187.html)
    > 本リポジトリでは、ベースイメージのバージョンをPython3.9系から3.11.8のDebian系にしている。


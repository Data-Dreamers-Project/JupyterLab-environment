# JupyterLab-environment

- JupyterLab開発環境です。
- インポートして使うことを想定しますが、使い方は自由です。
    - [リポジトリのインポートについて](https://docs.github.com/ja/migrations/importing-source-code/using-github-importer/importing-a-repository-with-github-importer)
    - ここでいう"インポート"とは、任意のリポジトリをベースに新しいリポジトリを作成できる機能を指します。
    - [インポート用リンク](https://github.com/new/import)
    

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
   - プロジェクトルート(`docker-compose.yml`があるディレクトリ)で以下を実行
    ```bash
    # ./JupyterLab-environment
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

- プロジェクトメンバーの方はコミュニティーリーダーの指示に従ってください。
- それ以外の方は、ISSUEを立ててください。

## 参考文献

- [Docker実践ガイド: コンテナ環境の構築・運用・活用](https://ndlsearch.ndl.go.jp/books/R100000002-I032642811)    
- [DockerでJupyterLabの環境を作ろう](https://www.idnet.co.jp/column/page_187.html)
    > 本リポジトリでは、ベースイメージのバージョンをPython3.9系から3.11.8のDebian系にしている。


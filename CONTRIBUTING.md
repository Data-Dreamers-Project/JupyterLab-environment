# コントリビューションガイドライン

このプロジェクトへの貢献を検討していただき、ありがとうございます！以下のガイドラインをお読みいただき、プロジェクトへの貢献をスムーズに進めてください。

## 開発環境のセットアップ

1. このリポジトリをクローンします。
    ```bash
    git clone https://github.com/Data-Dreamers-Project/JupyterLab-environment.git
    ```

2. リポジトリへ移動します。
    ```bash
    cd JupyterLab-environment
    ```

3. Dockerコンテナを起動します。
    ```bash
    docker compose up -d
    ```

## Issueの作成

問題を見つけたり、新しい機能の提案がある場合は、まず新しいIssueを作成してください。
その際、問題の詳細や機能の提案内容を具体的に記述してください。
Issueテンプレートは[こちら](.github/ISSUE_TEMPLATE/bug_report.md)と[こちら](.github/ISSUE_TEMPLATE/feature_request.md)をご参照ください。

## Pull Requestの作成

1. リポジトリをフォークします。
2. 新しいブランチを作成します（例：`feature/{追加する機能の名前}`）。
3. 変更をコミットします。
4. ブランチをGitHubにプッシュします。
5. GitHub上で新しいPull Requestを作成します。

## コードのスタイルガイド

- PythonのコードはPEP 8に従ってください。
- コミットメッセージは明確で理解しやすいものにしてください。(`add`や`delete`、`update`、等のprefixをつけると良い場合が多いです)

## ライセンス

このプロジェクトはMITライセンスの下で公開されています。詳細は[LICENSE](LICENSE)を参照してください。

## お問い合わせ

何か質問がある場合、DataDreamersメンバーの場合、コミュニティーリーダーに従ってください。
それ以外の方は、新しいIssueを作成してください。
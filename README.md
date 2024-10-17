# web_dev_workflow

ウェブ制作会社のworkflowボイラープレート

## 導入

このリポジトリからfork,ダウンロード
またはプロジェクトのルートで以下のコマンド（プロジェクトルートの.github/workflow/内に同盟のファイルがあるとコンフリクトします。）

```bash
bun create monosus/web_dev_workflow .
```

## 1. issue~ブランチ〜PR作成フロー

GitHubのリポジトリ画面での操作です。

issueに誰かをアサイン（以下の順序2の段階）のリモートのmainブランチからissueブランチを作成します。

1. 人がやる:issueを作成
2. 人がやる:issueに誰かをアサイン
3. botがやる:issueナンバーでブランチを作成（issue-12）
4. botがやる:issueに対応するPRをドラフト状態で作成する（PRテンプレートも挿入される）
5. botがやる:issueにブランチへのチェックアウトコマンドをコメントする
　


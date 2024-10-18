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
　
## 2. 非推奨：コミットメッセージをaiで生成

[openCommit](https://github.com/di-sukharev/opencommit)をGitHub Actionsに導入しましたが、

workflow毎にリモートとローカル間でcommit messageに関しての差分が出るため作業フローがそこまで簡素化できませんでした。  
ただし、openCommitを有用なプラグインですので導入をオススメします。似たようなもので[aicommits](https://github.com/Nutlope/aicommits)もあります。  
openCommitのほうがemojiを簡単に使えたりして楽しいと思います。（openAiのapi_keyは各々で用意する必要があります。）

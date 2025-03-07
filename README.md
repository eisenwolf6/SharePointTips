# プロジェクト名：SharePointTips

## 初めてのプロジェクトを作成し、リポジトリ連携する
- git initでローカルリポジトリを作る
- git addでステージングエリアに登録
- git commitでGitディレクトリに登録
- gitLabでプロジェクトを作成
- git remote add origin (https://github.com/eisenwolf6/SharePointTips.git)でローカルリポジトリとリモートリポジトリを連携
  - git remote rm origin　リモートリポジトリをローカルリポジトリから削除（よく使う。別のプロジェクトで作業する時）
  - git remote -v（リモートリポジトリの割り当て状況確認）
- git push origin main(origin：関連付けたリモートリポジトリの名称 main：リモートリポジトリのブランチ名)
  - 失敗する。リモートリポジトリにREADME.mdがあり、ローカルと異なるため
- git fetch originでリモートリポジトリの最新の変更を取得（まだワークツリーには反映されない！）
- git merge origin/main -allow-unrelated-histories(ワークツリーに反映)
  - 新しいプロジェクトを開始する際に、既存のリポジトリを投稿する場合
  - 異なるリポジトリから履歴を持つブランチをマージする場合
- git push origin main（今度は成功）
- git log origin/main..mainでリモートとローカルの差分が表示される
  - ..は範囲指定演算子で後ろのmainがローカルリポジトリのmainブランチ

### プルリクエストを試す
- プルリクエストからマージまでの動作を確認
  - ちなみにボッチプルリクエスト、マージも可能
  - デフォルトがマージ時に作成したトピックブランチを削除するものになっているので、そのチェックは外した方がいいかも

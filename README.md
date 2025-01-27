# プロジェクト名：SharePointTips

# 初めてのプロジェクト
- git initでローカルリポジトリを作る
- git addでステージングエリアに登録
- git commitでGitディレクトリに登録
- gitLabでプロジェクトを作成
- git remote add origin ssh://GitLabSSH/TM03209/SharePointTips.gitでローカルリポジトリとリモートリポジトリを連携
  -git remote rm origin　リモートリポジトリをローカルリポジトリから削除（よく使いそう）
- git push origin main(origin：関連付けたリモートリポジトリの名称 main：リモートリポジトリのブランチ名)
  -失敗する。リモートリポジトリにREADME.mdがあり、ローカルと異なるため
- git fetch originでリモートリポジトリの最新の変更を取得（まだワークツリーには反映されない！）
- git merge origin/main -allow-unrelated-histories(ワークツリーに反映)
  - 新しいプロジェクトを開始する際に、既存のリポジトリを投稿する場合
  - 異なるリポジトリから履歴を持つブランチをマージする場合
- git push origin main（今度は成功）
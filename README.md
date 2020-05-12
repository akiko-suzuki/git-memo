# git-memo


## github(リモートリポジトリ)をclone

1. GitHubで作成したリモートリポジトリをローカルにクローンする。 (ソースのフォルダをつくりたいディレクトリで)

    git clone https://github.com/akiko-suzuki/git-memo.git
    
    URLは↓↓↓からコピペ<br>
    <img width="427" alt="スクリーンショット 2020-05-07 13 36 22" src="https://user-images.githubusercontent.com/53561761/81255229-1f0a7900-9068-11ea-8298-26a1e3c97db9.png"><br>
    (実行後：Cloning into 'git-memo'...
    warning: You appear to have cloned an empty repository.
    中が空だとこうなる。)


## 新規ブランチ作成 〜 リモートにプッシュ

1. masterブランチで git pull　（リモートの最新の状態と合わせる）
2. masterブランチから git checkout -b ブランチ名　（例:create/index.html）
3. 作成したブランチで作業
4. git statusでローカルの状況確認　（作成、修正したファイルが見れる）
5. git diff 作成したファイル　(差分の確認)
6. git add 作成したファイル
7. git commit -m”コミットメッセージ”
8. git push origin 作成したブランチ名


## Pull Requests作成方法

1. githubでPR作成 （マージ先を確認）
2. 作業内容や注意点を書く
3. create pull request ポチ
4. レビュワーの指定


## リモートのmasterブランチにマージ

1. git checkout master
2. git pull origin master (他の誰かがmasterブランチを更新しているかもしれないから)
3. git merge 作成したブランチ
4. git push origin master


## ローカルブランチを削除する

### マージ済みのブランチのみ削除

1. git branch　（ローカルブランチの確認）
2. git branch -d ブランチ名

### マージされていないブランチを削除したいとき

1. git branch -D ブランチ名　（どんなローカルブランチも削除できる）


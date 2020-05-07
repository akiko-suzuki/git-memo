# git-memo

## github(リモートリポジトリ)とローカルを同期

1. githubと連携する新しく作ったディレクトリに移動。今回は git-memo

    - cd git-memo
    
2. ローカルリポジトリの生成
    
    - git init
    (実行後:Initialized empty Git repository in /Users/akiko/git-memo/.git/)

3. GitHubで作成したリモートリポジトリをローカルにクローンして同期する。

    - git clone https://github.com/akiko-suzuki/git-memo.git
    
    URLは↓↓↓からコピペ<br>
    <img width="427" alt="スクリーンショット 2020-05-07 13 36 22" src="https://user-images.githubusercontent.com/53561761/81255229-1f0a7900-9068-11ea-8298-26a1e3c97db9.png"><br>
    (実行後：Cloning into 'git-memo'...
    warning: You appear to have cloned an empty repository.
    中が空だとこうなる。)


## 新規ブランチ作成 〜 リモートにプッシュ

1. masterブランチで - git pull（リモートの最新の状態と合わせる）
2. masterブランチから - git checkout -b ブランチ名　（例:create/index.html）
3. 作成したブランチで作業
4. - git statusでローカルの状況確認　（作成、修正したファイルが見れる）
5. - git diff 作成したファイル　(差分の確認)
6. - git add 作成したファイル
7. - git commit -m”コミットメッセージ”
8. - git push origin 作成したブランチ名


## Pull Requests作成方法

1. githubでPR作成 （マージ先を確認）
2. 作業内容や注意点を書く
3. create pull request ポチ
4. レビュワーの指定


## リモートのmasterブランチにマージ

1. - git checkout master
2. - git pull origin master (他の誰かがmasterブランチを更新しているかもしれないから)
3. - git merge 作成したブランチ
4. - git push origin master



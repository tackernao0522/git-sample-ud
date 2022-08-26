## addしてないコードを消したい

+ `Local` (workingTree) (add)=> `staging` (commit)=> `save`<br>

(VSCodeのソース管理からでも消せる)<br>
+ 新規作成ファイルを消す<br>
`git clean -f <ファイル名><br>

+ ファイル変更を取り消す<br>
git restore <フォルダ/ファイル> // ファイル取り消し<br>
git restore . // add全て取消<br>

## addを取り消したい

(VSCodeのソース管理からでも消せる) `-`をクリックする<br>

+ `git restore --staged <フォルダ/ファイル>` // ファイル取消<br>

+ `git restore --staged .` // add全て取消<br>

+ `git reset <ファイル>` // ファイルの取り消し<br>

+ `git reset` // addを全て取消<br>

+ commitを取り消したい

+ HEAD : 現在の場所<br>

+ resetはcommitをなかったことにする<br>

+ `git reset --soft HEAD^` (stagingの状態までaddはされている状態 HEADをcommit idでも記述可能 一つ前のIDを入れる)<br>

+ `git reset --mixed HEAD^` (stagingを飛ばしてコードを書いている状態まで addされていない状態である)<br>

+ `git reset --hard HEAD^` (コードを書いている状態もなくす)<br>

## pushを取り消したい

+ Remote側: コミット履歴を残す場合
`git revert <commitID>` <br>
`git push` // 取消コミットのプッシュ<br>

+ Local側: コミット履歴を残さない場合<br>
`git reset --soft <commitID>`<br>
`git push -f` // 強制プッシュ<br>

#### resetとrevert

resetはコミット毎削除<br>

revertは打ち消しコミットを作る<br>

## pull requestを取り消したい

プルリク前後に取り消す（マージ前 Compare & pull requestのバーが出てる時）branchごと消える<br>
`git push --delete origin <branch名>`<br>

プルリク出した後（取り消すとclosedになる）<br>

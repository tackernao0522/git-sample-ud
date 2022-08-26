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

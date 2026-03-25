---
name: update-index
description: jigsawable_*.html を走査して index.html のゲーム一覧を更新する
user_invocable: true
---

# index.html 更新スキル

以下の手順で index.html を更新してください。

1. プロジェクトルートにある `jigsawable_*.html` ファイルを Glob で取得する
2. 各ファイルの `<title>` タグからゲーム名を取得する（例: `<title>Jigsawable Maze</title>` → `Maze`）。`<title>` が見つからない場合はファイル名から `jigsawable_` と `.html` を除いた部分を先頭大文字にして使う
3. ファイル名のアルファベット順でソートする
4. `index.html` の `<div class="games">` と `</div>` の間を、取得したゲームへのリンク一覧で置き換える。リンクの形式: `<a href="ファイル名">ゲーム名</a>`
5. 更新結果（何件のゲームがリストされたか）を報告する

# チャイナダイニング 喰う喰う 公式サイト

公開URL: https://kuukuu-zushi.github.io/ （GitHub Pages / main ブランチをそのまま公開）

## 更新のルール（オーナーの指示）

- オーナーから「こうして」と変更を頼まれたら、確認を待たずに変更し、**main ブランチに直接コミットして push してよい**（オーナーが恒常的に許可済み）。セッション用の作業ブランチが指定されていても、このリポジトリでは main に反映する。
- push の前に必ず GitHub の get_me で接続アカウントが `kuukuu-zushi` であることを確認する。違うアカウントなら push せず止めてオーナーに伝える。
- コミットの作成者・コミッターは必ず次にする（個人名・個人メールは入れない）:
  - `git -c user.name="kuukuu-zushi" -c user.email="357259525+kuukuu-zushi@users.noreply.github.com" commit ...`
- サイトにもリポジトリにも、kuukuu-zushi 以外の個人の GitHub アカウント名・個人メールアドレス・PC のユーザー名を入れない。
  - 旧サイトは「別アカウント名.github.io/kuukuu-zushi.com/」という URL だった。`github.io/kuukuu-zushi.com` を含む URL を見つけたら `https://kuukuu-zushi.github.io/` に置き換える。
  - オーナーから届く zip 等に `.claude/` フォルダ（PC の設定ファイル）が入っていても、リポジトリには入れない。
- push 前に、変更したファイルに上記の個人情報が含まれていないか grep で確認する。
- push 後は Actions の「pages build and deployment」が success になったか確認し、結果を短く日本語で報告する。

## 構成

- `index.html` … ページ本体（店舗情報・メニュー・構造化データ・OGP）
- `css/` `js/` … デザインと動き
- `config/notice.js` … お知らせバナーの内容（告知の変更はここ）
- `img/` … 画像（ページは `img/` から読み込む）
- `robots.txt` `sitemap.xml` … 検索エンジン用。内容を更新したら sitemap の lastmod も更新する。
- 店舗情報（営業時間・定休日・電話・価格）を変えるときは、本文・フッター・構造化データ（JSON-LD）・FAQ の全箇所をそろえて直す。

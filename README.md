# 計算物理領域ホームページ

## ホームページ

* https://www.cp.div.jps.or.jp/
* https://compphys-jp.github.io/ (上のアドレスから自動的に転送される)

## GitHub リポジトリ

* プライベートリポジトリ: https://github.com/compphys-jp/compphys-jp.github.io-dev
  - 作業・確認はこちらで行う
* パブリックリポジトリ: * プライベートリポジトリ: https://github.com/compphys-jp/compphys-jp.github.io
  - こちらの`main`ブランチにpushすると自動的に公開される

* cloneの方法

  ```sh
  git clone git@github.com:compphys-jp/compphys-jp.github.io-dev.git
  git remote add public git@github.com:compphys-jp/compphys-jp.github.io.git
  ```

## 編集手順

* おしらせ

  - `_post`の下に`YYYY-MM-DD-xxxx.md`という名前のファイルを作る
  - ヘッダで`title`と`date`を設定。`date`が未来の場合、トップページに表示されなので注意
  - `date`が新しい順にトップページにリストされる

* 計算物理領域メーリングリスト

  - `mailinglist.md`を編集

* 領域運営内規

  - `bylaws.md`を編集

* 領域代表・運営委員

  - `members.md`を編集

* メニューへの追加

  - `_config.yml`を編集

## プレビュー

* Dockerが必要
* `docker-compose up`を実行
* ブラウザで http://localhost:4000 にアクセスする
* Ctrl-Cで中断

## 公開

* 修正内容を`git commit`
* `git push origin main` (この段階ではまだ公開されない)
* `git push public main`
  - 2,3分すると公開される
  - ログは https://github.com/compphys-jp/compphys-jp.github.io/actions

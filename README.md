# isucon-template
isuconのテンプレート用

## 初動(Set up)

**Makefileの取得と変数設定**

サーバー上で Makefile を取得するため実行

```shell
curl https://raw.githubusercontent.com/Dorayaki-World/isucon-template/blob/main/Makefile -o Makefile
```

問題によって変わる変数 の部分を適切に設定する

```shell
vi Makefile
```

**サーバーの初期設定**

- percona-toolkit(for pt-query-digest), alp, netdata などの計測に必要なツールを install
- git の設定・ssh-keyの生成

```shell
make set-up
```

**remote repository との接続**

```shell
cat ~/.ssh/id_ed25519.pub
```

で出力した公開鍵をisucon用リポジトリの deploy key に設定し、remote repository に反映する

## 計測


## 参考

- https://github.com/oribe1115/traP-isucon-newbie-handson2022/tree/main
- https://github.com/oribe1115/isucon12-qualify/tree/main

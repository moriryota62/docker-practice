# Docker practice
## まえがき
Docker practiceはこれからDockerに入門する方を対象とした問題集です。dockerコマンドの基本的な使い方、Dockerfileによるコンテナイメージのビルド方法、docker-composeによるコンテナの起動方法など、Dockerの基本を抑えることを目的としています。テーマごとに動作や使い方を学ぶ問題を用意しています。問題の指示や公式ドキュメントを参考に自身で考えながら進めてください。

## 前提
Dockerおよびdocker-composeをインストールしてありDocker Hubに接続できる端末で実施する前提です。また、一部のプラクティスは2台のサーバを使用します。

なお、インストールの方法については以下の公式マニュアル等を確認ください。
- [dockerエンジン](https://docs.docker.com/engine/install/)
- [docker-compose](https://docs.docker.com/compose/install/)

また、WSLの環境でDockerを使えるようにするには以下のQiitaなどが参考になると思います。
- [WSLでdockerのインストールからdocker-composeまで動かす](https://qiita.com/tettsu__/items/85c96850d187e4386c24)

# プラクティスの内容

プラクティス内の``{ホストOS名}``など{}でくくった日本語の箇所は括弧内の日本語に従い置換してください。

## コンテナの基本
- [コンテナの起動](./container/container-run.md)
- コンテナの特徴（時間がある人向け）
  - [ホストOS上の隔離空間であるということ](./container/container-feature-isolation.md)
  - [一時的であるということ](./container/container-feature-ephemeral.md)
  - [どこでも同じものが動くということ](./container/container-feature-reproducibility.md)
- [コンテナへのアクセス](./container/container-access.md)
- [コンテナにファイルシステムをマウント](./container/container-volume.md)
- [コンテナに環境変数を設定](./container/container-env.md)
- [コンテナのログ](./container/container-log.md)
- [まとめ](./container/container-summary.md)

## コンテナイメージの基本
- [イメージの取得/削除](./image/image-operation.md)
- [イメージレジストリ](./image/image-registry.md)
- [イメージの作成](./image/image-build.md)
- [まとめ](./image/image-summary.md)
- [イメージの手動運搬](./image/image-transport.md)（興味のある人向け）

## docker-composeの基本
- [docker-composeによるコンテナ起動](./compose/compose-run.md)
- [docker-composeによるネットワーク作成](./compose/compose-network.md)
- [docker-composeによる複数コンテナの連携](./compose/compose-multi.md)
- [まとめ](./compose/compose-summary.md)

## dockerデーモンの設定（マニュアルのリンクだけ紹介）
- [dockerデーモンの設定](http://docs.docker.jp/engine/reference/commandline/daemon.html)

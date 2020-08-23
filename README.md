# Docker practice
## まえがき
Docker practiceはこれからDockerに入門する方を対象とした問題集です。dockerコマンドの基本的な使い方、Dockerfileによるコンテナイメージのビルド方法、docker-composeによるコンテナの起動方法などDockerの基本を抑えることを目的としています。テーマごとに動作や使い方を学ぶ問題を用意しています。問題の指示や公式ドキュメントを参考に自身で考えながら進めてください。

## 前提
Dockerおよびdocker-composeをインストールしてありDocker Hubに接続できる端末で実施する前提です。

# プラクティスの内容
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
- コンテナイメージの操作
- コンテナイメージの作成

## docker-composeの基本
- docker-composeによるコンテナ起動
- docker-composeによる複数コンテナの連携

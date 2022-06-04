# Dockerについて学んだことメモ

## Dockerイメージを使うには？
- Dockerイメージを使用するにはDocker Hubから `docker hub`コマンドでダウンロードするか
`docker build`コマンドを使用し自分で作成する。

## イメージのダウンロード
- dockerイメージにはタグという概念があり、1つのイメージに対して複数のタグを割り当てることが可能で
コマンド⇨ `docker pull イメージ名 タグ名` 。
タグ名を省略すると自動的にlatestのタグが適用される。
docker.io/library/hello-world:latest
⇨docker.io(レジストリDockerHub)、名前空間(イメージを格納するレポジトリ)はlibrary(公式イメージ)の中のhello-worldイメージのlatest(最新版)をpullしたことになる。
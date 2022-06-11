# Kubernetes

コンテナ化の当初の目的はプログラムを壊さずにデプロイするためのもの。

ポッド = VM のようなもの

Kubernetes を起動するユーザーが httpd コンテナを起動して外部公開しなさいというと、
Conrtol Planes であるマスターノードに Nodes のワーカーノードが Service と Pod を作成しろという。
すると、Nodes に iptables のルールが追加される。

## リソース

- Node
  ワーカーノードのことを言う。
  k8s では Node でコンテナが動作するマシンを管理する。
  - コンテナランタイム
  - kubelet
  - kube-proxy
- Pod
  - Pod = コンテナだと思って良い。しかし Pod というべきところをコンテナと表現しているところもある。
  - コンテナを連携させたいようなことがある。Pod には複数のコンテナを酸化させることができる。
  - Kubernetes では Pod を最小単位とする。
  - より詳細に見ると Pod には次のものが含まれる。コンテナ、ネットワーキング(Pod の Ip アドレス)、Pod 内の共有ストレージ
- ReplicaSet
  - Pod のレプリカを作成し、指定した数の Pod を維持し続けるリソースである。
  - Kubernetes は障害時にコンテナを自動復旧するがそれを行う仕組みがレプリカセット。
  - Pod が死んでしまってもレプリカ数(ReplicaSet)になるように Pod 数を補う。
- Deployment
  - ReplicaSet を管理する。
- Service

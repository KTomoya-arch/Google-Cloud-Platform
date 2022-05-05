## CI/CDパイプライン
- CI
CIはJenkinsやCircleCIにも含まれている
- CD
Cloud Buildをしようして新しいイメージを作成してContarinerRegistry,ArtifactRegistryに保存する
- DeploymentManager
Cloud Storage バケット、PubSub
- CloudMonitoring
デプロイしたアプリの動きは監視できる

## コンテナと仮想化
コンテナ化はOSのみを抽象化している

## Cloud Build
ビルドパイプラインを設定し、Dockerコンテナイメージを作成し、Container Registryへイメージをpushできる
またCloud BuildのビルドステータスをPub/Subへ通知することができ、そのステータスまたは他の属性に基づいてアクションを実施することができる

## DeploymentManager
- 役割
インフラの作成、作成済みのインフラの管理、インフラの削除
メリット:様々な環境に応じてテンプレートを再利用して個別にリソースを構成できる
- 複雑な例
yamlファイルを組み合わせた動的テンプレートを使える
python jinjaテンプレート、パラメータに基づいたリソースの作成が可能

## Cloud Functions
- イベントドリブン、サーバレスでスケーラブルなアプリを開発できる

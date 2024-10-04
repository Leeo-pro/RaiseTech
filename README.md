# RaiseTechのAWSフルコース課題提出用リポジトリ

## 概要
こちらのリポジトリでは上記のAWSコースで学習したことをアウトプットしたものである。<br>
Webアプリがどのように動いているかを学習し、AWSで環境構築し、<br>
最終的に、今まで構築してきた環境を全て「コード化」しました。<br>
特に、コード化を行ったCircleCIで以下の動作を自動処理するようにしています。<br>

## 自動構築の流れ
CircleCIを使用して次のようにインフラストラクチャを自動構築した。
1. CloudFormationでVPC・EC2・RDS・ALB・S3のAWS環境を自動構築
2. Ansibleでサーバーの構成をコード化し、サーバー構築とアプリのデプロイを自動化
3. Serverspecで構築したサーバーに対して自動でテスト

## 構成図
![AWS構成図](images/system_configuration.png)

## 講義内容
|講義番号|学習テーマ|学習内容|提出物|
|:---:|---|---|---|
|1|Railsアプリケーションの起動<br>（第1~3回講座）|- AWSアカウント作成<br>- IAM設定<br>- Cloud9作成|ー|
|2||- GitHubアカウントを作成<br>- リポジトリ作成からプルリクエスト実施|[lecture02.md](./lecture02.md)|
|3||- Railsアプリケーションのデプロイ<br>- APサーバー,DBサーバーについて|[lecture03.md](./lecture03.md)|
|4|AWS上でのネットワークの手動構築とアプリ起動<br>（第4~9回講座）|- VPC,EC2,RDSの作成<br>- EC2とRDSの接続確認|[lecture04.md](./lecture04.md)|
|5||- EC2でのアプリケーションのデプロイ<br>- ALB,S3組込み<br>- 構成図の作成|[lecture05.md](./lecture05.md)|
|6||- CloudTrailのイベント確認<br>- CloudWatchアラームの設定<br>- AWS利用料見積|[lecture06.md](./lecture06.md)|
|7||- AWSセキュリティ対策|[lecture07.md](./lecture07.md)|
|8||- 第4・5回講義課題の実演|ー|
|9||- 第4・5回講義課題の実演|ー|
|10|これまでの環境を自動構築<br>（第10~15回講座）|- AWS環境のコード化(CloudFormation)|[lecture10.md](./lecture10.md)|
|11||- 第5回作成のEC2へテスト(ServerSpec)|[lecture11.md](./lecture11.md)|
|12||- CircleCIでサンプルコンフィグを起動|[lecture12.md](./lecture12.md)|
|13||- CircleCiでCloudFormation、Ansible、ServerSpecを自動で実行|[lecture13.md](./lecture13.md)|
|14||- 第14回講義課題の実演<br>- AWS構成図と自動化処理がわかる図を作成<br>- README作成|ー|
|15||- 第14回講義課題の実演|ー|
|16|エンジニアとしての心得|- 現場で必要なスキルと心持ちについて|ー|
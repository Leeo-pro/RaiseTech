# 第13回課題

### CircleCIにCloudFormationやServerSpec、Ansibleの処理を加えて実行<br>
* CircleCIのコンソールにて、環境変数を設定（設定例）<br>
- AWS_ACCESS_KEY_ID(アクセスキー)<br>
- AWS_SECRET_ACCESS_KEY(シークレットアクセスキー)<br>
- AWS_DEFAULT_REGION(リージョン)<br>
- AWS_DB_PW(RDSのパスワード)<br><br>

## CloudFormationのテンプレートを使用しスタックの作成<br>
* CircleCIにCloudFormationテンプレートを実行する処理<br>
![処理結果](images/lecture13/CloudFormation.png)<br><br>

## Ansible-Playbookの作成<br>
* CircleCIにAnsibleのPlaybookを実行する処理<br>
![処理結果](images/lecture13/Ansible.png)<br><br>

## Serverspecによるテスト実行<br>
* CircleCIにServerspecのテストを実行する処理<br>  
![処理結果](images/lecture13/Serverspec.png)<br><br>

## CircleCI結果（参考）<br>
![全体の処理結果](images/lecture13/CircleCI.png)<br><br>

## ALBのDNS名経由でアプリが正常に動作していることの確認<br>
![動作確認](images/lecture13/APP_CHECK.png)<br><br>

※これまでの課題と別のリポジトリを作成し検証  

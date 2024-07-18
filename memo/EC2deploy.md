# 第5回課題メモ
## 組み込みサーバーでデプロイ
- EC2に接続
- sudo yum updateを実行

$ sudo yum update -y
- Gitのインストール

$ sudo yum install git
- rbenvをインストール

$ git clone https://github.com/rbenv/rbenv.git ~/.rbenv
$ echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile
$ echo 'eval "$(rbenv init -)"' >> ~/.bash_profile
$ source ~/.bash_profile
- rbenvのインストールを確認
$ rbenv -v
- ruby-buildのインストール
$ git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build
$ cd ~/.rbenv/plugins/ruby-build
$ sudo ./install.sh
$ cd ..
- rubyに必要なパッケージをインストール
$ sudo yum -y install gcc-c++ glibc-headers openssl-devel readline libyaml-devel 	readline-devel zlib zlib-devel libffi-devel libxml2 libxslt libxml2-devel libxslt-devel 	sqlite-devel
- rbenvでバージョン(x.x.x)を指定してRubyをインストール
$ rbenv install x.x.x
$ rbenv global x.x.x
$ rbenv -v
- Bundlerをバージョン(x.x.x)を指定してインストール
$ gem install bundler -v x.x.x
$ bundler -v
Railsをバージョン(x.x.x)を指定してインストール
$ gem install rails -v x.x.x
$ rails -v
- Node Version Manager (NVM) をインストール
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
$ source ~/.bashrc
- Node.jsをバージョン(x.x.x)を指定してインストール
$ nvm install 17.9.1
$ node -v
- yarnをバージョン(x.x.x)を指定してインストール
# npmはnvmインストール時にインストールされている
$ npm install -global yarn@1.22.19
$ yarn -v
- サンプルアプリケーションをクローン
$ git clone "sample_application"
- インスタンス作成初期からインストールされているMariaDB用パッケージを削除する
# mariaDBを削除しておかないとmysql動作時エラーが生じる
$ sudo yum remove -y mariadb-*
- MySQLのリポジトリをyumに追加
$ sudo yum localinstall -y 	https://dev.mysql.com/get/mysql80-community-release-el7-11.noarch.rpm
- MySQLに必要なパッケージを取得
$ sudo yum install -y --enablerepo=mysql80-community mysql-community-server
$ sudo yum install -y --enablerepo=mysql80-community mysql-community-devel
- インストールされたMySQLに関係のあるパッケージを確認
$ yum list installed | grep mysql
- mysqlのlogファイルを作成
$ sudo touch /var/log/mysqld.log
- mysqlを起動
$ sudo systemctl start mysqld
- mysqlの状態を確認
$ systemctl status mysqld.service
- mysqlがインスタンスの起動と同時に起動するように設定
$ sudo systemctl enable mysqld
- mysqlの初期パスワードの確認
$ sudo cat /var/log/mysqld.log | grep "temporary password"

- ログイン確認
$ mysql -u root -p
Enter password: パスワードを入力 # パスワードは入力しても表示されない
- mysqlのパスワードを変更する
mysql> ALTER USER 'root'@'localhost' IDENTIFIED BY '新しいパスワード';
mysql> FLUSH PRIVILEGES;
# exit or ctrl+Dでmysqlから抜ける
- サンプルアプリへディレクトリの移動
$ cd ./raisetech-live8-sample-app

- データベースの編集
$ cp config/database.yml.sample config/database.yml
$ nano config/database.yml
- database.ymlに追加、または、編集
host: RDSのエンドポイント
port: RDSのポート
username: RDSのユーザ－ネ－ム
password: RDSのパスワード
- 環境構築
$ bin/setup
- 組み込みサーバーを走らせる
$ bin/dev
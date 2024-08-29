# 第11回課題

## Serverspecを使用してテスト検証
* サンプルコードを使ってSeverspecのテストを実施
* [サンプルコード](https://github.com/MasatoshiMizumoto/raisetech_documents/tree/main/aws/samples/serverspec)
* [公式 doc](https://serverspec.org/)

## 流れ
* serverspecのインストール<br>
$ gem install serverspec<br><br>

* 作業ディレクトリへ移動<br><br>

* 初期設定<br>
$ serverspec-init
対話形式で設定。設定後、以下の通りファイルが作成<br>
* [ツリー構造](serverspec/tree.png)<br><br>

* テストコードの作成<br>
* [specファイル](serverspec/lecture11_spec.rb)<br><br>

* テストコードの実行<br>
$ rspec spec/localhost/sample_spec.rb<br>
* [実行結果](serverspec/test_success.png)


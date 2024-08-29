# 第11回課題

## Serverspecを使用してテスト検証
* サンプルコードを使ってSeverspecのテストを実施
* [サンプルコード](https://github.com/MasatoshiMizumoto/raisetech_documents/tree/main/aws/samples/serverspec)
* [公式 doc](https://serverspec.org/)

## 流れ
* serverspecのインストール
$ gem install serverspec

* 作業ディレクトリへ移動

* 初期設定
$ serverspec-init
対話形式で設定。設定後、以下の通りファイルが作成
  ├─ spec
  │  ├─ localhost
  │  │  └─ sample_spec.rb
  │  └─ spec_helper.rb
  ├─ Rakefile
  └─ .rspec

* テストコードの作成
* [specファイル](serverspec/lecture11_spec.rb)

* テストコードの実行
$ rspec spec/localhost/sample_spec.rb
* [実行結果](serverspec/test_success.png)


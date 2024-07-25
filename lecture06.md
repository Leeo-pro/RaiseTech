# 第6回課題

## CloudTrail
### 含まれる内容3つ（イベント時間・イベント名・イベントソース）
- イベント時間 7月 19, 2024, 21:27:58 (UTC+09:00)
- イベント名 ConsoleLogin
- イベントソース signin.amazonaws.com
![エビデンス](images/lecture06/CloudTrail.png)
![エビデンス](images/lecture06/CloudTrails-eventrecord.png)

## アラート
- アプリ起動の状態
![エビデンス](images/lecture06/status_success.png)
- アプリ停止の状態
![エビデンス](images/lecture06/status_alert.png)
- アラートグラフ
![エビデンス](images/lecture06/alert_graph.png)
- アラート受信メール
![エビデンス](images/lecture06/alert_mail.png)

## 費用
- 現在の利用料
![エビデンス](images/lecture06/billing.png)
- 現在の利用料（内訳）
![エビデンス](images/lecture06/billing_detail.png)
- AWS Pricing Calculatorを使用した見積もり
https://calculator.aws/#/estimate?id=7c74b4ed78ae86fb5a84e4c29ac7025a36d3c8f1

## マネジメントコンソールから、現在の利用料を確認
- 無料枠内の使用を超えていたため料金が発生している。
- EC2はわずかながら超過していた。超過要因はインスタンスを合計4つ使用していたため
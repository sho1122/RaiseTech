# 第7回課題

## アプリについての脆弱性と対策
+ アプリケーションコード

   脆弱なコードだと、ハッキングに利用される、ウイルスに感染する可能性がある。
   
   対策
   + CodeGuru ReviewerやDependabot でコードをスキャンして修正する。
   + WAFを設置することが挙げられる。※1

+ EC2が1つ
  
  DoS・DDoS攻撃などの攻撃でたくさんアクセスされた時にサーバーが停止する可能性がある。

  対策
  + EC2を複数台設置する。
  + WAFを設置する。※1
  + AWS Shield で、DDoS 攻撃からインフラを保護してくれるマネージドサービスを使う。

+ SSL接続になってない

  利用者と Web サーバーの間で通信をのぞき見される可能性がある。

  対策
  + AWS Certificate Manager（ACM）でSSL 証明書を発行して通信を暗号化する。
  + ALB のリスナールールで HTTP アクセスを HTTPS に転送するルールを追加する。※2

+ OS、ミドルウェア
  
  マルウェアに感染したり、サイバー攻撃を受けて不正侵入されたりする可能性がある。

  対策
  + Amazon Inspector で脆弱性のスキャンを行う
  + 脆弱性に対しての重要度を設定しているCVSS(共通脆弱性評価システム)で修正が必要か判断する。

+ IAM の権限が最小限になってない

  対策
  + IAM Access Analyzerで不要な権限を与えてないか確認する。

## 感想
今回、AWSのセキュリティ対策について知ることができた。AWSにはセキュリティ対策のサービスがたくさんあることがわかった。セキュリティ対策は無限にあり、どこまで対策するのか判断するのが難しいと思った。事前にどのようなリスクがあるか意識することが大事であることもわかった。

## 参考リンク

  + [WAFとは？種類や仕組みを初心者にもわかりやすく徹底解説！｜ITトレンド](https://it-trend.jp/waf/article/162-0008#chapter-1):※1
  + [Application Load Balancer のリスナールール - Elastic Load Balancing](https://docs.aws.amazon.com/ja_jp/elasticloadbalancing/latest/application/listener-update-rules.html):※2



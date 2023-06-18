# 第５回課題

## EC2上にサンプルアプリケーションをデプロイして、動作させる

+ 組み込みサーバーだけ動作させる
![picture 3](images/a3f41691dcccd3e8f8f6ac113740d8166d82a63a4d4c796babb2ca1d6c4e545a.png)  

+ Webサーバーとアプリケーションサーバーを分けて動作させる
![picture 7](images/d42570d2919fb0dccbdccbdd66b4ac2b9dc25f5168ae62413787964dd702e730.png)  


## ELB(ALB)を追加
![picture 6](images/180b4bd14d3ec79d785fa37cc7121d089f4dceff748ed72c95ef8526e65c7dc6.png)  

## S3を追加
ALBのアクセスログをS3に保存するように設定。アクセスすると下の図のようにログが保存される。
![picture 5](images/e339e1f623b941d947c528516b6f4f027af804c08e0a0b4afe57531411204ad9.png)  


## 構成図に書き起こす
![picture 8](images/edf5b153241f0cc895642fed7595b57710a66e69a825659bec2670fe26e3e53e.png)  

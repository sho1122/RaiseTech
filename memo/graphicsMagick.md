
# GraphicsMagickのインストール方法

サイトにアクセスして、画像を追加する際に、画像が表示されない現象が起きた。原因はGraphicsMagickがインストールされてないから。

![picture 1](images/dc38f370a45505500d0b1462671539b568a3754d970b87c9bcae05c0bf2ac8c8.png)  

GraphicsMagickをインストール

```
sudo yum install GraphicsMagick GraphicsMagick-devel
```

再度サイトにアクセスして、画像を追加した際は、下の図のようにバナナの画像が表示されるようになった。

![picture 2](images/96c6de8029e0fc45d58ec2a523fa6273e32c9f5b6db79e9bec0bc7f8dd400182.png)  


## 参考リンク
  + [install graphicsmagick to EC2](https://gist.github.com/pzaich/3997914)

<script src="https://blz-soft.github.io/md_style/relea
se/v1.2/md_style.js" ></script>
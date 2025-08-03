# Ubuntu ServerでSFTPサーバをディレクトリ設定をする
##### このレポジトリーを使って構築設定する場合は、あくまで参考程度に使ってください。<br>OSやバージョンによっては、うまく設定できない場合がございます。

#### 各ユーザごとにSFTPサーバのディレクトリを設定する方法
##### ※ここではすでにユーザを作成設定が完了している状態から説明する。

> １，SFTPサーバ用ディレクトリの作成
```
sudo mkdir /home/user1
```
>２，ディレクトリ所有者の変更
```
sudo chown root:root /home/user1
```
> ３，ディレクトリアクセス権限の設定
```
sudo chmod 755 /home/user1
```
##### この時点でFileZillaを使ってサーバに接続してみると空のディレクトが表示される。<br>ここから実際にサーバに接続したときに表示されるファイルを作成する

> ４，FileZillaの画面に表示されるファイルディレクトリの作成
```
cd /home/user1
```
```
sudo mkdir uploads
```
```
sudo chown user1:user1 /home/user1/uploads
```

> ５，権限についての仕組み
- root権限所有ディレクトリ
<br>/home/user1

- ユーザ（user1）権限所有ディレクトリ
<br>~/uploads

# SpringBootをOpenshift上で動かすアプリケーション
## 起動方法
* 以下コマンドでOpenShift起動
 minishift start --vm-driver virtualbox
* IPの確認
    * minishift ip
* コンソールを開く（アカウント情報はログに出力されている）
    * minishift console
* アプリのビルドデプロイ

``` 
pringBoot Appをminikubeにデプロイする
ビルド 
 mvn package fabric8:build  
k8s用リソース生成 
 mvn fabric8:resource 
フォアグラウンド実行(コンソールが捕まる)
 mvn fabric8:run 

デプロイ （バックグラウンド実行となる）
 mvn fabric8:deploy
※標準入出力を使うのでタイムアウト等で失敗することがあるが、 再実行すればたいていうまくいく 
``` 
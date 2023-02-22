# 誘導

## ラズパイの基本設定

### モバイルホットスポット
- 名前: mobilehot
- パスワード: mobilehot
- バンド: 2.4GHz

### ラズパイログイン
- Username: pi
- Password: pi

### コンパイル方法
- ラズパイ起動後、これをする
- $ export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/lib/arm-linux-gnueabihf
- videoXの所を書き換える
-$ ++ -Wall videoX.cpp -o videoX.out -I /usr/local/include/opencv4 -L /usr/local/lib -lopencv_core -lopencv_objdetect -lopencv_highgui -lopencv_imgproc -lopencv_videoio -lopencv_imgcodecs -l wiringPi


### config.txtに追記したこと
- dtoverlay=disable-bt //primaty UARTをmini UARTからUART0に変更
- 参考url  https://www.ingenious.jp/articles/howto/raspberry-pi-howto/gpio-uart/#toc8)

## その他

### 注意点
- 現在は、videoX.cppがコンパイルされ、videoX.outが出来ている。
- sample.txtにログが書き込まれる
- imshow()関数をコメントアウトしないと、自動で実行することができない（ターミナルから、$./videoX.outで実行する分には問題ない）
- 実行するファイルを変更する場合は.serviceファイルも書き換える

### 改善？すべき点
- 使うラズベリーパイによって、primary UARTが異なる。そのため最終的に使うラズパイに設定を合わせて、設定を保存し、コードも直す
- 閾値の調整（変数名Threshold）
- inRange()関数での、色を取る範囲の調整
- データを記録するファイルの状況を確認する（何も書き込まれていない or 存在しない）

### 便利？なコマンド

#### 自動実行に関連する
- sudo nano /etc/systemd/system/sample.service  //.serviceファイルに書き込む
- sudo systemctl daemon-reload
- sudo systemctl restart sample.service 
- sudo systemctl status sample.service  
- sudo systemctl stop sample.service
- sudo systemctl enable sample.servic   //.serviceを有効化する

- vcgencmd get_camera   //カメラの接続確認


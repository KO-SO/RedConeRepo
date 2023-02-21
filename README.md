# ラズベリーパイ

## モバイルホットスポット
名前: mobilehot
パスワード: mobilehot
バンド: 2.4GHz

## ラズパイログイン
Username: pi
Password: pi

## config.txtに追記したこと
dtoverlay=disable-bt //primaty UARTをmini UARTからUART0に変更
参考url  https://www.ingenious.jp/articles/howto/raspberry-pi-howto/gpio-uart/#toc8

## 改善？すべき点
使うラズベリーパイによって、primary UARTが異なる。そのため最終的に使うラズパイに設定を合わせて、設定を保存する
閾値の調整（変数名Threshold）
inRange()関数での、色を取る範囲の調整
imshow()等のコメントアウト
データを記録するファイルの状況を確認する（何も書き込まれていない or 存在しない）

## すること
/etc/systemd/system/ディレクトリに、RedVideo.serviceという名前の新しいサービスファイルを作成する
サービスを有効化する
$ sudo systemctl enable sample.service
プログラムの動作状況の環境
$ sudo systemctl status sample.service
サービスが起動していたら"active (running)"と表示される


# play_raspi_pico
raspi picoで触ってみたファイルです。

参考　https://garchiving.com/use-raspberry-pi-pico-with-arduino-ide/

ボードマネージャーは参考サイトの通りに
# 書き込み
BOOTSELを押しながら、USBを差し込み、ArduinoIDEで書き込みます。
# サンプルプログラム
rp2040の中にあるものは基本的に動きます。
- Lチカ
- 温度測定
- 時間計測
- BOOTSELボタンの確認
- マルチコアプログラミング
などが試せます。
# ピン配置
https://akizukidenshi.com/download/ds/raspberry/pico-datasheet.pdf
秋月のデータシートより
- 3V3
- UART
# 不具合
仮想ドライブは開くけど、COMポートが認識しなくなっていました。
デバイスマネージャーのCOMポートを確認すると、RP2 Bootに注意マークが。

https://bokunimo.net/blog/raspberry-pi/1460/
こちらのサイトを参考に、.uf2ファイルをダウンロードし、
RaspiPocoのドライブに投げると、色々書き代わり認識するようになりました。

その後ArduinoIDEでプログラムをアップロードすると勝手にファームを書き換えて、アップロードできました。

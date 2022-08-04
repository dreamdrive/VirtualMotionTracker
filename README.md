# VMT - Virtual Motion Tracker の "だみとら"向け改造版

本家VMTから派生した MocapForAll向け改造版VMTに、更に"だみとら"に必要だった機能(SetRoomMatrixの外部実行)を追加しました。
"だみとら"アプリ内から、必要なVMTのセットアップをすべて制御できるように作成しました。

- だみとら : https://booth.pm/ja/items/2897804
- だみとら2 : https://ddrive.booth.pm/items/3821909

## MocapForAll向け改造版からの変更点

- SetRoomMatrixを実行する起動時の引数の追加 : setroom
``` 
vmt_manager.exe setroom	
```
実行すると即座にSetRoomMatrixが実行され、ダイアログを表示したあと、終了します。

## VMT の MocapForAll向け改造版の機能

ドライバに対する操作に、下記が追加されています。

- **/VMT/GetDevicePose serial**  
  指定したシリアル番号のデバイスの姿勢の返送を要求します。
  「serial」は、string型でデバイスシリアル(LHR-xxxxxxx等)を指定します。ヘッドマウントディスプレイに対しては、デバイスシリアルの代わりに「HMD」と指定することができます。

ドライバからの応答に、下記が追加されています。

- **/VMT/Out/DevicePose serial x, y, z, qx, qy, qz, qw**  
  シリアル番号で特定されるデバイスの姿勢を通知します。  

## リンク
- [Virtual Motion Tracker - MocapForAll向け改造版](https://github.com/KenjiAsaba/VirtualMotionTracker)
- [Virtual Motion Tracker - オリジナル版](https://gpsnmeajp.github.io/VirtualMotionTrackerDocument/)

# Licence
MIT Licence

Logo text font: M+ Fonts https://mplus-fonts.osdn.jp/about2.html

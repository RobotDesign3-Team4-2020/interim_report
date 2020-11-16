# 4班中間発表
##  ロボットアームと消毒スプレーによるうんこの消毒
### 動機
 <img src= "https://github.com/RobotDesign3-Team4-2020/interim_report/blob/master/img/picture1.png" width="400" >
 あ！うんこがいるよ！消毒しなきゃ！
 <img src= "https://github.com/RobotDesign3-Team4-2020/interim_report/blob/master/img/picture2.png" width="400" >
 君こっち来いよ！
 <img src= "https://github.com/RobotDesign3-Team4-2020/interim_report/blob/master/img/picture3.png" width="400" >
 これで清潔なうんこになるんだ…
 <img src= "https://github.com/RobotDesign3-Team4-2020/interim_report/blob/master/img/picture4.png" width="400" >
 <img src= "https://github.com/RobotDesign3-Team4-2020/interim_report/blob/master/img/picture5.png" width="400" >
 わーい！綺麗になったよ！
 こうしてcrane-x7くんは清潔なうんこくんと仲良く暮らしましたとさ
### 何が面白い？
* うんこが消毒される
### 使用する道具
* crane_x7  
* ubuntu18.04(WSL/Desktop)
  * Gazebo
  * rviz
* inventor
* うんこのおもちゃ  
* 噴射型のアルコール
###  実行環境
- ubuntu18.04
- ROS 
### 操作説明

### プログラム説明

Move it を使って姿勢を指定して アルコールスプレーに当たらないようにした

### 実演

### 動画
https://youtu.be/FMTXlpocT58 

### 開発スケジュール予定
| 内容 | アームの座標計測 | 3Dデータ作成  | アームの移動コード | 中間発表資料 |
| :--: | :-------------: | :-----------: | :-------------: | :-------------: |
| 担当 | [Mitsuike](https://github.com/SomaMitsuike) | [Ikeda](https://github.com/ikeda-hitomi) | [Nakajima](https://github.com/Isamu-Nakajima) | [Mibuchi](http://github.com/mibuchiyuta) |
| 　　 | [Kamioka](https://github.com/rlove1023) | [Mibuchi](http://github.com/mibuchiyuta) | [Sakamoto](https://github.com/Sakamoto-Takaya) |
| 期日 | 10/26 | 10/26 | 11/15 | 11/15 |
### 実際の進捗
- アームの座標計測 : 予定通り完了
  - ソースコードに合わせて物体を配置したので計測することほぼなしでした.
- 3Dデータ作成 : 一週間遅れて完了
  - Inventorで作成したデータを扱えないか試行錯誤 → できない
  - gazebo上でのモデルは必須項目ではないので時間をかけるのは違うのではないか
  - 目標は実機で動作させることなので,簡易的なモデルを使用することにピボット → 実機を動かすことに集中できた
- 
###  まとめ
基本的な動作はおおむね問題はなかったが、まれに目標座標にぶれが出ることがあったためさらなる調整が必要だ。

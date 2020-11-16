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
- うんこが消毒される
- 
### 使用した道具
- crane_x7  
- ubuntu18.04(WSL/Desktop)
  - Gazebo
  - rviz
- Inventor
- うんこのおもちゃ  
- 噴射型のアルコール
###  実行環境
- ubuntu18.04
- ROS 
### 実機操作説明
#### モデル配置
- 用意するもの
  - うんこのおもちゃ
  - 市販の据え置き型アルコールスプレー  
<img src= "https://github.com/RobotDesign3-Team4-2020/interim_report/blob/master/img/img4.jpg" width="400">

- 配置方法
<img src= "https://github.com/RobotDesign3-Team4-2020/interim_report/blob/master/img/img5.png" width="400">  
<img src= "https://github.com/RobotDesign3-Team4-2020/interim_report/blob/master/img/img2.jpg" width="400">  

#### 実機の動かし方
動作確認する場合、信号ケーブルを接続した状態で次のコマンドを実行してください。
```
$ sudo chmod 666 /dev/ttyUSB0
$ roslaunch crane_x7_bringup demo.launch fake_execution:=false  
```  

### プログラム説明

Move it を使って姿勢を指定して アルコールスプレーに当たらないようにした

### 実演動画
[![うんこを消毒](https://i9.ytimg.com/vi/FMTXlpocT58/mq2.jpg?sqp=CJisx_0F&rs=AOn4CLCmc1RQ60qa4UNeHhZr6m1B__A6jQ)](https://www.youtube.com/watch?v=FMTXlpocT58&feature=youtu.be "うんこを消毒")  

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
- アームの移動コード : 予定通り完了
  - 実機を動かすまでにおおむねのソースコード作成完了
  - 実機を動かして調整/機能の追加の時間を多く取れた
### まとめ
基本的な動作はおおむね問題はなかったが、まれに目標座標にぶれが出ることがあったためさらなる調整が必要だ。


[English](README.en.md) | [日本語](README.md)
# うんこ消毒ロボット

## CRANE-X7のROSパッケージをインストール
```
$ cd ~/catkin_ws/src/
$ git clone https://github.com/RobotDesign3-Team4-2020/crane_x7_ros.git
$ rosdep install -r -y --from-paths --ignore-src crane_x7_ros
```
## branchの移動
```
cd ~/catkin_ws/src/crane_x7_ros
git checkout unko_shodoku_try
```
## 実機を使う場合
### モデル配置
- 用意するもの
  - うんこのおもちゃ
  - 市販の据え置き型アルコールスプレー  
<img src= "https://github.com/RobotDesign3-Team4-2020/interim_report/blob/master/img/img4.jpg" width="400">

- 配置方法
<img src= "https://github.com/RobotDesign3-Team4-2020/interim_report/blob/master/img/img5.png" width="400">  
<img src= "https://github.com/RobotDesign3-Team4-2020/interim_report/blob/master/img/img2.jpg" width="400">  
<img src= "https://github.com/RobotDesign3-Team4-2020/interim_report/blob/master/img/img1.jpg" width="400">  

### 実機の動かし方
動作確認する場合、信号ケーブルを接続した状態で次のコマンドを実行してください。
```
$ sudo chmod 666 /dev/ttyUSB0
$ roslaunch crane_x7_bringup demo.launch fake_execution:=false  
```  
## gazeboを使用する場合 
   
   - gazeboの起動方法  
   ~~~
   $ roslaunch crane_x7_gazebo crane_x7_with_table.launch
   ~~~
## プログラム
 - うんこを消毒する手順   
1.うんこをつかむ  
2.うんこを消毒スプレーのそばに置く  
3.消毒スプレーを押す

  - 実行方法  
  下記のコマンドを実行してください  
  ~~~
rosrun crane_x7_examples try_third.py
  ~~~
  - ソースコードは[こちら](https://github.com/RobotDesign3-Team4-2020/crane_x7_ros/blob/master/crane_x7_examples/scripts/try_third.py)をご覧ください

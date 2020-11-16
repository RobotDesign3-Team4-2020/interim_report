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
- うんこは消毒されるものなのか
- というか他のもの消毒したら実用的

### 使用した道具  
- crane_x7    
- ubuntu18.04(WSL/Desktop)  
  - Gazebo  
  - rviz  
- Inventor  
- うんこのおもちゃ   
- 据え置き型アルコールスプレー

###  実行環境
- ubuntu18.04
- ROS Melodic Morenia

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
READMEに従ってください
[README](https://github.com/RobotDesign3-Team4-2020/crane_x7_ros/blob/unko_shodoku_try/crane_x7_examples/README.md)


### プログラム説明

- [コメント付きソースコード](https://github.com/RobotDesign3-Team4-2020/crane_x7_ros/blob/R.kamioka/crane_x7_examples/scripts/try_third.py)

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
- 中間発表資料 : 1日遅れて完了
  - 分担して作業したので情報を集めることに苦戦
  - 分担しても情報の共有はもう少しこまめにやっておくべきだった
  
### 最終的に担当したもの
- Ikeda
  - Inventorで作成したデータをGazeboに取り入れる
  - urdfファイルの編集
  - READMEの作成
- Kamioka
  - プッシュ動作の実装
  - 姿勢制御/プッシュの調整
- Sakamoto
  - 姿勢制御のソースコード作成
  - 去年のリポジトリからうんこデータを持ってくる
- Nakazima
  - 配布されたソースコード読み取り
  - 中間発表資料作成
- Mitsuike
  - READMEの作成
- Mibuchi
  - 買い物/検収
  - 実機動作確認
  - 発表資料作成
  - README作成
  - Githubの勉強会(のようなもの)
### まとめ
- そもそものスタンスは最低限の作業で面白いものを作ろう → 成功
- 1週間単位での余裕を持ったがギリギリであった
- Github/slack/backlogなどのサービスの使い方を教え合うことにリソースを割かれた
- 作業量に偏りができてしまった,
  - タスク管理も大きな作業となった

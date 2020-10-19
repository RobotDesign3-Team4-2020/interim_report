# 中間発表の目標

## ロボットアームと消毒スプレーによるうんこの消毒
### 動機
 <img src= "https://github.com/RobotDesign3-Team4-2020/interim_report/blob/master/picture1.png" width="400" >
 あ！うんこがいるよ！消毒しなきゃ！
 <img src= "https://github.com/RobotDesign3-Team4-2020/interim_report/blob/master/picture2.png" width="400" >
 君こっち来いよ！
 <img src= "https://github.com/RobotDesign3-Team4-2020/interim_report/blob/master/picture3.png" width="400" >
 これで清潔なうんこになるんだ…
 <img src= "https://github.com/RobotDesign3-Team4-2020/interim_report/blob/master/picture4.png" width="400" >
 <img src= "https://github.com/RobotDesign3-Team4-2020/interim_report/blob/master/picture5.png" width="400" >
 わーい！綺麗になったよ！
 こうしてcrane-x7くんは清潔なうんこくんと仲良く暮らしましたとさ
 
### 何が面白いか
- うんこが消毒される

### 使用する道具
- crane_x7
- ubuntu18.04(WSL/Desktop)
 - Gazebo
 - Inventor
 - rviz
- うんこ(のおもちゃ)
- 噴射型のアルコール(のようなもの)

### システム構成
1． 指定の座標にあるうんこを掴む  
2． スプレーの噴射口の下にうんこを移動する  
3． うんこを置く  
4． スプレーの上部にアームを移動させる  
5． 垂直に任意の高さまでアームを下げ,アルコールを噴射させる  

### やらなきゃいけないこと
1. アームを移動させたときの各座標データをとる 
2. アームの開閉(サンプルコードを参照すれば良い？)  
3. アームの移動  
4. 仮想空間での追加の3Dデータについて?

### 想定される問題について
1. アームを移動させたときの各座標データをとる 
 →実機と仮想空間で座標に差が生じる
2. アームの開閉(サンプルコードを参照すれば良い？)  
 →アルコールを押すときにハンドの開閉をしないとうまく行かない可能性がある  
3.アームの移動  
 →実機と仮想空間で座標に差が生じる
4.垂直に任意の高さまでアームを下げ,アルコールを噴射させる
 →アルコールが傾いてうまく噴出できない可能性

### スケジュール/担当
| 内容 | アームの座標計測 | 3Dデータ作成  | アームの移動コード | 中間発表資料 |
| :--: | :-------------: | :-----------: | :-------------: | :-------------: |
| 担当 | [Mitsuike](https://github.com/SomaMitsuike) | [Ikeda](https://github.com/ikeda-hitomi) | [Nakajima](https://github.com/Isamu-Nakajima) | [Mibuchi](http://github.com/mibuchiyuta) |
| 　　 | [Kamioka](https://github.com/rlove1023) | [Mibuchi](http://github.com/mibuchiyuta) | [Sakamoto](https://github.com/Sakamoto-Takaya) |
| 期日 | 10/26 | 10/26 | 11/15 | 11/15 |

なお担当の作業が終わり次第,次に近い期日の作業を手伝うこととする

### チームアップから第一週目のやったこと
- [Move itで容器をプッシュさする動作をさせてみた(GAZEBO)](https://www.youtube.com/watch?v=xksuRjdeR2U&feature=youtu.be)
- gazeboにインベンターからのデータを反映させられないかやってみた→STLデータを出力してそれを反映させるのは難しそう？
- githubでプルリクとマージを全員やってみる

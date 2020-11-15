# うんこ消毒ロボット

## CRANE-X7のROSパッケージをインストール

## 実機を使う場合

## gazeboを使用する場合 
   - gazeboモデルのインストール  
  ~~~
$ git clone https://github.com/RobotDesign3-Team4-2020/crane_x7_ros.git
  ~~~
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
  - プログラムコードは[こちら](https://github.com/RobotDesign3-Team4-2020/crane_x7_ros/blob/master/crane_x7_examples/scripts/try_third.py)をご覧ください

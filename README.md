# models
![gazebo_card_stand_model](https://user-images.githubusercontent.com/72371743/97830667-1510bc80-1d11-11eb-809c-ae885aaa81df.png)



## モデル置き場所  
~/.gazebo/models 

crane_x7_ros_team3_2020/crane_x7_gazebo/下のworlds,launchディレクトリが必要です。

## 実行する時  
roslaunch crane_x7_gazebo crane_x7_card_stand.launch


![ダウンロード](https://user-images.githubusercontent.com/72371743/98934361-4d8c7380-2525-11eb-9d9b-b7446e183553.gif)

## モデルの作成方法（wslの場合）  
### 注意  
あくまで自己流の方法なのでもっといい方法があるかもしれません  
  
事前にubuntuでモデルを置くディレクトリを作成しておきます  
例：penのモデル  
### windows側の操作
1,Inventorなど好きなCADソフトを使い、stlファイルを作成する  
pen.stl  
  
2,作成したstlファイルをblenderでインポートし、COLLADA形式(.dae)でエクスポートする（モデルのサイズに注意!!blender上でNキーで大きさが見えます）  
pen.stl → pen.dae  
  
3,windowsの左下のタスクバー検索で\\\wsl$と入力し、ubuntu-18.04の中の自分がmodelを置きたい場所にwindowsから（コピーして）移す  
ubuntu-18.04/home/username/.gazebo/models/pen  

### ubuntu側の操作
4,モデルを置くために作成したディレクトリの中でmodel.sdf,model.configファイルを作成する  
~/.gazebo/models/penの下にmodel.sdf,model.config  
  
5,model.sdfとmodel.configの中身はgazeboのデフォルトモデル（~/.gazebo/modelsのwood_cube_5cmなど）のファイルを参考にして作成する  
  
6,worldファイルを書き換える  
  
7,launchファイルを書き換える → 完成：roslaunchで実行すればgazebo上にモデルがある状態　　


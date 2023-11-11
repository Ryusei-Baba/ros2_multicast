# ros2_multicast

Jetsonの処理が重いとき，ROS 2のmulticast機能を利用することで，別のPCでRViz2の可視化や画面録画，rosbag2の記録をし，Jetson側の処理を軽くすることができる．

---
### 使い方
1. 受信するPC（humble）のipアドレスを192.168.0.xxxに設定
2. 受信する側（PC）
```
ros2 multicast receive
```
3. Jetson側
```
ros2 multicast send
```
4. 受信する側（PC）
```
cd ~/ws/src/orne-box//orne_box_navigation_executor/config/rviz/
rviz2 -d nav2_default_view.rviz
```
5. 

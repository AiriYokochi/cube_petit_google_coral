# cube_petit_google_coral

卓上ロボットCube petitにGoogleCoralを接続して、インタラクションを行うROS2 Package郡です。

## Setup
- Ubunt24.04 PC
- Google Coral
- ROS2 Jazzy
- cube_petit_ros (`jazzy-devel`)

## Quick install and Test
- pip install
  - vcs
  - uv

```
cd ~/ros/src/
git clone
rosdep update
rosdep install --from-paths . -iry
colcon build --symlink-install cube_petit_google_coral
```

## Input/Oputput
### Inout topic
- `image_raw` : Sensor/Image : Camera image

### Output topic
- `<robot_name>/coral_recog/face_expression`:(`std_msgs/String`)
- `<robot_name>/coral_recog/face_direction`:
- `<robot_name>/coral_recog/hand_direction`:
- `<robot_name>/coral_recog/pose_estimation`::(`std_msgs/String`)

## Packages
### coral_face_exression_recognition
表情認識のPackagesです。表情を出力します。
`std_msgs/String`
```
happy, annry, sad, 
```
### coral_face_direction_recognition
人の顔の向きを取得するPackageです
### coral_hand_direction_recognition
指を指した方向をす取得するPackageです
### coral_pose_estimation_recognition
ポーズ認識のPackagesです。人のポーズを出力します


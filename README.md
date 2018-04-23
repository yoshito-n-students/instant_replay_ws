# instant_replay_ws
A ROS workspace for instant replay system containing of an IP camera

## Setup
```
git clone git@github.com:yoshito-n-students/instant_replay_ws.git
cd instant_replay_ws
git checkout devel
git submodule update --init --recursive
catkin_make
```

## Run
```
cd instant_replay_ws
source devel/setup.bash
roslaunch instant_replay_application everything.launch server:=<camera's ip address> path:=<path to motion-jpeg video> delay:=<delay in seconds>
```
Parameters for `everything.launch` can be ommited if you want to use the default values (`server`: 192.168.0.90, `path`: /axis-cgi/mjpg/video.cgi, and `delay`: 1.0).

### Trouble shooting
* check if the PC and camera are connected by running `ping <server>` in a terminal
* check if the camera is streaming a motion-jpeg video by accessing an URL like `http://<server><path>` using a browser. The URL is specific to the camera model.

## Update
```
cd instant_replay_ws
git pull
git submodule update --init --recursive
catkin_make
```

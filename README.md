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
roslaunch instant_replay_application everything.launch server:=<camera's ip address> delay:=<delay in seconds>
```

## Update
```
cd instant_replay_ws
git pull
git submodule update --init --recursive
catkin_make
```

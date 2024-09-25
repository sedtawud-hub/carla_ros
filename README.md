# ROS/ROS2 bridge for CARLA simulator

This is a fork of [gezp/carla_ros](https://github.com/gezp/carla_ros/tree/carla-python-api). to adapt ros humble, carla 0.9.15 and numpy 2.x.x

### Quickly Start

Environment

* OS: ubuntu 22.04
* ROS2: Humble
* Carla Simulator: 0.9.14
* Numpy: 2.1.1

Install client library

* download python package of client library for ubuntu22.04 in [release(carla-0.9.15-ubuntu-22.04)](https://github.com/gezp/carla_ros/releases/)

```
pip3 install carla-0.9.14-cp310-cp310-linux_x86_64.whl
```

Build `carla-simulator/ros-bridge`
```bash
# cd workspace/src
git clone --recurse-submodules https://github.com/sedtawud-hub/carla_ros.git
# install dependencies
cd ..
rosdep install --from-paths src --ignore-src -r
pip3 install pygame
# complie
colcon build --symlink-install
```

> Tip: carla server and client could run on differnet machines separately (or Docker Container), so you can install and run carla server on ubuntu18.04 or windows10/11, but run carla client and ROS on ubuntu22.04.

### Carla Client Library Build CI

this repo also provides multiple versions of Carla Client Library on ubuntu platform, these python package(.whl) is automatically built and released by CI.

* python package of client library: [releases](https://github.com/gezp/carla_ros/releases/)

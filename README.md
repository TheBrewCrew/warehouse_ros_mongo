Code for persisting ROS message data using MongoDB.  Contains C++ and Python libraries to serialize ROS data to MongoDB, as well as some handy scripts to record data from the command line.  See http://www.ros.org/wiki/warehousewg for more.

master branch: [![Build Status](https://travis-ci.org/ros-planning/warehouse_ros.png?branch=master)](https://travis-ci.org/ros-planning/warehouse_ros)

# Building from source

## ROS Kinetic / Ubuntu 16.04

In order to build from source you'll need to install the [mongo c++ drivers](https://github.com/mongodb/mongo-cxx-driver/wiki/Download-and-Compile-the-Legacy-Driver)

First get the driver:
```
git clone -b 26compat https://github.com/mongodb/mongo-cxx-driver.git
```

Then compile using scons:
```
sudo apt-get install scons
scons --prefix=/usr/local/ --full --use-system-boost --disable-warnings-as-errors
sudo scons install
```

You should now be able to compile the packages using catkin.

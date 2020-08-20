## Installation Instructions

### Install the latest Intel® RealSense™ SDK 2.0

* Add Intel server to the list of repositories :

echo 'deb http://realsense-hw-public.s3.amazonaws.com/Debian/apt-repo xenial main' | sudo tee /etc/apt/sources.list.d/realsense-public.list

It is recommended to backup /etc/apt/sources.list.d/realsense-public.list file in case of an upgrade.
* Register the server’s public key :

sudo apt-key adv --keyserver keys.gnupg.net --recv-key 6F3EFCDE
* Refresh the list of repositories and packages available :

sudo apt-get update

* In order to run demos install:

sudo apt-get install librealsense2-dkms

sudo apt-get install librealsense2-utils

The above two lines will deploy librealsense2 udev rules, kernel drivers, runtime library and executable demos and tools. Reconnect the Intel RealSense depth camera and run: realsense-viewer

### Install Intel® RealSense™ ROS from Sources
git clone https://github.com/IntelRealSense/realsense-ros
catkin_make

如果报错基本是SDK的版本和ROS包的版本不对应，需要从源码编译安装。

源码于：https://github.com/IntelRealSense/librealsense/releases下载，使用cmake编译安装。

* 示例程序：

roslaunch realsense2_camera demo_pointcloud.launch 

* 效果:


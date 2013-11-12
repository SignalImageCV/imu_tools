IMU tools for ROS
===================================

Overview
-----------------------------------

IMU-related filters and visualizers. The stack contains:

 * `imu_filter_madgwick`: a filter which fuses angular velocities,
accelerations, and (optionally) magnetic readings from a generic IMU 
device into an orientation. Based on the work of [1].

 * `rviz_imu_plugin` a plugin for rviz which displays `sensor_msgs::Imu`
messages

Installing
-----------------------------------

### From source ###

[Create a catkin workspace](http://wiki.ros.org/catkin/Tutorials/create_a_workspace)
(e.g., `~/ros-hydro-ws/`) and source the `devel/setup.bash` file.

Make sure you have git installed:

    sudo apt-get install git-core

Download the stack from our repository into your catkin workspace (e.g.,
`ros-hydro-ws/src`; use the proper branch for your distro, e.g., `groovy`,
`hydro`...):

    git clone -b <distro> https://github.com/ccny-ros-pkg/imu_tools.git

Install any dependencies using [rosdep](http://www.ros.org/wiki/rosdep).

    rosdep install imu_tools

Compile the stack:

    cd ~/ros-hydro-ws
    catkin_make

More info
-----------------------------------

http://wiki.ros.org/imu_tools

License
-----------------------------------

 * `imu_filter_madgwick`: currently licensed as GPL, following the original implementation

 * `rviz_imu_plugin`: BSD

References
-----------------------------------
 [1] http://www.x-io.co.uk/node/8#open_source_ahrs_and_imu_algorithms

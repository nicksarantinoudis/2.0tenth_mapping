# 2.0tenth_mapping
A mapping package for the 2.0 Tenth platform using the new Gazebo sim. 

## ROS2 Build
1. Create your workspace folder
2. Create a src folder
3. Run `colcon build` on the empty folder to initialize
5. Clone the repository into the src folder
6. Run `rosdep update`
7. Run `rodep install --from-paths src -i -y`
8. Run `colcon build`

The build should be succesfully completed

## Tips 

Don't forget to `source /opt/ros/humble/setup.bash` if not 
in your `.bashrc` file.
Also `source install/setup.bash` on your workspace after the 
succesful build 

## Launch Files
There are 3 useful `.launch` files which can be used for testing

1. `ros2 launch slam_toolbox f1_tenth_offline_mapping.launch.py` -> Launches the mapping
node which expects either real or simulated data to the subscribed topics
2.  `ros2 launch slam_toolbox f1_tenth_slam_rviz.launch.py` -> Launches RViz with the 
Slam Toolbox plugin. The map is created in real time and can be saved through the plugin.
3. `ros2 launch map2gazebo map2gazebo.launch.py` -> Converts the recorded file into a 3D
file that can be then used into Gazebo.


First, build the workspace:

colcon build

To launch the model in rviz:

ros2 launch mecanum_model display.launch.py gui:=true

To launch the model in gazebo:

ros2 launch mecanum_model display-gazebo.launch.py

Convert xacro to urdf:

xacro ./s1-based-rover.urdf.xacro > s1-based-rover.urdf

Convert urdf to Gazebo sdf:

gz sdf --verbose -p ./s1-based-rover.urdf

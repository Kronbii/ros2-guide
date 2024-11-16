# ros2-guide
This is a complete guide for the ROS2 user experience

### Sourcing the underlay
```
source /opt/ros/<"your distro">/setup.bash
```

### Sourcing the overlay
```
cd ~/ros2_ws
source install/setup.bash
```

### Downloading all dependencies
```
rosdep install -i --from-path src --rosdistro jazzy -y
```

### Creating a workspace
```
mkdir -p ~/ros2_ws/src
```

### Building a project
> Builds all the workspace
```
cd ~/ros2_ws
colcon build
```
> Builds specific package only
```
colcon build --packages-select <"package-name">
```
> Build creates the following directory structure
```
.
├── build
├── install
├── log
└── src

```

### Running turtlesim package
```
ros2 run turtlesim turtlesim_node
ros2 run turtlesim turtle_teleop_key
```

### 
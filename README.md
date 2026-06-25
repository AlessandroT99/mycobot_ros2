# myCobot ROS 2

![Ubuntu](https://img.shields.io/ubuntu/v/ubuntu-wallpapers/noble)
![ROS 2](https://img.shields.io/ros/v/jazzy/rclcpp)

A comprehensive ROS 2 package suite for the myCobot series collaborative robots by Elephant Robotics.

## Overview

This repository provides complete ROS 2 integration for myCobot collaborative manipulators. It includes robot descriptions with URDF/Xacro models, 3D meshes, visualization configurations, and launch files for easy setup and control.

## Supported Models

- **myCobot 280** - 6-DOF collaborative robotic arm
- **Adaptive Gripper** - End-effector attachment
- **G-Shaped Base v2.0** - Mobile base platform
- **D435 Camera** - Intel RealSense sensor integration

## Prerequisites

- **Ubuntu 24.04 (Noble)** or compatible
- **ROS 2 Jazzy** or later
- **Xacro** for URDF processing

## Installation

Clone this repository into your ROS 2 workspace:

```bash
cd ~/ros2_ws/src
git clone https://github.com/yourusername/mycobot_ros2.git
cd ~/ros2_ws
rosdep install --from-paths src --ignore-src -r -y
```

## Building

```bash
cd ~/ros2_ws
colcon build --packages-select mycobot_ros2 mycobot_description
```

## Packages

### mycobot_ros2 (Metapackage)

Aggregates all myCobot ROS 2 packages.

### mycobot_description

Contains all robot description files:
- **URDF/Xacro Models** - Robot kinematics and structure
- **3D Meshes** - Visual representations
- **RViz Configs** - Visualization setups
- **Launch Files** - Automated robot loading

See [mycobot_description/README.md](mycobot_description/README.md) for:
- Detailed file organization
- URDF customization guide
- Launch file parameters
- Adding new sensors
- RViz configuration

## Usage Examples

### Load Robot in Your Launch File

See [mycobot_description/README.md](mycobot_description/README.md#ros-2-integration) for code examples on integrating the robot description into your launch files.

### Validate and Debug URDF

Refer to [mycobot_description/README.md](mycobot_description/README.md#contributing) for URDF validation tools.

## Directory Structure

```
mycobot_ros2/
├── mycobot_ros2/            # Metapackage
└── mycobot_description/     # Robot descriptions, meshes, configs, launch files
    ├── urdf/                # URDF/Xacro models
    ├── meshes/              # 3D mesh files
    ├── rviz/                # RViz configurations
    ├── launch/              # Launch files
    └── README.md            # Detailed documentation
```

## Contributing

When contributing:

1. Follow ROS 2 coding standards
2. Test changes with RViz visualization
3. Update relevant documentation
4. Reference the [mycobot_description README](mycobot_description/README.md#contributing) for URDF validation

## License

BSD-3-Clause License - See LICENSE file for details

## Maintainers

- **ale** <ale@todo.todo>

## References

- [ROS 2 Documentation](https://docs.ros.org/en/jazzy/)
- [URDF Tutorial](https://wiki.ros.org/urdf/Tutorials)
- [Xacro Documentation](https://wiki.ros.org/xacro)
- [Elephant Robotics](https://www.elephantrobotics.com/)

## Support

For issues, questions, or contributions, please open an issue or pull request on the repository.
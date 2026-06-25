# myCobot Description Package

This package contains the robot description files for myCobot robots, including URDF/Xacro definitions, 3D meshes, and visualization configurations.

## Overview

The `mycobot_description` package provides:

- **URDF/Xacro Models** - Complete robot kinematic and dynamic descriptions
- **3D Meshes** - Visual representations of robot components
- **RViz Configurations** - Pre-configured visualization setups
- **Launch Files** - Automated robot visualization and state publishing

## Package Contents

### URDF/Xacro Files (`urdf/`)

Located in `urdf/` directory:

#### Robots (`urdf/robots/`)
- **`mycobot_280.urdf.xacro`** - Complete myCobot 280 robot assembly
  - Includes arm, base, gripper, and optional sensors
  - Main entry point for the robot model

#### Mechanical Components (`urdf/mech/`)
- **`mycobot_280_arm.urdf.xacro`** - 6-DOF robotic arm kinematics
  - Joint definitions and limits
  - Link geometry and dynamics
  
- **`adaptive_gripper.urdf.xacro`** - Adaptive gripper attachment
  - End-effector definition
  - Gripper control interface
  
- **`g_shape_base_v2_0.urdf.xacro`** - Mobile base platform
  - Base link and platform geometry
  - Optional wheels or support structure

#### Sensors (`urdf/sensors/`)
- D435 camera definitions
- Other sensor mount points and configurations

#### Control (`urdf/control/`)
- Control-related joint and link definitions
- Transmission definitions (if applicable)

### 3D Meshes (`meshes/`)

Visual mesh files organized by component:

```
meshes/
├── mycobot_280/         # Arm links and joints
├── adaptive_gripper/    # Gripper components
├── g_shape_base_v2_0/   # Base platform
└── d435/                # Camera housing
```

All meshes use visual representations in the `visual/` subdirectories.

## File Structure

```
mycobot_description/
├── urdf/
│   ├── robots/
│   │   └── mycobot_280.urdf.xacro
│   ├── mech/
│   │   ├── mycobot_280_arm.urdf.xacro
│   │   ├── adaptive_gripper.urdf.xacro
│   │   └── g_shape_base_v2_0.urdf.xacro
│   ├── sensors/
│   │   └── (sensor definitions)
│   └── control/
│       └── (control definitions)
├── meshes/
│   ├── mycobot_280/visual/
│   ├── adaptive_gripper/visual/
│   ├── g_shape_base_v2_0/visual/
│   └── d435/visual/
├── rviz/
│   └── mycobot_280_description.rviz
├── launch/
│   └── display.launch.py
├── package.xml
└── CMakeLists.txt
```

## Dependencies

This package depends on:
- `urdf_tutorial` - For URDF utilities
- ROS 2 standard packages (robot_state_publisher, rviz2, joint_state_publisher_gui)

## Xacro Usage

All URDF files use Xacro macros for parameterization and modularity.

## References

- [ROS 2 URDF Tutorial](https://wiki.ros.org/urdf/Tutorials)
- [Xacro Documentation](https://wiki.ros.org/xacro)
- [Robot State Publisher](https://github.com/ros/robot_state_publisher)
- [RViz User Guide](https://wiki.ros.org/rviz)

## License

BSD-3-Clause - See LICENSE file for details

## Support

For issues or questions about the robot description, please refer to the main repository.
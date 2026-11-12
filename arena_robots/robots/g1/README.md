# Unitree G1 Robot

This directory contains the Arena robot definition for the Unitree G1 humanoid robot.

## Overview

The Unitree G1 is a 29-degree-of-freedom humanoid robot with:
- 12 leg joints (6 per leg)
- 3 waist joints (yaw, roll, pitch)
- 14 arm joints (7 per arm, including 3-finger hands)

## Files

- `urdf/g1.urdf.xacro` - Main URDF description
- `urdf/base_hw/g1.ros2_control.urdf` - ros2_control hardware interface
- `model_params.yaml` - Robot-wide parameters (base frame, sensors, etc.)
- `control.yaml` - ros2_control controller configuration
- `mappings.yaml` - Simulator ↔ ROS2 topic bridges
- `caps/mobile.yaml` - Mobile base capabilities
- `assembly.yaml` - Component catalog sensor mounts
- `champ/` - CHAMP quadruped locomotion controller config
- `launch/bringup.launch.py` - Robot bringup launch file

## Usage

```bash
# Launch in Gazebo
arena launch ... robot:=g1 sim:=gazebo

# Launch in MuJoCo
arena launch ... robot:=g1 sim:=mujoco
```

## References

- [Unitree G1](https://www.unitree.com/g1/)
- [unitree_ros repository](https://github.com/unitreerobotics/unitree_ros)

## License

This robot definition is provided for educational and research purposes.
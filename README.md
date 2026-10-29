# Dynamic Control of a 3R Robot

Joint-space control of a planar 3R robot in MATLAB/Simulink with **Simscape Multibody**: PD control and computed torque control.

> Third assignment of the Robot Dynamics and Control course (1st year, 2nd semester), MSc Robotics Engineering, University of Genoa.

## Content

The robot is a 3R planar manipulator (three 20 cm links) following the Denavit-Hartenberg convention. In both cases the gains are K<sub>p</sub> = 5.0 and K<sub>d</sub> = 4.5, and the torques required at t = 10 s are computed.

| Folder | Controller | Motion |
|---|---|---|
| `A31_…` | **PD control** | From [10°, 20°, −30°] to [40°, −10°, −50°] within 10 s |
| `A32_…` | **Computed torque control**: the robot dynamics is compensated, so the PD acts on a linearized system | Polynomial trajectory from [10°, 20°, −30°] to [30°, 40°, −10°] in 10 s |

`x_robot_structure_3r.slx` is the Simscape model of the robot, used by both controllers. `Assignment_3.pdf` contains the full assignment text with all the parameters.

## Usage

Requires MATLAB with Simulink and Simscape Multibody.

**A3.1:**
1. Run `a31_load_param_and_robot.m` to load the robot and the parameters.
2. Open and run `A31_S6504193_Martinenghi.slx`.

**A3.2:**
1. Run `a32_load_param_and_robot.m` to load the robot and the parameters.
2. Open and run `A32_S6504193_Martinenghi.slx`.

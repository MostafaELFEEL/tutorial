# ROS2_tutorial
# ROS 2 Tutorial Environment Setup

This repository contains instructions for setting up your environment for a ROS 2 tutorial. Follow these steps to get started.

## Prerequisites

Before you begin, make sure you have the following prerequisites installed:

- A Linux-based operating system (ROS 2 is primarily supported on Ubuntu 22.04)
- [ROS 2](https://docs.ros.org/en/humble/Installation.html)
- [CoppeliaSim Edu V4 for Ubuntu 22.04](https://your-coppelia-download-link-here](https://coppeliarobotics.com/downloads?flavor=edu))


## Getting Started

1. **Create a Directory**: Open your terminal and create a directory for your ROS 2 tutorial. You can name it whatever you like. In this example, we'll call it `ros2_tutorial`.

   ```bash
   mkdir ros2_tutorial
   cd ros2_tutorial

2. **Download the Repository**:
   ```bash
   https://github.com/MostafaELFEEL/ROS2_tutorial.git
3. **Building the packages**:
   ```bash
   colcon build

4. **Sourcing Workspace in .bashrc**:
   ```bash
   gedit ~/.bashrc
   ```

   **Paste the following line in bashrc**:
   ```bashrc
   source ~/ros2_tutorial/install/setup.bash
   ```
**Now you're all set!**


## Project 1: Running your first node.
**In a terminal run**:
```bash
ros2 run my_robot_controller test_node
```
**Observe the terminal as it prints the counter every second.**
## Porject 2: Running your first subscribe message.
**In a terminal run**:
```bash
ros2 run turtlesim turtlesim_node
```
**In a second terminal run**:
```bash
ros2 run turtlesim turtle_teleop_key
```
**In a third terminal run**:
```bash
ros2 run my_robot_controller pose_sub
```
**Control the turtle's movement in the teleop terminal by giving commands using the keys 'w,' 'a,' 's,' and 'd.' Simultaneously, observe the turtle's pose changes in the terminal.**
## Project 3: Turtle draws a circle.
**In a terminal run**:
```bash
ros2 run turtlesim turtlesim_node
```
**In a second terminal run**:
```bash
ros2 run my_robot_controller draw_circle
```
**Watch the turtle as it draws a circle.**
## Project 4: Turtle controller.
**In a terminal run**:
```bash
ros2 run turtlesim turtlesim_node
```
**In a second terminal run**:
```bash
ros2 run my_robot_controller closed_loop
```
**In this project, observe how the turtle is controlled to prevent it from coming into contact with the edges. Additionally, the SetPen service is utilized to alter the pen color when the turtle moves into the left half and revert to the original color when it moves back to the right half.**
## Project 5: Publisher_Subscriber nodes.
**In a terminal run**:
```bash
ros2 run pubsub sub
```
**In a second terminal run**:
```bash
ros2 run pubsub pub
```
**Simple Publisher-Subscriber Nodes.**
## Project 6: Turtle Draws shapes using parametric equation
**In a terminal run**:
```bash
ros2 run pubsub shapeNode
```
**In a second terminal run**:
```bash
ros2 run turtlesim turtlesim_node
```
**In a third terminal run**:
```bash
ros2 run pubsub turtleCommander
```
**Enter one of these shape commands (heart, star, epicycloid) in the shapeNode terminal and observe the turtle as it draws the corresponding shape.** 

| Image 1 | Image 2 | Image 3 |
| ------- | ------- | ------- |
| ![Image 1](https://github.com/MostafaELFEEL/ROS2_tutorial/assets/106331831/5895ed29-8c63-4988-b8a0-9d973779c5f3) | ![Image 2](https://github.com/MostafaELFEEL/ROS2_tutorial/assets/106331831/75bc428c-0c59-4929-884a-c7d65db8dbc0) | ![Image 3](https://github.com/MostafaELFEEL/ROS2_tutorial/assets/106331831/ed5de0a2-cd30-41ac-9eb7-1afa3a06f22f) |

## Project 7: Model vs Simulation on CoppeliaSim
**Automated**
**In a terminal run**:
```bash
cd CoppeliaSim_Edu_V4_5_1_rev4_Ubuntu22_04 && ./coppeliaSim.sh
```
**Open Coppeliasim and select robot.ttt from extra folder.**

**In a second terminal run**:
```bash
ros2 run pubsub diffdrivetime
```
**Real-Time Manual**:
**In a terminal run**:
```bash
cd CoppeliaSim_Edu_V4_5_1_rev4_Ubuntu22_04 && ./coppeliaSim.sh
```
**Open Coppeliasim and select robot.ttt from extra folder.**

**In a second terminal run**:
```bash
ros2 run pubsub diffdrive
```
**In a third terminal run**:
```bash
ros2 run pubsub shapeNode
```


# Ball Catching via 6R Manipulator

## Project Overview
This project involves the development of control algorithms for a 6R robotic manipulator designed to catch a moving ball. The system integrates real-time motion planning to calculate the precise trajectory of the manipulator's arm and catch the ball in a simulated environment. The manipulator's control is implemented using ROS (Robot Operating System) and Gazebo, allowing for simulation and testing before real-world deployment.

## Key Features
- **Real-time motion planning** for robotic arm control.
- **Trajectory estimation and optimization** to accurately predict and catch the ball.
- **ROS and Gazebo integration** for control and simulation.
- **Control algorithms** designed to enhance the accuracy and efficiency of the catching mechanism.

## Tools Used
- **ROS** (Robot Operating System)
- **Gazebo** (Robotic Simulator)
- **Python** (Control algorithms and simulation management)
- **C++** (ROS node development and motion planning)
- **RViz** (Visualization of robot movements)

## Installation

To run this project on your local machine, follow these steps:

### 1. Set up ROS environment:
Ensure that you have ROS installed. This project was developed on **ROS Noetic** (Ubuntu 20.04). You can install ROS by following the official [ROS installation guide](http://wiki.ros.org/noetic/Installation).

### 2. Install Dependencies:
You will need to install Gazebo and other required ROS packages:

```bash
sudo apt-get install gazebo11 libgazebo11-dev
sudo apt-get install ros-noetic-ros-control ros-noetic-ros-controllers
sudo apt-get install ros-noetic-trajectory-msgs
```
### 3. Clone the repository:
Clone the repository to your workspace:

```bash
cd ~/catkin_ws/src
git clone https://github.com/kirankigi5/catkin_ws.git
cd ~/catkin_ws
catkin_make
```
### 4. Run the simulation:
Once everything is set up, you can run the Gazebo simulation with the following command:

```bash
roslaunch <your_package> <launch_file>.launch
```

## Project Structure

- `src/`: Contains the ROS nodes for control algorithms and simulation setup.
- `launch/`: Contains ROS launch files to start various simulations.
- `config/`: Contains configuration files for robot parameters and controllers.
- `urdf/`: Contains the Unified Robot Description Format (URDF) files for the 6R manipulator model.
- `scripts/`: Contains Python scripts for control logic and simulation management.

## How It Works

1. **Trajectory Prediction**: The ball's trajectory is predicted based on its current velocity and motion. The system uses control algorithms to compute the ideal position and orientation for the manipulator.
   
2. **Motion Planning**: Using ROS's MoveIt! and Gazebo, real-time motion planning is performed to calculate the required joint positions for the 6R manipulator to catch the ball.

3. **Catching Mechanism**: The manipulator adjusts its position to intercept the ball based on continuous feedback from sensors in the Gazebo simulation.

## Future Work
- Implementing feedback from real-world sensors for a physical manipulator.
- Optimizing control algorithms for handling high-speed projectiles.
- Integrating machine learning-based prediction models for improved trajectory forecasting.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements
- Special thanks to **Prof. Spandan Roy** for his guidance and support during this project.
- The robotics simulation environment was powered by [ROS](https://www.ros.org/) and [Gazebo](http://gazebosim.org/).

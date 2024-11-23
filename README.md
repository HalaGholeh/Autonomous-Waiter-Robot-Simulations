# Autonomous-Waiter-Robot-Simulations

## How to run:

### System Requirements:
* **Host System:** Windows 11 
* **Development Environment:** Ubuntu 22.04.4 LTS running via WSL (Windows Subsystem for Linux) 
* **ROS2 Distribution:** Humble 
* **Simulation Tools:** 
  * Gazebo for simulation
  * RViz for visualization

### Step-by-Step Instructions:
* **Locate and click on the dev_ws.zip file.**
* **Click the Download button to download the zipped folder to your local machine.**
![image](https://github.com/user-attachments/assets/5982f975-0af5-4438-8aba-76d0b671be13)

### Extract the Folder
* **After downloading, extract the dev_ws.zip folder to a desired location on your system**
* **Set UP the Development Workspace in WSL**
  * Open WSL (Ubuntu 22.04.4 LTS in my case).
  * Navigate to the dev_ws directory.
  * To ensure that the contents of the dev_ws folder are as expected, use ls command, this command lists the contents of the current directory. It should display files like src/, install/, build/, etc.
   ![image](https://github.com/user-attachments/assets/29551d91-970f-4f1d-b05a-bb4943b285df)

### Running the Simulation
To start the simulation run the following command in your terminal:
**ros2 launch my_bot launch_sim.launch.py**
* This command will launch the simulation in Gazebo, opening a virtual space environment where the Autonomous Waiter Robot will be placed.
* Once the command is executed, you should see Gazebo running with the robot in a 3D simulated environment.
  ![image](https://github.com/user-attachments/assets/cf3954c4-c731-4026-a60f-7ab2323c5b9f)

### Controlling the Robot
By default, the robot will placed in the environment, but it will not move. To control the robot’s movements, you need to open a second Terminal and run the following command:
**ros2 run teleop_twist_keyboard teleop_twist_keyboard**
* This command will allow you to control the robot using the keyboard.
* You can navigate the robot and control its speed using the arrow keys on your keyboard.
* **Note:** The terminal running the teleop_twist_keyboard command must remain active and open in order for the controls to work. If the terminal is closed or minimized, the robot will not respond to movement commands.
* Once the terminal is running, you can use the following keys to control the robot:
 * I: Move the robot forward.
 * L: Turn the robot right.
 * J: Turn the robot left.
 * K: Stop the robot.
Here is a link for running teleop_twist_keyboard with Gazebo: https://youtu.be/FbXKk7vDK7c

### Running RViz2 for Visualization
To visualize the robot and the simulation environment, you need to run RViz2 in a separate terminal. Follow these steps:
  * 1.	Open a new terminal “don’t close any previous terminal”
  * 2.	Run the following command: **rviz2**
* This will launch RViz2, a 3D visualization tool, where you can see the robot and its surroundings the simulation.
* In RViz2, you will be able to visualize the robot’s sensor data, its path, and other relevant information.

![image](https://github.com/user-attachments/assets/1f27155a-6555-44a4-916f-663ae282c2bf)
**In RViz2 in the left side put the Fixed Frame to the base_link**
![image](https://github.com/user-attachments/assets/2220d6f8-bc1e-4363-a42d-d502d05359b5)








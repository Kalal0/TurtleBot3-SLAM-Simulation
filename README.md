# TurtleBot3-SLAM-Simulation

  Now moving on from the Arudino Arm, we'll be using the TurtleBot3 robot in a simulation. TurtleBot3 is a 2 wheel robot that operates similar to how a Roomba vacuum cleaner does. The simulation will be ran in Gazebo for the virtual enviroment and RVIZ paired with SLAM (Simultaneous Localization and Mapping) will display the mapping process the bot goes through. 
  
  - Ubuntu 20.04.4
  - ROS NOETIC
  
  Reality:
  
  ![image](https://user-images.githubusercontent.com/109832303/184434019-f9d1bb9b-9cd8-4f77-bd4a-d5e677fd77a0.png)


  
  Simulation:
  
  
![image](https://user-images.githubusercontent.com/109832303/184434098-3fac39f1-02cf-4054-9b94-bd0f3ffa8ef7.png)


# Installing TurtleBot3: 

CMD commands: 

    1 - sudo apt-get install ros-noetic-joy ros-noetic-teleop-twist-joy \
      ros-noetic-teleop-twist-keyboard ros-noetic-laser-proc \
      ros-noetic-rgbd-launch ros-noetic-rosserial-arduino \
      ros-noetic-rosserial-python ros-noetic-rosserial-client \
      ros-noetic-rosserial-msgs ros-noetic-amcl ros-noetic-map-server \
      ros-noetic-move-base ros-noetic-urdf ros-noetic-xacro \
      ros-noetic-compressed-image-transport ros-noetic-rqt* ros-noetic-rviz \
      ros-noetic-gmapping ros-noetic-navigation ros-noetic-interactive-markers

    2 - sudo apt install ros-noetic-dynamixel-sdk
    
    3 - sudo apt install ros-noetic-turtlebot3-msgs
    
    4 - sudo apt install ros-noetic-turtlebot3


# Running the Simulation: 

  As stated above we'll be using gazebo to run a virtual enviroment. You can create your own enviroment, but for simplicity sake we'll use a pre-existing one.
  
  
  1 - Open a new terminal and input the following commands: 
  
      1 - source /home/*username*/catkin_*workspace name*/devel/setup.bash
      2 - export TURTLEBOT3_MODEL=burger
      3 - roslaunch turtlebot3_gazebo turtlebot3_house.launch
 Replace the *username* and *workspace name* tags accordingly 
 
 2 - Open another terminal amd input the following commands:
 
    1 - source /home/*username*/catkin_*workspace name*/devel/setup.bash
    2 - roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
    3 - export TURTLEBOT3_MODEL=burger
    
 3 - Open another terminal and input the following commands: 
 
    1 - source /home/*username*/catkin_*workspace name*/devel/setup.bash
    2 - roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
    3 - export TURTLEBOT3_MODEL=burger
 
      
    

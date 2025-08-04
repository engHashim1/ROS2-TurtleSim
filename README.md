# ROS2-TurtleSim
This project documents my hands-on experience with ROS2 Humble using the turtlesim package

ROS2 Humble Turtlesim Tutorial
Overview

This repository contains my exploration of ROS2 Humble using the turtlesim package. I followed the official ROS2 tutorials to learn about nodes, topics, services, and basic ROS2 commands.
Key Features Explored

✔ Running the turtlesim simulator
✔ Controlling the turtle using ROS2 nodes
✔ Understanding ROS2 topics and services
✔ Using rqt for visualization and debugging
✔ Customizing turtle movement with Python scripts
Difference Between Nodes and Topics in ROS2
Nodes

    A node is an executable process that performs computation in ROS2.

    Nodes are modular—each node is responsible for a single task (e.g., controlling the turtle, reading sensor data).

    Example:

        turtlesim_node (runs the turtle simulation)

        teleop_twist_keyboard (sends movement commands)

Topics

    A topic is a communication channel that nodes use to exchange messages.

    Topics use a publish-subscribe model:

        Publisher Node → Sends data (e.g., /turtle1/cmd_vel for movement commands).

        Subscriber Node → Receives data (e.g., turtlesim_node listens to /turtle1/cmd_vel).

    Example:

        /turtle1/pose (turtle's position)

        /turtle1/cmd_vel (velocity commands)

Key Differences
Feature	Node	Topic
Purpose	Executes tasks	Transfers data
Communication	Can publish/subscribe	Only carries messages
Example	turtlesim_node	/turtle1/cmd_vel
Demo Media

📷 Screenshots & Videos

Node list
<img width="1906" height="933" alt="لقطة شاشة 2025-08-04 050052" src="https://github.com/user-attachments/assets/82429c15-b729-4a91-8419-726c8dc46bdb" />

    Turtlesim Basic Movement
<img width="1912" height="918" alt="لقطة شاشة 2025-08-04 045553" src="https://github.com/user-attachments/assets/416e5190-9a95-4fbe-b376-b3dabbcbf8f3" />

    RQT Graph Visualization
<img width="1915" height="924" alt="لقطة شاشة 2025-08-04 045120" src="https://github.com/user-attachments/assets/351f2bc1-d1c7-48a8-a805-5366fde92892" />

cmd_vel
<img width="1918" height="989" alt="لقطة شاشة 2025-08-04 050906" src="https://github.com/user-attachments/assets/19500fd5-174a-4dda-9bc2-93358bbde600" />

How to Run

    Start Turtlesim
    bash

ros2 run turtlesim turtlesim_node

Control the Turtle
bash

ros2 run turtlesim turtle_teleop_key

View Active Topics
bash

ros2 topic list

Visualize with RQT
bash

    rqt

Conclusion

This project helped me understand ROS2 fundamentals, including nodes, topics, and basic robot control. The turtlesim package is a great way to learn ROS2 before working on real robots!

🚀 Next Steps: Explore ROS2 services, actions, and custom message types.

📌 Author: [Hashim Hasan]
🔗 ROS2 Version: Humble Hawksbill

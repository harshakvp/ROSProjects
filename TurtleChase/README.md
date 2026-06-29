# Turtle Chase

A ROS 2 application that demonstrates autonomous escape behavior using publishers, subscribers, and real-time pose feedback in the **turtlesim** simulator. The project simulates a thief turtle that continuously monitors the position of a police turtle and dynamically flees while avoiding the simulator boundaries.

<p align="center">
  <img src="https://github.com/user-attachments/assets/33c24fcc-c082-4ae6-8cb4-01dc42c0b901" width="100%">
</p>

---

## Project Overview

The application consists of a single ROS 2 node that controls the behavior of the **thief turtle** within the `turtlesim` environment.

The node performs the following tasks:

* Spawns a new turtle named `thief_turtle` using the `/spawn` service.
* Subscribes to the pose of both the police turtle (`/turtle1`) and the thief turtle.
* Continuously calculates the distance between the two turtles.
* Detects when the police turtle enters a predefined safety radius.
* Computes an escape direction opposite to the police turtle.
* Ensures the escape path remains within the simulator boundaries.
* Publishes velocity commands to move the thief turtle away from the police.
* Stops the thief turtle when the police is outside the detection range.

---

## Features

* Autonomous escape behavior
* Dynamic obstacle avoidance
* Boundary-aware motion planning
* Publisher–Subscriber communication
* ROS 2 Services
* Real-time pose tracking
* Reactive robot behavior

---

## Project Structure

```text id="ug5j7k"
TurtleChase/
│
├── thief_turtle_node.py
│
└── README.md
```

---

## Repository Notes

This repository contains the **core Python source code** for the project. It does **not** include the complete ROS 2 package configuration files such as:

* `package.xml`
* `setup.py`
* `setup.cfg`
* `CMakeLists.txt`

To run this project, you should:

1. Create a ROS 2 Python package.
2. Add the provided source file to your package.
3. Configure the package using the required ROS 2 build files.
4. Build the workspace:

```bash id="8gzf6i"
colcon build
```

5. Source the workspace:

```bash id="g7bhku"
source install/setup.bash
```

6. Run the node using:

```bash id="qsgf88"
ros2 run <package_name> thief_turtle_node
```

---

## Technologies Used

* ROS 2
* Python
* turtlesim

---

## Author

### Harshak V P

Electrical and Electronics Engineering Undergraduate
Vellore Institute of Technology (VIT), Vellore

#### Connect

* GitHub: [harshakvp](https://github.com/harshakvp)
* LinkedIn: [Harshak V P](https://www.linkedin.com/in/harshakvp/)
* Portfolio: [harshakvp.dev](https://chain-science-5eb.notion.site/HARSHAK-V-P-4f4889ae8ebf4c05a5790637c39213ba)
* Email: [harshakvp.contact@gmail.com](mailto:harshakvp.contact@gmail.com)

---

This project was developed as part of my learning journey in ROS 2 and robotic software development. Feel free to explore, use, modify, and extend it for your own learning and experimentation.

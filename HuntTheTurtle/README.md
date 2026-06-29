# Hunt The Turtle

A ROS 2 application that demonstrates autonomous target hunting using publishers, subscribers, services, and custom interfaces in the **turtlesim** simulator. The project consists of a turtle spawner node that continuously spawns turtles and a controller node that autonomously navigates `turtle1` to catch and remove them from the simulation.

<p align="center">
  <img src="https://github.com/user-attachments/assets/40829d57-f72f-4df8-a7dd-6d96f7fd7e38" width="100%">
</p>

---

## Project Overview

The application consists of two ROS 2 nodes working together to create a dynamic turtle hunting simulation.

### Turtle Spawner Node

The **TurtleSpawnerNode** is responsible for managing turtles within the simulator. It:

* Periodically spawns turtles at random positions.
* Assigns a unique name to every spawned turtle.
* Maintains a list of all active turtles.
* Publishes the active turtle list using a custom `TurtleArray` message.
* Provides a `catch_turtle` service that removes turtles from the simulator through the `/kill` service.

### Turtle Controller Node

The **TurtleControllerNode** controls `turtle1` and performs autonomous target tracking. It:

* Subscribes to the `alive_turtles` topic.
* Tracks the pose of `turtle1` and all spawned turtles.
* Supports two hunting strategies:

  * Chase the first turtle in the list.
  * Chase the closest available turtle.
* Automatically calls the `catch_turtle` service when the target turtle is reached.

---

## Features

* Autonomous turtle hunting
* Random turtle spawning
* Publisher–Subscriber communication
* ROS 2 Services
* Custom Messages and Services
* Parameterized controller behavior
* Real-time target selection

---

## Project Structure

```text
HuntTheTurtle/
│
├── turtle_controller_node.py
├── turtle_spawner_node.py
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
* Custom message and service interface definitions

To run this project, you should:

1. Create a ROS 2 Python package.
2. Add the provided source files to your package.
3. Create the required custom interfaces (`Turtle`, `TurtleArray`, and `CatchTurtle`).
4. Configure the package using the required ROS 2 build files.
5. Build the workspace:

```bash
colcon build
```

6. Source the workspace:

```bash
source install/setup.bash
```

---

## Example Parameters

```yaml
# Turtle Spawner Node
spawn_frequency: 0.5
turtle_name_prefix: "turtle"

# Turtle Controller Node
catch_closest_turtle: true
```

---

## Technologies Used

* ROS 2
* Python
* turtlesim
* Custom ROS 2 Messages
* Custom ROS 2 Services

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

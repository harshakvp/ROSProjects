# ROS2 Projects

[![Stars](https://img.shields.io/github/stars/harshakvp/ROSProjects?style=flat-square\&label=stars)](https://github.com/harshakvp/ROSProjects/stargazers)
[![Forks](https://img.shields.io/github/forks/harshakvp/ROSProjects?style=flat-square\&label=forks)](https://github.com/harshakvp/ROSProjects/forks)
[![Watchers](https://img.shields.io/github/watchers/harshakvp/ROSProjects?style=flat-square\&label=watchers)](https://github.com/harshakvp/ROSProjects/watchers)
[![Contributors](https://img.shields.io/github/contributors/harshakvp/ROSProjects?style=flat-square\&label=contributors)](https://github.com/harshakvp/ROSProjects/graphs/contributors)
![Last Commit](https://img.shields.io/github/last-commit/harshakvp/ROSProjects?style=flat-square\&label=last%20commit)
![Repo Size](https://img.shields.io/github/repo-size/harshakvp/ROSProjects?style=flat-square\&label=repo%20size)
![Projects](https://img.shields.io/badge/projects-2-blue?style=flat-square)
![Visitors](https://visitor-badge.laobi.icu/badge?page_id=harshakvp.ROSProjects)

A collection of ROS 2 projects developed as part of my learning journey in robotics, autonomous systems, and robotic software development. This repository contains multiple ROS 2 packages demonstrating core concepts such as publishers, subscribers, services, actions, custom interfaces, and inter-node communication using the **turtlesim** simulator.

---

## Projects

### 1. HuntTheTurtle

A ROS 2 application that demonstrates autonomous target hunting using publishers, subscribers, services, and custom interfaces in the **turtlesim** simulator.

<p align="center">
  <img src="https://github.com/user-attachments/assets/40829d57-f72f-4df8-a7dd-6d96f7fd7e38" width="100%">
</p>

**Project Directory:**
[HuntTheTurtle](https://github.com/harshakvp/ROSProjects/tree/main/HuntTheTurtle)

---

### 2. TurtleChase

A ROS 2 application that demonstrates autonomous leader-follower behavior using publishers, subscribers, and real-time pose feedback in the **turtlesim** simulator.

<p align="center">
  <img src="https://github.com/user-attachments/assets/33c24fcc-c082-4ae6-8cb4-01dc42c0b901" width="100%">
</p>

**Project Directory:**
[TurtleChase](https://github.com/harshakvp/ROSProjects/tree/main/TurtleChase)

---

## Repository Structure

```text
ROSProjects/
│
├── HuntTheTurtle/
│
├── TurtleChase/
│
└── README.md
```

---

## Repository Notes

This repository contains the **core source code** for each project. It does **not** include the complete ROS 2 package configuration files such as:

* `package.xml`
* `setup.py`
* `setup.cfg`
* `CMakeLists.txt`
* Custom message/service definitions (where applicable)

To run these projects, you should:

1. Create a ROS 2 workspace using `colcon`.
2. Recreate the required package structure.
3. Add the required ROS 2 configuration files.
4. Build the workspace:

```bash
colcon build
```

5. Source the workspace:

```bash
source install/setup.bash
```

---

## Tools Used

* ROS 2
* turtlesim
* Python
* Git
* GitHub

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

This repository is maintained for learning, experimentation, and ROS 2 application development. Feel free to explore, use, modify, and extend these projects.

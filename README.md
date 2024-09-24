# ros2india

This repository serves as a collection of various **ROS1** and **ROS2** projects. Each project is added as a Git submodule, allowing modular access and maintenance. This guide provides instructions on how to clone the repository with submodules, manage individual projects, and contribute to the collection.

## Table of Contents

1. [Overview](#overview)
2. [Cloning the Repository](#cloning-the-repository)
3. [Working with Submodules](#working-with-submodules)
    - [Adding a New Project](#adding-a-new-project)
    - [Updating Submodules](#updating-submodules)
4. [List of Projects](#list-of-projects)
5. [Contributing](#contributing)
6. [License](#license)

---

## Overview

The **ros2india** repository contains a variety of **ROS1** and **ROS2** projects, each housed in a separate directory. Each project is a standalone repository, added as a **Git submodule**, enabling easy management and modular development. You can clone and work with each project independently or with the whole collection.

Some projects currently included are:
- **NavRover**: A 4-wheeled rover capable of teleoperation, mapping, and autonomous navigation.
- (Add your other ROS1/ROS2 projects here.)

---

## Cloning the Repository

To clone the **ros2india** repository along with all its submodules (i.e., the individual ROS1/ROS2 projects), use the `--recurse-submodules` flag:

### Steps:

1. Open a terminal and run:
   ```bash
   git clone --recurse-submodules https://github.com/hwjalapeno/ros2india.git
   ```

2. Navigate into the cloned directory:
   ```bash
   cd ros2india
   ```

3. If you have already cloned the repository without the submodules, you can initialize and update the submodules manually:
   ```bash
   git submodule init
   git submodule update
   ```

---

## Working with Submodules

Each project inside **ros2india** is included as a submodule. Here’s how you can manage and interact with the individual projects.

### Adding a New Project

To add a new ROS1/ROS2 project to this repository, follow these steps:

1. Navigate to the root of the **ros2india** repository:
   ```bash
   cd /path/to/ros2india
   ```

2. Add the project repository as a submodule:
   ```bash
   git submodule add https://github.com/username/project-repo.git path/to/project-directory
   ```
   Replace:
   - `https://github.com/username/project-repo.git` with the repository URL of the project.
   - `path/to/project-directory` with the desired path within the **ros2india** directory.

3. Commit the changes:

   ```bash
   git add .
   git commit -m "Added [Project Name] as a submodule"
   git push origin main
   ```

### Updating Submodules

To pull the latest changes from a specific submodule:

```bash
git submodule update --remote --merge
```

To update all submodules:

```bash
git submodule update --remote
```

---

## List of Projects

### 1. [NavRover](https://github.com/jj7258/NavRover)
- **Description**: A 4-wheeled rocker mechanism-based rover with teleoperation, mapping, and navigation capabilities.
- **ROS Version**: ROS1 (Noetic)
- **Quick Start**:
  ```bash
  cd NavRover
  catkin_make  # or colcon build for ROS2
  source devel/setup.bash
  roslaunch navrover navrover.launch
  ```

### 2. [Project 2 Name]
- **Description**: (Add description here)
- **ROS Version**: (Specify ROS version)
- **Quick Start**:
  (Add instructions here)

(Repeat this for all other projects)

---

## Contributing

Contributions are welcome to add new ROS1/ROS2 projects to **ros2india** or improve the existing ones. To contribute:

1. Fork the repository.
2. Add your project as a submodule following the steps in the [Adding a New Project](#adding-a-new-project) section.
3. Create a pull request (PR) with a description of the project.

---

## License

This repository is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
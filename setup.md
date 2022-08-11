---
layout: page
title: noetic setup
permalink: /setup noetic/
nav_order: 3
---

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

# Setup Guidelines

- Always use the apt installation preferably as it is more stable
- Refer the youtube video on the setup page (end of page) if available
- If not, just follow the installation step-by-step

## Note on bashrc

[What is bashrc](https://unix.stackexchange.com/questions/129143/what-is-the-purpose-of-bashrc-and-how-does-it-work)

Read the above article and understand what bashrc represents, it is a file that is called everytime /
a new terminal is created

We run the commands:
```bash
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```
These basically put the source for ros on bashrc

## After installation

Simply run the command **roscore** to verify if installtion has happened properly



# Setting up your Workspace

**Catkin is the ROS build system which comprises of a set of CMake macros and custom Python scripts to provide extra functionality on top of normal CMake**

- In general after using catkin, the only files you may have to edit will be the **CMakeLists.txt** and the **package.xml** files

- A workspace is mandatory for ROS as all the nodes, test scripts, backend servers, parameter servers, etc., all live within this workspace

## Setting up a trial workspace

1. Check if the ros setup.bash has been added to your bashrc file

	```bash
	nano ~/.bashrc
	```
	Check the last line of this

2. Now we'll start creating the actual workspace

    ```bash
    mkdir -p ~/catkin_ws/src
    cd ~/catkin_ws/src
    catkin_init_workspace
    cd ~/catkin_ws
    catkin_make
    ```

    At the end of the above statements you will have a **build, devel and src** inside your workspace
    - Devel will contain the setup files which will have to be sourced everytime we work within the workspace
    - Better to add this ~/catkin_ws/devel/setup.bash to the .bashrc file if we only have one workspace
    - src is where all your ros packages are going to be

3. Let's create a trial ros package
    
    ```bash
    cd ~/catkin_ws/src
    catkin_create_pkg sush_trials rospy
    ```

    Now your ~/catkin_ws/src will have a sush_trials folder inside which we will again have a src folder, CMakeLists.txt and a package.xml which are all package specific. **Any python scripts for this particular package will be stored in this src directory**


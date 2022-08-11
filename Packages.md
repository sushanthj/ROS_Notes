---
layout: page
title: Packages
permalink: /packages/
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

[Tutorial Page 1](http://wiki.ros.org/ROS/Tutorials/NavigatingTheFilesystem)
[Tutorial Page 2](http://wiki.ros.org/ROS/Tutorials/CreatingPackage)

# Filesystem Tools

**rospack** gives info about packages and it takes attributes like *rospack find roscpp*

- **find** : returns path to package
- **depends** : returns list of dependencies for all packages
- **depends-on** : returns a list of dependencies to a particular package
- **export** : return flags necessary for building and linking against a package

## rosbash

this is a suite which contains bash functions which is the ros equivalent of normal bash commands we are used to like **cd, ls**

- **roscd** is just like **cd**, it allows us to change working directories like *roscd roscpp*
- **rosls** returns contents of a directory

# Creating Packages

## Build Systems






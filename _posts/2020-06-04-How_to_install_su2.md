---
title: "How to install SU2 in MPI mode on Linux"
layout: single
categories:
  - howto
author_profile: true
toc: false
---

## Pre-requisite installations installations

1. Install swig

    ```bash
    sudo yum install swig
    ````

2. Install [MPICH](/posts/2020-06-05_How_to_Install_MPICH/)

3. Install MPI for Python ([mpi4py](/posts/2020-06-05_How_to_Install_mpi4py/))

4. It is not needed to install Meson, Ninja, CoDiPack and MeDiPack. SU2 installation process does that for you and ensures the correct versions.


## Installation


1. Make sure you are using bash.

    ```bash
    echo $SHELL
    # if it is not bash, command: bash
    ```

2. Create a folder for mpich

    ```bash
    mkdir /home/you/su2
    ```

3. Download to that folder the latest stable source code version of su2 from: <https://su2code.github.io/download.html>

4. Unzip the file

    ```bash
    unzip su2code...zip
    ```

5. Create 2 other folders

    ```bash
    mkdir /home/you/su2/build
    ```

6. Enter the unziped su2 source code folder and run mason

    ```bash
    ./meson.py build -Denable-autodiff=true --prefix=/home/you/su2/build
    cd /home/you/su2/su2code...
    ```

7. Compile with ninja

    ```bash
    ./ninja -C build install
    ```


[Learn more](https://su2code.github.io/docs_v7/Build-SU2-Linux-MacOS/)
[Install on Windows](https://su2code.github.io/docs_v7/SU2-Windows/)
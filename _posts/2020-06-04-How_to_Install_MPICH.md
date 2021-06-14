---
title: "How to install MPICH"
layout: single
classes: wide
categories:
  - howto
author_profile: true
toc: false
sidebar_ads: true
---



1. Make sure you are using bash. 

    ```bash
    echo $SHELL
    ``` 

2. Create a folder for mpich

    ```bash
    mkdir /home/you/mpich
    # If it is not bash, command: bash
    ```

3. Download to that folder the latest stable version of mpich from: <https://www.mpich.org/downloads/>

4. Unpack the tar file that you just downloaded, mpich-x-y-z.tar.gz, where x-y-z is the version

    ```bash
    tar xfz mpich-x-y-z.tar.gz
    ```

5. Create 2 other folders

    ```bash
    mkdir /home/you/mpich/build
    mkdir /home/you/mpich/mpich-install
    ```

6. Enter the build directory and run the configuration script.

    ```bash
    cd /home/you/mpich/build ../mpich-x-y-z/configure --with-device=ch4:ofi -prefix=/home/you/mpich/mpich-install 2>&1 | tee c.txt
    ```

7. Build mpich. Run command and go for a coffee:

    ```bash
    make 2>&1 | tee m.txt
    ```

8. Install MPICH.

    ```bash
    make install 2>&1 | tee mi.txt	
    ```

9. Add the bin subdirectory of the installation directory to your path:

    ```bash
    export PATH=/home/you/mpich/mpich-install/bin:$PATH
    ```

10. Check if the installation went well:

    ```bash
    which mpicc
    which mpiexec
    ```

11. Test mpi in your machine by using the example file that the building process creates. That simple program computes the value of PI. If your machine has NC cores, then:

    ```bash
    mpiexe -n NC ./examples/cpi
    ```

[Learn more](https://www.mpich.org/static/downloads/3.4.2/mpich-3.4.2-installguide.pdf){:target="_blank"}
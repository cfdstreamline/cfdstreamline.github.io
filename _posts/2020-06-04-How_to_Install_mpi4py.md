---
title: "How to install mpi4py"
layout: single
classes: wide
categories:
  - howto
author_profile: true
toc: false
sidebar_ads: true
---

MPI for Python enables MPI usage for the Python language, allowing programmers to write codes that leverage multiple processor computing systems.

1. In a bash terminal, sudo your user:

   ```bash
   sudo su
   ```

2. Make sure you have Python 3 developer installed:

   ```bash
   yum install python3-devel
   ```

3. If you don't have pip installed, install it with:

   ```bash
   easy_install pip
   ```

4. Finally, install mpi4py.

   ```bash
   pip3 install mpi4py
   ```

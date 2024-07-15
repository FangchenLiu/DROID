# Using MOKA with DROID

This repository contains the code for setting up the robot system used in [MOKA](https://arxiv.org/abs/2403.03174). It is based on the great efforts provided by [DROID](https://droid-dataset.github.io), a large-scale and in-the-wild dataset collection platform of robot manipulation.

For more information about DROID, please see the following links: 

[**[Homepage]**](https://droid-dataset.github.io) &ensp; [**[Documentation]**](https://droid-dataset.github.io/droid) &ensp; [**[Paper]**](https://arxiv.org/abs/2403.12945) &ensp; [**[Dataset Visualizer]**](https://droid-dataset.github.io/dataset.html)

![](https://droid-dataset.github.io/droid/assets/index/droid_teaser.jpg)

## Setup Guide

DROID assembled a easy-to-follow step-by-step guide for setting up the robot platform in [developer documentation](https://droid-dataset.github.io/droid).
This guide has been used to set up 18 DROID robot platforms over the course of the DROID dataset collection. Please refer to the steps in this guide for setting up your own robot. Specifically, you can follow these key steps:

1. [Hardware Assembly and Setup](https://droid-dataset.github.io/droid/docs/hardware-setup)
2. [Software Installation and Setup](https://droid-dataset.github.io/droid/docs/software-setup)
In step 2, you'll find the instructions about cloning the official [DROID](https://github.com/droid-dataset/droid) repository.
Change it to this repository to make it compatible with MOKA.

```bash
git clone git@github.com:FangchenLiu/DROID.git
pip install -e .

# Done like this to avoid dependency issues
pip install dm-robotics-moma==0.5.0 --no-deps
pip install dm-robotics-transformations==0.5.0 --no-deps
pip install dm-robotics-agentflow==0.5.0 --no-deps
pip install dm-robotics-geometry==0.5.0 --no-deps
pip install dm-robotics-manipulation==0.5.0 --no-deps
pip install dm-robotics-controllers==0.5.0 --no-deps
```
3. [Example Workflows to collect data or calibrate cameras](https://droid-dataset.github.io/droid/docs/example-workflows)

MOKA can be independent from the DROID platform. You can use your own robot platform to run MOKA by adapting your own robot and controller interface to the MOKA codebase. 
The MOKA codebase is designed to be modular and easy to adapt to different robot platforms.

If you encounter issues during setup, please raise them as issues in this github repo.

Acknowledgements:
- [DROID](https://droid-dataset.github.io) for providing the great robot platform and dataset collection infrastructure.
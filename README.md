# What's new on this fork
Addes support for the Nvidia RTX graphics cards (RTX 2060, 2070, 2080).
It is tested on Nvidia RTX 2080 Ti.

The original environment-gpu.yml file requires tensorflow 1.3.0 that does not support CUDA 10.
The latest GPUs, such as Nvidia RTX 2080 Ti require CUDA 10 or later.
This environment uses the latest tensorflow version (tf-nightly-gpu) that supports CUDA 10.
You can use this environment if you have a new GPU and you want to use it for your projects.
IMPORTANT WARNINGS: 
1) The trained models from the new tensorflow version are not compatible with older tensorflow versions. If you work on a team project, everyone should have the same tensorflow version.
2) The CarND-Capstone-Project requires tensorflow version 1.3.0 because Carla has this version installed. You can use the latest version for development but you should train the final model with version 1.3.0. You may use the Udacity's workspace or an AWS instance for the final training.


# CarND Term1 Starter Kit

[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

The purpose of this project is to provide unified software dependency support for students enrolled in Term 1 of the [Udacity Self-Driving Car Engineer Nanodegree](https://www.udacity.com/course/self-driving-car-engineer-nanodegree--nd013).

Python 3 is used for the entirety of term 1.

There are two ways to get up and running:

## [Anaconda Environment](doc/configure_via_anaconda.md)

Get started [here](doc/configure_via_anaconda.md). More info [here](http://conda.pydata.org/docs/).

Supported Sytems: Linux (CPU), Mac (CPU), Windows (CPU)     

| Pros                         | Cons                                               |
|------------------------------|----------------------------------------------------|
| More straight-forward to use | AWS or GPU support is not built in (have to do this yourself)              |
| More community support       | Implementation is local and OS specific            |
| More heavily adopted         |                                                    |

## [Docker](doc/configure_via_docker.md)

Get started [here](doc/configure_via_docker.md). More info [here](http://docker.com).

Supported Systems : AWS (CPU, [GPU](doc/docker_for_aws.md)), Linux (CPU), Mac (CPU), Windows (CPU)     

| Pros                                | Cons                                 |
|-------------------------------------|--------------------------------------|
| Configure once for all environments | More challenging to use              |
| AWS, GPU support                    | Less community support               |
| Practice with Docker              | Have to manage images and containers |
|                                     |                                      |

## Trouble Shooting

If you get an Import Error on cv2 and have ROS installed. See [here](https://stackoverflow.com/questions/43019951/after-install-ros-kinetic-cannot-import-opencv#).

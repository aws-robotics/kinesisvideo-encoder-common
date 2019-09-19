# ROS H264 Video Encoding Library for Amazon Kinesis Video Streams


## Overview
This repository contains the h264_encoder_core package, a library for encoding images into video frames. It is used by the `h264_video_encoder` node.

### License
The source code is released under [LGPL 2.1]. However, h264_encoder_core incorporates several different encoding components which may further restrict the license. By default, x264 is used for software encoding, thereby applying GPL to all of h264_encoder_core.

**Author**: AWS RoboMaker<br/>
**Affiliation**: [Amazon Web Services (AWS)]<br/>
**Maintainer**: AWS RoboMaker, ros-contributions@amazon.com

### Supported ROS Distributions
- Kinetic
- Melodic
- Dashing

### Build status
* Travis CI:
    * "master" branch [![Build Status](https://travis-ci.org/aws-robotics/kinesisvideo-encoder-common.svg?branch=master)](https://travis-ci.org/aws-robotics/kinesisvideo-encoder-common/branches)
    * "release-latest" branch [![Build Status](https://travis-ci.org/aws-robotics/kinesisvideo-encoder-common.svg?branch=release-latest)](https://travis-ci.org/aws-robotics/kinesisvideo-encoder-common/branches)
* ROS build farm:
    * ROS Kinetic @ u16.04 Xenial [![Build Status](http://build.ros.org/job/Kbin_uX64__h264_encoder_core__ubuntu_xenial_amd64__binary/badge/icon)](http://build.ros.org/job/Kbin_uX64__h264_encoder_core__ubuntu_xenial_amd64__binary)
    * ROS Melodic @ u18.04 Bionic [![Build Status](http://build.ros.org/job/Mbin_uB64__h264_encoder_core__ubuntu_bionic_amd64__binary/badge/icon)](http://build.ros.org/view/Mbin_uB64/job/Mbin_uB64__h264_encoder_core__ubuntu_bionic_amd64__binary/)
    * ROS Dashing @ u18.04 Bionic [![Build Status](http://build.ros2.org/job/Dbin_uB64__h264_encoder_core__ubuntu_bionic_amd64__binary/badge/icon)](http://build.ros2.org/job/Dbin_uB64__h264_encoder_core__ubuntu_bionic_amd64__binary)

## Installation

**Installing on Raspberry Pi**

It is recommended that you build this package from source for use on the Raspberry Pi. The ROS2 build farm doesn't have ffmpeg and related encoding libraries that are specific to the Raspberry Pi and required to enable hardware encoding. If installing from apt on RaspberryPi expect to use software encoding which can be very slow with limited computing resources. Raspberry Pi-compatible ffmpeg binaries can be found in the ppa:ubuntu-pi-flavour-makers/ppa repository . Once you add the PPA to your system and use rosdep install to fetch the dependencies, you will be able to build this package and link it against the compatible dependencies.

### Binaries
On Ubuntu you can install the latest version of this package using the following command

        sudo apt-get update
        sudo apt-get install -y ros-$ROS_DISTRO-h264-encoder-core

### Building from Source

To build from source you'll need to create a new workspace, clone and checkout the latest release branch of this repository, install all the dependencies, and compile. If you need the latest development features you can clone from the `master` branch instead of the latest release branch. While we guarantee the release branches are stable, __the `master` should be considered to have an unstable build__ due to ongoing development. 

- Install build tool: please refer to `colcon` [installation guide](https://colcon.readthedocs.io/en/released/user/installation.html)

- Create a ROS workspace and a source directory

        mkdir -p ~/ros-workspace/src

- Clone the package into the source directory . 

        cd ~/ros-workspace/src
        git clone https://github.com/aws-robotics/kinesisvideo-encoder-common.git -b release-latest

- Install dependencies

        cd ~/ros-workspace 
        sudo apt-get update && rosdep update
        rosdep install --from-paths src --ignore-src -r -y
        
_Note: If building the master branch instead of a release branch you may need to also checkout and build the master branches of the packages this package depends on._

- Build the packages

        cd ~/ros-workspace && colcon build

- Configure ROS library Path

        source ~/ros-workspace/install/local_setup.bash


[Amazon Web Services (AWS)]: https://aws.amazon.com/
[LGPL 2.1]: http://www.gnu.org/licenses/old-licenses/lgpl-2.1.html

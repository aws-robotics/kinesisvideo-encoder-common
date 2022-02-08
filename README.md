# ROS H264 Video Encoding Library for Amazon Kinesis Video Streams


## Overview
This repository contains the h264_encoder_core package, a library for encoding images into video frames. It is used by the `h264_video_encoder` node.

### License
The source code is released under [LGPL 2.1]. However, h264_encoder_core incorporates several different encoding components which may further restrict the license. By default, x264 is used for software encoding, thereby applying GPL to all of h264_encoder_core.

**Author**: AWS RoboMaker<br/>
**Affiliation**: [Amazon Web Services (AWS)]<br/>

RoboMaker cloud extensions rely on third-party software licensed under open-source licenses and are provided for demonstration purposes only. Incorporation or use of RoboMaker cloud extensions in connection with your production workloads or commercial product(s) or devices may affect your legal rights or obligations under the applicable open-source licenses. License information for this repository can be found [here](https://github.com/aws-robotics/kinesisvideo-encoder-common/blob/master/LICENSE.txt). AWS does not provide support for this cloud extension. You are solely responsible for how you configure, deploy, and maintain this cloud extension in your workloads or commercial product(s) or devices.

### Supported ROS Distributions
- Kinetic
- Melodic
- Dashing

## Installation

**Installing on Raspberry Pi**

It is recommended that you build this package from source for use on the Raspberry Pi. The ROS2 build farm doesn't have ffmpeg and related encoding libraries that are specific to the Raspberry Pi and required to enable hardware encoding. If installing from apt on RaspberryPi expect to use software encoding which can be very slow with limited computing resources. Raspberry Pi-compatible ffmpeg binaries can be found in the ppa:ubuntu-pi-flavour-makers/ppa repository . Once you add the PPA to your system and use rosdep install to fetch the dependencies, you will be able to build this package and link it against the compatible dependencies.

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

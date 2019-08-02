### NOTE: This release branch is no longer maintained and is deprecated. Please consider the using the `release-latest` branch for the latest stable sources.


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
- Lunar
- Melodic

### Build status

* Travis CI: [![Build Status](https://travis-ci.org/aws-robotics/kinesisvideo-encoder-common.svg?branch=master)](https://travis-ci.org/aws-robotics/kinesisvideo-encoder-common)
 * ROS build farm:
   * v1.0.0:
     * ROS Kinetic @ u16.04 Xenial [![Build Status](http://build.ros.org/job/Kbin_uX64__h264_encoder_core__ubuntu_xenial_amd64__binary/badge/icon)](http://build.ros.org/job/Kbin_uX64__h264_encoder_core__ubuntu_xenial_amd64__binary)

[Amazon Web Services (AWS)]: https://aws.amazon.com/
[LGPL 2.1]: http://www.gnu.org/licenses/old-licenses/lgpl-2.1.html

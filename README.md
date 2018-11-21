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

[Amazon Web Services (AWS)]: https://aws.amazon.com/
[LGPL 2.1]: http://www.gnu.org/licenses/old-licenses/lgpl-2.1.html

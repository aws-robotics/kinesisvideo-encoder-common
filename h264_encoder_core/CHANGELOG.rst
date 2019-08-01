^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package h264_encoder_core
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

2.0.1 (2019-08-01)
------------------
* increment patch version (`#30 <https://github.com/aws-robotics/kinesisvideo-encoder-common/issues/30>`_)
  Signed-off-by: Miaofei <miaofei@amazon.com>
* Add gtest and gmock as test dependencies (`#14 <https://github.com/aws-robotics/kinesisvideo-encoder-common/issues/14>`_)
  * Add gtest and gmock as test dependencies
  Signed-off-by: Miaofei <miaofei@amazon.com>
  * use the macro in aws_common to find test dependencies for ROS1 or ROS2
  Signed-off-by: Miaofei <miaofei@amazon.com>
  * update travis.yml to be compatible with specifying multiple package names
  Signed-off-by: Miaofei <miaofei@amazon.com>
  * update travis.yml test matrix
  Signed-off-by: Miaofei <miaofei@amazon.com>
  * update PACKAGE_NAMES
  Signed-off-by: Miaofei <miaofei@amazon.com>
* Update to use non-legacy ParameterReader API (`#9 <https://github.com/aws-robotics/kinesisvideo-encoder-common/issues/9>`_)
* Update to use new ParameterReader API (`#8 <https://github.com/aws-robotics/kinesisvideo-encoder-common/issues/8>`_)
  * fix h264_encoder_test to be compatible with new ParameterReader API
  * increment major version number in package.xml
* Merge pull request `#3 <https://github.com/aws-robotics/kinesisvideo-encoder-common/issues/3>`_ from mm318/bionic_hardware_encoder
  workaround avcodec_find_encoder_by_name() unreliably indicating that h264_omx codec is available
* implementing runtime solution for workaround
* workaround avcodec_find_encoder_by_name() unreliably indicating that h264_omx codec is available
* Contributors: M. M, Miaofei, Ross Desmond

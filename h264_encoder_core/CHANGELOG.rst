^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package h264_encoder_core
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

2.0.0 (2019-03-20)
------------------
* Update to use non-legacy ParameterReader API (`#9 <https://github.com/aws-robotics/kinesisvideo-encoder-common/issues/9>`_)
* Update to use new ParameterReader API (`#8 <https://github.com/aws-robotics/kinesisvideo-encoder-common/issues/8>`_)
  * fix h264_encoder_test to be compatible with new ParameterReader API
  * increment major version number in package.xml
* Merge pull request `#3 <https://github.com/aws-robotics/kinesisvideo-encoder-common/issues/3>`_ from mm318/bionic_hardware_encoder
  workaround avcodec_find_encoder_by_name() unreliably indicating that h264_omx codec is available
* implementing runtime solution for workaround
* workaround avcodec_find_encoder_by_name() unreliably indicating that h264_omx codec is available
* Contributors: M. M, Miaofei

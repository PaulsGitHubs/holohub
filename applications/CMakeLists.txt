# SPDX-FileCopyrightText: Copyright (c) 2022-2023 NVIDIA CORPORATION & AFFILIATES. All rights reserved.
# SPDX-License-Identifier: Apache-2.0
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

# Make sure to order by alphabetical list
add_holohub_application(basic_networking_ping DEPENDS
                        OPERATORS basic_network)

add_holohub_application(colonoscopy_segmentation HOLOSCAN_SAMPLE_APP)

add_holohub_application(deltacast_endoscopy_tool_tracking DEPENDS
                        OPERATORS lstm_tensor_rt_inference
                                  tool_tracking_postprocessor
                                  videomaster
                        )

add_holohub_application(deltacast_transmitter DEPENDS
                        OPERATORS videomaster
                        )

add_holohub_application(endoscopy_out_of_body_detection HOLOSCAN_SAMPLE_APP)

add_holohub_application(endoscopy_tool_tracking DEPENDS
                        OPERATORS lstm_tensor_rt_inference
                                  tool_tracking_postprocessor
                        HOLOSCAN_SAMPLE_APP
                        )

add_holohub_application(h264_endoscopy_tool_tracking DEPENDS 
                        OPERATORS video_encoder video_decoder
                                  video_read_bitstream video_write_bitstream
                                  tensor_to_video_buffer
                                  lstm_tensor_rt_inference
                                  tool_tracking_postprocessor
                        HOLOSCAN_SAMPLE_APP
                        )

add_holohub_application(h264_video_decode DEPENDS
                        OPERATORS video_decoder video_read_bitstream
                        HOLOSCAN_SAMPLE_APP)

add_holohub_application(high_speed_endoscopy DEPENDS
                        OPERATORS emergent_source)

add_holohub_application(multiai_ultrasound DEPENDS
                        OPERATORS visualizer_icardio
                        HOLOSCAN_SAMPLE_APP)

add_holohub_application(simple_radar_pipeline)                        

add_holohub_application(ultrasound_segmentation HOLOSCAN_SAMPLE_APP)

add_holohub_application(usb_hdmi_video_capture DEPENDS 
                        OPERATORS v4l2_video_capture)


# Copyright 2019 The MediaPipe Authors.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

load("@rules_cc//cc:cc_library.bzl", "cc_library")
load(
    "//mediapipe/framework/tool:mediapipe_graph.bzl",
    "mediapipe_binary_graph",
)

licenses(["notice"])

package(default_visibility = ["//visibility:public"])

cc_library(
    name = "mobile_calculators",
    deps = [
        "//mediapipe/calculators/core:packet_resampler_calculator",
        "//mediapipe/graphs/tracking/subgraphs:object_detection_gpu",
        "//mediapipe/graphs/tracking/subgraphs:object_tracking_gpu",
        "//mediapipe/graphs/tracking/subgraphs:renderer_gpu",
    ],
)

cc_library(
    name = "desktop_calculators",
    deps = [
        "//mediapipe/calculators/core:packet_resampler_calculator",
        "//mediapipe/graphs/tracking/subgraphs:object_detection_cpu",
        "//mediapipe/graphs/tracking/subgraphs:object_tracking_cpu",
        "//mediapipe/graphs/tracking/subgraphs:renderer_cpu",
    ],
)

mediapipe_binary_graph(
    name = "mobile_gpu_binary_graph",
    graph = "object_detection_tracking_mobile_gpu.pbtxt",
    output_name = "mobile_gpu.binarypb",
    deps = [":mobile_calculators"],
)

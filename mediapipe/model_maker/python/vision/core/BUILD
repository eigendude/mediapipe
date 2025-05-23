# Copyright 2022 The MediaPipe Authors.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

# Placeholder for internal Python strict library and test compatibility macro.
# Placeholder for internal Python strict test compatibility macro.

load("@rules_python//python:defs.bzl", "py_library", "py_test")

licenses(["notice"])

package(default_visibility = [
    "//mediapipe:__subpackages__",
])

py_library(
    name = "image_preprocessing",
    srcs = ["image_preprocessing.py"],
    deps = [
        "@model_maker_pip_deps_tensorflow//:pkg",
    ],
)

py_test(
    name = "image_preprocessing_test",
    srcs = ["image_preprocessing_test.py"],
    deps = [
        ":image_preprocessing",
        "@model_maker_pip_deps_numpy//:pkg",
        "@model_maker_pip_deps_tensorflow//:pkg",
    ],
)

py_library(
    name = "image_utils",
    srcs = ["image_utils.py"],
    deps = [
        "@model_maker_pip_deps_pillow//:pkg",
        "@model_maker_pip_deps_tensorflow//:pkg",
    ],
)

py_test(
    name = "image_utils_test",
    srcs = ["image_utils_test.py"],
    deps = [
        ":image_utils",
        ":test_utils",
        "@model_maker_pip_deps_tensorflow//:pkg",
    ],
)

py_library(
    name = "test_utils",
    srcs = ["test_utils.py"],
    deps = [
        "@model_maker_pip_deps_numpy//:pkg",
        "@model_maker_pip_deps_tensorflow//:pkg",
    ],
)

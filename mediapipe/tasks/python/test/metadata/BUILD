# Placeholder: load py_test

load("@rules_python//python:defs.bzl", "py_test")

package(
    default_visibility = [
        "//visibility:public",
    ],
    licenses = ["notice"],  # Apache 2.0
)

py_test(
    name = "metadata_test",
    srcs = ["metadata_test.py"],
    data = ["//mediapipe/tasks/testdata/metadata:data_files"],
    deps = [
        "//mediapipe/tasks/metadata:metadata_schema_py",
        "//mediapipe/tasks/metadata:schema_py",
        "//mediapipe/tasks/python/metadata",
        "//mediapipe/tasks/python/test:test_utils",
        "@flatbuffers//:runtime_py",
        "@mediapipe_pip_deps_absl_py//:pkg",
        "@mediapipe_pip_deps_six//:pkg",
    ],
)

py_test(
    name = "metadata_parser_test",
    srcs = ["metadata_parser_test.py"],
    deps = [
        "//mediapipe/tasks/python/metadata",
        "@mediapipe_pip_deps_absl_py//:pkg",
    ],
)

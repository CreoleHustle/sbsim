#     Copyright 2023 Google LLC
#
#     Licensed under the Apache License, Version 2.0 (the "License");
#     you may not use this file except in compliance with the License.
#     You may obtain a copy of the License at
#
#         https://www.apache.org/licenses/LICENSE-2.0
#
#     Unless required by applicable law or agreed to in writing, software
#     distributed under the License is distributed on an "AS IS" BASIS,
#     WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
#     See the License for the specific language governing permissions and
#     limitations under the License.
#
#      Top-level BUILD for Smart Buildings Smart Control

load("//devtools/python/blaze:pytype.bzl", "pytype_strict_library")

package(
    default_applicable_licenses = ["//third_party/py/smart_buildings:license"],
    default_visibility = ["//visibility:public"],
)

licenses(["notice"])

pytype_strict_library(
    name = "base_building",
    srcs = ["base_building.py"],
    srcs_version = "PY3",
    deps = [
        "//third_party/py/pandas",
        "//third_party/py/smart_buildings/smart_control/proto:smart_control_building_py_pb2",
        "//third_party/py/smart_buildings/smart_control/proto:smart_control_reward_py_pb2",
    ],
)

pytype_strict_library(
    name = "base_reward_function",
    srcs = ["base_reward_function.py"],
    srcs_version = "PY3",
    deps = [
        "//third_party/py/smart_buildings/smart_control/proto:smart_control_reward_py_pb2",
    ],
)

pytype_strict_library(
    name = "base_energy_cost",
    srcs = ["base_energy_cost.py"],
    srcs_version = "PY3",
    deps = [
        "//third_party/py/absl/logging",
        "//third_party/py/pandas",
    ],
)

pytype_strict_library(
    name = "base_occupancy",
    srcs = ["base_occupancy.py"],
    srcs_version = "PY3",
    deps = [
        "//third_party/py/pandas",
    ],
)

pytype_strict_library(
    name = "base_normalizer",
    srcs = ["base_normalizer.py"],
    srcs_version = "PY3",
    deps = [
        "//third_party/py/numpy",
        "//third_party/py/smart_buildings/smart_control/proto:smart_control_building_py_pb2",
        "//third_party/py/tf_agents/specs",
    ],
)

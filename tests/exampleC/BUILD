# Copyright 2017 GRAIL, Inc.
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

load("@com_grail_rules_r//R:defs.bzl", "r_package_with_test")

package(default_visibility = ["//visibility:public"])

PKG_NAME = "exampleC"

PKG_SRCS = glob(
    ["**"],
    exclude = [
        "BUILD",
    ],
)

PKG_DEPS = [
    "//exampleB",
]

PKG_CHECK_DEPS = [
    "@R_RProtoBuf//:RProtoBuf",
    "@R_testthat//:testthat",
]

r_package_with_test(PKG_NAME, PKG_SRCS, PKG_DEPS, PKG_CHECK_DEPS)

load("//tools:apollo_package.bzl", "apollo_cc_library", "apollo_cc_binary", "apollo_package", "apollo_component")
load("//tools:cpplint.bzl", "cpplint")

package(default_visibility = ["//visibility:public"])

filegroup(
    name = "sample_component_files",
    srcs = glob([
        "dag/**",
        "launch/**",
        "conf/**",
    ]),
)

apollo_component(
    name = "libsample_component_component.so",
    srcs = [
        "sample_component_component.cc",
    ],
    hdrs = [
        "sample_component_component.h",
    ],
    linkstatic = True,
    deps = [
        "//cyber",
        "//sample_component/proto:sample_component_proto",

    ],
)

apollo_package()

cpplint()
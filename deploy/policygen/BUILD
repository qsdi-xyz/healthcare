load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library")

licenses(["notice"])  # Apache 2.0

go_library(
    name = "go_default_library",
    srcs = [
        "config.go",
        "main.go",
    ],
    data = [
        "//policygen/templates",
    ],
    importpath = "github.com/GoogleCloudPlatform/healthcare/deploy/policygen",
    visibility = ["//visibility:private"],
    deps = [
        "//config:go_default_library",
        "//policygen/terraform:go_default_library",
        "//runner:go_default_library",
        "//template:go_default_library",
        "@in_ghodss_yaml//:go_default_library",
    ],
)

go_binary(
    name = "policygen",
    embed = [":go_default_library"],
    visibility = ["//visibility:public"],
)

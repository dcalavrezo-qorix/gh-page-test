load("@dash_license_checker//:dash.bzl", "dash_license_checker")
load("//:project_config.bzl", "PROJECT_CONFIG")


filegroup(
    name = "requirements_lock",
    srcs = ["requirements_lock.txt"],
    visibility = ["//visibility:private"],
)

dash_license_checker(
    visibility = ["//visibility:public"],
    src = "//:requirements_lock",
    project_config = PROJECT_CONFIG,
)
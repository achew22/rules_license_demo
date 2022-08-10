load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library")

# gazelle:prefix github.com/achew22/rules_license_demo
# gazelle:go_naming_convention import

package(default_applicable_licenses = [":license"])

load("@rules_license//rules:license.bzl", "license")

license(
    name = "license",
    license_kinds = [],
    package_url = "https://github.com/bazelbuild/bazel-gazelle",
    package_version = "v0.31.0",
)

load("@rules_license//rules:compliance.bzl", "licenses_used")

licenses_used(
    name = "licenses_used",
    deps = ["//:rules_license_demo"],
)

go_binary(
    name = "rules_license_demo",
    embed = [":rules_license_demo_lib"],
    visibility = ["//visibility:public"],
)

go_library(
    name = "rules_license_demo_lib",
    srcs = ["main.go"],
    importpath = "github.com/achew22/rules_license_demo",
    visibility = ["//visibility:private"],
)

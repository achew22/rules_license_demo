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
    deps = ["//:test"],
)

go_library(
    name = "test_lib",
    srcs = ["main.go"],
    importpath = "github.com/achew22/test",
    visibility = ["//visibility:private"],
)

go_binary(
    name = "test",
    embed = [":test_lib"],
    visibility = ["//visibility:public"],
)

# deps
#       "@com_github_golang_protobuf//jsonpb:go_default_library_gen",
#       "@org_golang_google_grpc//:go_default_library",
#       "@org_golang_google_grpc//reflection:go_default_library",
load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library")

go_binary(
    name = "go-server",
    embed = [":go_default_library"],
    visibility = ["//visibility:public"],
)

go_library(
    name = "go_default_library",
    srcs = ["server.go"],
    importpath = "bootcamp/go/cmd/server",
    visibility = ["//visibility:private"],
    deps = [
        "//proto/logger:go_default_library",
        "@com_github_golang_protobuf//jsonpb:go_default_library_gen",
        "@org_golang_google_grpc//:go_default_library",
        "@org_golang_google_grpc//reflection:go_default_library",
    ],
)

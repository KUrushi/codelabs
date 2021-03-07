# load("@rules_java//java:defs.bzl", "java_binary", "java_library", "java_test")

# deps you may need for various targets
#    "@io_grpc_grpc_java//core",
#    "@io_grpc_grpc_java//netty",
#    "@junit_junit//jar" - optional

load("@rules_java//java:defs.bzl", "java_binary", "java_library", "java_test")

java_binary(
    name = "HelloBazelBootcamp",
    srcs = [
        "HelloBazelBootCamp.java",
    ],
)

java_library(
    name = "JavaLoggingClientLibrary",
    srcs = ["JavaLoggingClientLibrary.java"],
    deps = [
        "//proto/logger:logger_java_grpc",
        "//proto/logger:logger_java_proto",
        "@io_grpc_grpc_java//core",
        "@io_grpc_grpc_java//netty",
    ],
)

java_binary(
    name = "JavaLoggingClient",
    srcs = ["JavaLoggingClient.java"],
    main_class = "bazel.bootcamp.JavaLoggingClient",
    visibility = ["//visibility:public"],
    deps = [
        ":JavaLoggingClientLibrary",
    ],
)

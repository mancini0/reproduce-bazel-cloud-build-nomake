workspace(name="nomake")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

all_content = """filegroup(name = "all", srcs = glob(["**"]), visibility = ["//visibility:public"])"""


http_archive(
    name = "kafka",
    build_file_content = all_content,
    strip_prefix = "librdkafka-1.2.1",
    urls = [
        "https://github.com/edenhill/librdkafka/archive/v1.2.1.tar.gz",
    ],
)


http_archive(
    name = "rules_foreign_cc",
    strip_prefix = "rules_foreign_cc-master",
    url = "https://github.com/bazelbuild/rules_foreign_cc/archive/master.zip",
)

http_archive(
    name = "cmake",
    build_file_content = all_content,
    strip_prefix = "CMake-3.12.1",
    urls = [
        "https://github.com/Kitware/CMake/archive/v3.12.1.tar.gz",
    ],
)

load("@rules_foreign_cc//:workspace_definitions.bzl", "rules_foreign_cc_dependencies")

rules_foreign_cc_dependencies(["//:built_cmake_toolchain"])


http_archive(
    name = "kafka",
    build_file_content = all_content,
    #sha256 = "123b47404c16bcde194b4bd1221c21fdce832ad12912bd8074f88f64b2b86f2b",
    strip_prefix = "librdkafka-1.2.1",
    urls = [
        "https://github.com/edenhill/librdkafka/archive/v1.2.1.tar.gz",
    ],
)

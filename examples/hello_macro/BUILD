package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_rust//rust:rust.bzl",
    "rust_doc",
    "rust_doc_test",
    "rust_library",
    "rust_test",
)

rust_library(
    name = "hello_macro",
    srcs = [
        "src/lib.rs",
    ],
    crate_type = "proc-macro",
)

rust_test(
    name = "hello_macro_test",
    crate = ":hello_macro",
)

rust_test(
    name = "greeting_test",
    srcs = ["tests/greeting.rs"],
    proc_macro_deps = [":hello_macro"],
)

rust_doc(
    name = "hello_macro_doc",
    dep = ":hello_macro",
)

rust_doc_test(
    name = "hello_macro_doc_test",
    dep = ":hello_macro",
)

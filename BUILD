filegroup(
    name = "harpoon",
    srcs = ["docker/harpoon", "docker/harpoon.yml"],
    visibility = ["//visibility:public"],
)

sh_test(
    name = "one_test",
    args = ["make", "one"],
    srcs = ["docker/harpoon"],
    data = ["//:harpoon", "//one:example"],
    size = "enormous",
)

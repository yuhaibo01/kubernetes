package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "csi_volume_predicate.go",
        "error.go",
        "metadata.go",
        "predicates.go",
        "testing_helper.go",
        "utils.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/scheduler/algorithm/predicates",
    deps = [
        "//pkg/apis/core/v1/helper:go_default_library",
        "//pkg/apis/core/v1/helper/qos:go_default_library",
        "//pkg/features:go_default_library",
        "//pkg/kubelet/apis:go_default_library",
        "//pkg/scheduler/algorithm:go_default_library",
        "//pkg/scheduler/algorithm/priorities/util:go_default_library",
        "//pkg/scheduler/api:go_default_library",
        "//pkg/scheduler/nodeinfo:go_default_library",
        "//pkg/scheduler/util:go_default_library",
        "//pkg/scheduler/volumebinder:go_default_library",
        "//pkg/volume/util:go_default_library",
        "//staging/src/k8s.io/api/core/v1:go_default_library",
        "//staging/src/k8s.io/api/storage/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/fields:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/labels:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/rand:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/sets:go_default_library",
        "//staging/src/k8s.io/apiserver/pkg/util/feature:go_default_library",
        "//staging/src/k8s.io/client-go/listers/core/v1:go_default_library",
        "//staging/src/k8s.io/client-go/listers/storage/v1:go_default_library",
        "//staging/src/k8s.io/client-go/util/workqueue:go_default_library",
        "//vendor/k8s.io/klog:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "csi_volume_predicate_test.go",
        "max_attachable_volume_predicate_test.go",
        "metadata_test.go",
        "predicates_test.go",
        "utils_test.go",
    ],
    embed = [":go_default_library"],
    deps = [
        "//pkg/apis/core/v1/helper:go_default_library",
        "//pkg/features:go_default_library",
        "//pkg/kubelet/apis:go_default_library",
        "//pkg/scheduler/algorithm:go_default_library",
        "//pkg/scheduler/api:go_default_library",
        "//pkg/scheduler/nodeinfo:go_default_library",
        "//pkg/scheduler/testing:go_default_library",
        "//pkg/volume/util:go_default_library",
        "//staging/src/k8s.io/api/core/v1:go_default_library",
        "//staging/src/k8s.io/api/storage/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/api/resource:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/labels:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/sets:go_default_library",
        "//staging/src/k8s.io/apiserver/pkg/util/feature:go_default_library",
        "//staging/src/k8s.io/apiserver/pkg/util/feature/testing:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)

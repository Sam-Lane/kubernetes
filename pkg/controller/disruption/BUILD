package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = ["disruption.go"],
    importpath = "k8s.io/kubernetes/pkg/controller/disruption",
    deps = [
        "//pkg/api/v1/pod:go_default_library",
        "//pkg/controller:go_default_library",
        "//staging/src/k8s.io/api/apps/v1beta1:go_default_library",
        "//staging/src/k8s.io/api/core/v1:go_default_library",
        "//staging/src/k8s.io/api/extensions/v1beta1:go_default_library",
        "//staging/src/k8s.io/api/policy/v1beta1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/api/equality:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/api/meta:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/runtime/schema:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/types:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/intstr:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/runtime:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//staging/src/k8s.io/client-go/informers/apps/v1:go_default_library",
        "//staging/src/k8s.io/client-go/informers/core/v1:go_default_library",
        "//staging/src/k8s.io/client-go/informers/policy/v1beta1:go_default_library",
        "//staging/src/k8s.io/client-go/kubernetes:go_default_library",
        "//staging/src/k8s.io/client-go/kubernetes/scheme:go_default_library",
        "//staging/src/k8s.io/client-go/kubernetes/typed/core/v1:go_default_library",
        "//staging/src/k8s.io/client-go/listers/apps/v1:go_default_library",
        "//staging/src/k8s.io/client-go/listers/core/v1:go_default_library",
        "//staging/src/k8s.io/client-go/listers/policy/v1beta1:go_default_library",
        "//staging/src/k8s.io/client-go/scale:go_default_library",
        "//staging/src/k8s.io/client-go/tools/cache:go_default_library",
        "//staging/src/k8s.io/client-go/tools/record:go_default_library",
        "//staging/src/k8s.io/client-go/util/workqueue:go_default_library",
        "//vendor/k8s.io/klog/v2:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["disruption_test.go"],
    embed = [":go_default_library"],
    deps = [
        "//pkg/apis/core/install:go_default_library",
        "//pkg/controller:go_default_library",
        "//staging/src/k8s.io/api/apps/v1:go_default_library",
        "//staging/src/k8s.io/api/autoscaling/v1:go_default_library",
        "//staging/src/k8s.io/api/core/v1:go_default_library",
        "//staging/src/k8s.io/api/policy/v1beta1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/api/equality:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/api/meta/testrestmapper:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/runtime/schema:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/types:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/intstr:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/uuid:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//staging/src/k8s.io/client-go/informers:go_default_library",
        "//staging/src/k8s.io/client-go/kubernetes/fake:go_default_library",
        "//staging/src/k8s.io/client-go/scale/fake:go_default_library",
        "//staging/src/k8s.io/client-go/testing:go_default_library",
        "//staging/src/k8s.io/client-go/tools/cache:go_default_library",
        "//staging/src/k8s.io/client-go/util/workqueue:go_default_library",
        "//vendor/k8s.io/klog/v2:go_default_library",
        "//vendor/k8s.io/utils/pointer:go_default_library",
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

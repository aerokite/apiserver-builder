package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "admission.go",
        "doc.go",
    ],
    importpath = "k8s.io/kubernetes/plugin/pkg/admission/persistentvolume/label",
    deps = [
        "//vendor/github.com/golang/glog:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/admission:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/api:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/cloudprovider:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/cloudprovider/providers/aws:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/cloudprovider/providers/gce:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/kubeapiserver/admission:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/kubelet/apis:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/volume:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["admission_test.go"],
    importpath = "k8s.io/kubernetes/plugin/pkg/admission/persistentvolume/label",
    library = ":go_default_library",
    deps = [
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/types:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/admission:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/api:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/cloudprovider/providers/aws:go_default_library",
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

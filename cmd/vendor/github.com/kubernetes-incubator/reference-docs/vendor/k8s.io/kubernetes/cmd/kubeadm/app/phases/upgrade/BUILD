load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "compute.go",
        "configuration.go",
        "health.go",
        "policy.go",
        "postupgrade.go",
        "postupgrade_v17_v18.go",
        "prepull.go",
        "selfhosted.go",
        "staticpods.go",
        "versiongetter.go",
    ],
    importpath = "k8s.io/kubernetes/cmd/kubeadm/app/phases/upgrade",
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/api/extensions/v1beta1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/fields:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/errors:go_default_library",
        "//vendor/k8s.io/client-go/kubernetes:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/apis/kubeadm:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/apis/kubeadm/v1alpha1:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/apis/kubeadm/validation:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/constants:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/images:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/phases/addons/dns:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/phases/addons/proxy:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/phases/apiconfig:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/phases/bootstraptoken/clusterinfo:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/phases/bootstraptoken/node:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/phases/controlplane:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/phases/selfhosting:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/phases/uploadconfig:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/util:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/util/apiclient:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/util/config:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/api:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/bootstrap/api:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/util/version:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/version:go_default_library",
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
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = [
        "compute_test.go",
        "policy_test.go",
        "prepull_test.go",
        "staticpods_test.go",
    ],
    importpath = "k8s.io/kubernetes/cmd/kubeadm/app/phases/upgrade",
    library = ":go_default_library",
    deps = [
        "//vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/apis/kubeadm:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/apis/kubeadm/v1alpha1:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/constants:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/phases/controlplane:go_default_library",
        "//vendor/k8s.io/kubernetes/cmd/kubeadm/app/util/apiclient:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/api:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/util/version:go_default_library",
    ],
)

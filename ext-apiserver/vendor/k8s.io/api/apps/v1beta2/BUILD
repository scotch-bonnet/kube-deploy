load("@io_bazel_rules_go//proto:def.bzl", "go_grpc_library")
load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "generated.pb.go",
        "register.go",
        "types.go",
        "types_swagger_doc_generated.go",
        "zz_generated.deepcopy.go",
    ],
    importpath = "k8s.io/api/apps/v1beta2",
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/github.com/gogo/protobuf/proto:go_default_library",
        "//vendor/github.com/gogo/protobuf/sortkeys:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/conversion:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime/schema:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/intstr:go_default_library",
    ],
)

proto_library(
    name = "v1beta2_proto",
    srcs = ["generated.proto"],
    visibility = ["//visibility:public"],
    deps = [
        "//k8s.io/api/core/v1:v1_proto",
        "//k8s.io/api/policy/v1beta1:v1beta1_proto",
        "//k8s.io/apimachinery/pkg/apis/meta/v1:v1_proto",
        "//k8s.io/apimachinery/pkg/runtime:runtime_proto",
        "//k8s.io/apimachinery/pkg/runtime/schema:schema_proto",
        "//k8s.io/apimachinery/pkg/util/intstr:intstr_proto",
    ],
)

go_grpc_library(
    name = "v1beta2_go_proto",
    importpath = "k8s.io/api/apps/v1beta2",
    proto = ":v1beta2_proto",
    visibility = ["//visibility:public"],
    deps = [
        "//k8s.io/api/core/v1:go_default_library",
        "//k8s.io/api/policy/v1beta1:go_default_library",
        "//k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//k8s.io/apimachinery/pkg/runtime/schema:go_default_library",
        "//k8s.io/apimachinery/pkg/util/intstr:go_default_library",
    ],
)

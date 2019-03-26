load("//tools:cpplint.bzl", "cpplint")

package(default_visibility = ["//visibility:public"])

cc_binary(
    name = "obstacle_detection",
    srcs = [
        "obstacle_detection.cc",
    ],
    linkopts = [
        "-lboost_system",
        "-lopencv_core",
        "-lopencv_imgproc",
        "-lopencv_highgui",
    ],
    deps = [
        "//modules/perception/base",
        "//modules/perception/camera/lib/interface",
        "//modules/perception/camera/lib/obstacle/detector/yolo:yolo_obstacle_detector",
        "//modules/perception/camera/lib/obstacle/transformer/multicue:multicue_obstacle_transformer",
        "//modules/perception/common/io:io_util",
        "//modules/perception/inference/utils:inference_cuda_util_lib",
        "@gtest",
    ],
)

cpplint()

# JNI headers for native code compilation
load("@rules_cc//cc:defs.bzl", "cc_library")

cc_library(
    name = "jni_headers", 
    hdrs = [
        ":jni_h",
        ":jni_md_h",
    ],
    includes = ["."],
    visibility = ["//visibility:public"],
)

genrule(
    name = "jni_h",
    outs = ["jni.h"],
    cmd = "cp /opt/homebrew/opt/openjdk@17/libexec/openjdk.jdk/Contents/Home/include/jni.h $@",
    visibility = ["//visibility:public"],
)

genrule(
    name = "jni_md_h",
    outs = ["jni_md.h"],
    cmd = "cp /opt/homebrew/opt/openjdk@17/libexec/openjdk.jdk/Contents/Home/include/darwin/jni_md.h $@",
    visibility = ["//visibility:public"],
)

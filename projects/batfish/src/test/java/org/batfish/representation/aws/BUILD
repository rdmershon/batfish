load("@batfish//skylark:junit.bzl", "junit_tests")

package(
    default_testonly = True,
    default_visibility = ["//visibility:public"],
)

junit_tests(
    name = "tests",
    srcs = glob([
        "**/*Test*.java",
    ]),
    resources = [
        "//projects/batfish/src/test/resources/org/batfish/representation/aws",
        "//projects/batfish/src/test/resources:log4j_config",
        ],
    runtime_deps = [
        "@maven//:org_mockito_mockito_inline",
        "@maven//:org_apache_logging_log4j_log4j_core",
                "@maven//:org_apache_logging_log4j_log4j_slf4j_impl",
    ],
    deps = [
        "//projects/batfish",
        "//projects/batfish:batfish_testlib",
        "//projects/batfish-common-protocol:common",
        "//projects/batfish-common-protocol/src/test/java/org/batfish/datamodel/matchers",
        "//projects/batfish/src/main/java/org/batfish/representation/aws",
        "@maven//:com_fasterxml_jackson_core_jackson_core",
        "@maven//:com_fasterxml_jackson_core_jackson_databind",
        "@maven//:com_google_guava_guava",
        "@maven//:com_google_guava_guava_testlib",
        "@maven//:junit_junit",
        "@maven//:org_hamcrest_hamcrest",
        "@maven//:org_mockito_mockito_core",
    ],
)

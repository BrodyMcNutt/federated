package(default_visibility = ["//tensorflow_federated/python/research"])

licenses(["notice"])

py_library(
    name = "metrics_hook",
    srcs = ["metrics_hook.py"],
    srcs_version = "PY3",
    deps = [
        "//tensorflow_federated",
        "//tensorflow_federated/python/research/utils:utils_impl",
        "//tensorflow_federated/python/tensorflow_libs:nest",
    ],
)

py_library(
    name = "models",
    srcs = ["models.py"],
    srcs_version = "PY3",
)

py_test(
    name = "models_test",
    srcs = ["models_test.py"],
    python_version = "PY3",
    srcs_version = "PY3",
    deps = [":models"],
)

py_binary(
    name = "run_dp_experiment",
    srcs = ["run_dp_experiment.py"],
    python_version = "PY3",
    srcs_version = "PY3",
    deps = [
        ":metrics_hook",
        ":models",
        "//tensorflow_federated",
        "//tensorflow_federated/python/research/utils:training_loops",
        "//tensorflow_federated/python/research/utils:utils_impl",
    ],
)

py_binary(
    name = "run_experiment",
    srcs = ["run_experiment.py"],
    python_version = "PY3",
    srcs_version = "PY3",
    deps = [
        ":metrics_hook",
        ":models",
        "//tensorflow_federated",
        "//tensorflow_federated/python/research/utils:training_loops",
        "//tensorflow_federated/python/research/utils:utils_impl",
        "//tensorflow_federated/python/tensorflow_libs:nest",
    ],
)

py_binary(
    name = "non_federated_emnist_10",
    srcs = ["non_federated_emnist_10.py"],
    python_version = "PY3",
    srcs_version = "PY3",
    deps = [
        ":models",
        "//tensorflow_federated",
    ],
)

py_binary(
    name = "non_federated_emnist_62",
    srcs = ["non_federated_emnist_62.py"],
    python_version = "PY3",
    srcs_version = "PY3",
    deps = [
        ":models",
        "//tensorflow_federated",
    ],
)

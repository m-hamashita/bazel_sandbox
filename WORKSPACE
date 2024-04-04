load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

RULES_PYTHON_VERSION = "0.31.0"

RULES_PYTHON_DIGEST = "c68bdc4fbec25de5b5493b8819cfc877c4ea299c0dcb15c244c5a00208cde311"

http_archive(
    name = "rules_python",
    sha256 = RULES_PYTHON_DIGEST,
    strip_prefix = "rules_python-" + RULES_PYTHON_VERSION,
    urls = [
        "https://github.com/bazelbuild/rules_python/releases/download/" + RULES_PYTHON_VERSION + "/rules_python-" + RULES_PYTHON_VERSION + ".tar.gz",
    ],
)

load(
    "@rules_python//python:repositories.bzl",
    "py_repositories",
    "python_register_toolchains",
)

py_repositories()

python_register_toolchains(
    name = "python3",
    # Available versions are listed in @rules_python//python:versions.bzl.
    python_version = "3.10.12",
)

package(default_visibility = ["//visibility:public"])

# Note: The genrule targets rename the scripts to .py generated files.
# Note: subpar does not yet support C extensions.

genrule(
    name = "bean_check_py",
    srcs = ["bean-check"],
    outs = ["bean_check.py"],
    cmd = "cat $(locations :bean-check) > $@",
)

py_binary(
    name = "bean_check",
    srcs = ["bean_check.py"],
    deps = [
        "//beancount/scripts:check",
        "//beancount:loader_with_plugins",
    ],
)

genrule(
    name = "bean_doctor_py",
    srcs = ["bean-doctor"],
    outs = ["bean_doctor.py"],
    cmd = "cat $(locations :bean-doctor) > $@",
)

py_binary(
    name = "bean_doctor",
    srcs = ["bean_doctor.py"],
    deps = [
        "//beancount/scripts:doctor",
        "//beancount:loader_with_plugins",
    ],
)

genrule(
    name = "bean_example_py",
    srcs = ["bean-example"],
    outs = ["bean_example.py"],
    cmd = "cat $(locations :bean-example) > $@",
)

py_binary(
    name = "bean_example",
    srcs = ["bean_example.py"],
    deps = [
        "//beancount/scripts:example",
        "//beancount:loader_with_plugins",
    ],
)

genrule(
    name = "bean_format_py",
    srcs = ["bean-format"],
    outs = ["bean_format.py"],
    cmd = "cat $(locations :bean-format) > $@",
)

py_binary(
    name = "bean_format",
    srcs = ["bean_format.py"],
    deps = [
        "//beancount/scripts:format",
    ],
)

genrule(
    name = "bean_query_py",
    srcs = ["bean-query"],
    outs = ["bean_query.py"],
    cmd = "cat $(locations :bean-query) > $@",
)

py_binary(
    name = "bean_query",
    srcs = ["bean_query.py"],
    deps = [
        "//beancount/query:shell",
        "//beancount:loader_with_plugins",
    ],
)

genrule(
    name = "bean_sql_py",
    srcs = ["bean-sql"],
    outs = ["bean_sql.py"],
    cmd = "cat $(locations :bean-sql) > $@",
)

py_binary(
    name = "bean_sql",
    srcs = ["bean_sql.py"],
    deps = [
        "//beancount/scripts:sql",
        "//beancount:loader_with_plugins",
    ],
)

genrule(
    name = "treeify_py",
    srcs = ["treeify"],
    outs = ["bean_treeify.py"],
    cmd = "cat $(locations :treeify) > $@",
)

py_binary(
    name = "bean_treeify",
    srcs = ["bean_treeify.py"],
    deps = [
        "//beancount/tools:treeify",
    ],
)

genrule(
    name = "upload_to_sheets_py",
    srcs = ["upload-to-sheets"],
    outs = ["upload_to_sheets.py"],
    cmd = "cat $(locations :upload-to-sheets) > $@",
)

py_binary(
    name = "upload_to_sheets",
    srcs = ["upload_to_sheets.py"],
    deps = [
        "//beancount/tools:sheets_upload",
        "//beancount:loader_with_plugins",
    ],
)

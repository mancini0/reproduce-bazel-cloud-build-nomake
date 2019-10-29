Build kafka using rules_foreign_cc's cmake_external rule.

Locally (ubuntu 18.04), run bazel build //...

(on Fedora, you might need to uncomment the <code>out_lib_dir = "lib64" </code> line in the //kafka cmake_external rule.)

It should build fine locally.


On google cloud build, you will get the following error:



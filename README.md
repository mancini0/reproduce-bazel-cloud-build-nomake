This repo builds kafka using rules_foreign_cc's cmake_external rule, with cmake built as part of the build process.

It works fine when built locally, but does not build on Google's Cloud Build, it fails with the following error:

<code>
CMake 3.12.1, Copyright 2000-2018 Kitware, Inc. and Contributors
Found GNU toolchain
C compiler on this system is: gcc
C++ compiler on this system is: g++ -std=gnu++17
Error when bootstrapping CMake:
Cannot find appropriate Makefile processor on this system.
Please specify one using environment variable MAKE.
</code>
<h3>instructions to build locally</h3>

(ubuntu 18.04), run bazel build //...

(on Fedora, you might need to uncomment the <code>out_lib_dir = "lib64" </code> line in the //kafka cmake_external rule.)

It should build fine locally.

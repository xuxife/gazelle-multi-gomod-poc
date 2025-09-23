# POC for patching gazelle to support multiple go.mod in one bazel workspace

did some hack in gazelle, then
https://github.com/bazel-contrib/bazel-gazelle/compare/master...xuxife:bazel-gazelle:master

```
❯ bazelisk run //main
INFO: Analyzed target //main:main (9 packages loaded, 10969 targets configured).
INFO: Found 1 target...
Target //main:main up-to-date:
  bazel-bin/main/main_/main
INFO: Elapsed time: 4.976s, Critical Path: 0.86s
INFO: 5 processes: 2 internal, 3 darwin-sandbox.
INFO: Build completed successfully, 5 total actions
INFO: Running command line: bazel-bin/main/main_/main
v0.0.1

❯ bazelisk run //main2
INFO: Analyzed target //main2:main2 (35 packages loaded, 325 targets configured).
INFO: Found 1 target...
Target //main2:main2 up-to-date:
  bazel-bin/main2/main2_/main2
INFO: Elapsed time: 2.776s, Critical Path: 0.35s
INFO: 5 processes: 2 internal, 3 darwin-sandbox.
INFO: Build completed successfully, 5 total actions
INFO: Running command line: bazel-bin/main2/main2_/main2
v0.0.2
```
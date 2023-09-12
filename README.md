Example: Bazel with bzlmod & pip extensions

Loosely based on github.com/bazelbuild/rules_python/examples/bzlmod

I am trying first with a 3.9 target. Next, I'll try mixed 3.9, 3.10, 3.11, etc.

```
make this work with coverage by adding this to
python.toolchain() configure_coverage_tool = True

bazel coverage //:test

❯ genhtml --output genhtml /home/jwattenb/.cache/bazel/_bazel_jwattenb/027271961879245cbafd9351c8545dbd/execroot/_main/bazel-out/k8-fastbuild/testlogs/test/coverage.dat
Reading data file /home/jwattenb/.cache/bazel/_bazel_jwattenb/027271961879245cbafd9351c8545dbd/execroot/_main/bazel-out/k8-fastbuild/testlogs/test/coverage.dat
Resolved relative source file path "lib.py" with CWD to "/home/jwattenb/git/github.com/jjwatt/play-bzlmod/lib.py".
Found 1 entries.
Found common filename prefix "/home/jwattenb/git/github.com/jjwatt"
Writing .css and .png files.
Generating output.
Processing file play-bzlmod/lib.py
Writing directory view page.
Overall coverage rate:
  lines......: 100.0% (3 of 3 lines)
  functions..: no data found
```

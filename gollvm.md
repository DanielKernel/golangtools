一、gollvm可以构建成功的commits：

gollvm commit:  0e34e09fc15cde73f1b9974f2a657360abb94b4f
libbacktrace commit:  2446c66076480ce07a6bd868badcbceb3eeecc2e
libffi commit:  ab1677106605aba1c27665964ff90bea59612ce3
gofrontend commit 7f33baa09a8172bb2c5f1ca0435d9efe3e194c9b
llvm-project commit 09629215c272f09e3ebde6cc7eac9625d28910ff

参考链接：https://groups.google.com/g/golang-nuts/c/sTh5tpz7ork/m/yQWQTX1zAAAJ

需要执行以下命令获取对应的commit快照代码
`git checkout commit-ID`

二、针对MacOS，需要确保SHELL环境变量指向 `/usr/bin/bash`
参考：https://github.com/golang/go/issues/36554
否则会有类似错误
`/Users/daniel/llvmProjects/llvm-project/llvm/tools/gollvm/gofrontend/libgo/match.sh:162: no such file or directory:  callee.go imports.go map.go methodsetcache.go ui.go
/Users/daniel/llvmProjects/llvm-project/llvm/tools/gollvm/gofrontend/libgo/match.sh:172: no such file or directory:  callee.go imports.go map.go methodsetcache.go ui.go
/Users/daniel/llvmProjects/llvm-project/llvm/tools/gollvm/gofrontend/libgo/match.sh:162: no such file or directory:  analysis.go
/Users/daniel/llvmProjects/llvm-project/llvm/tools/gollvm/gofrontend/libgo/match.sh:172: no such file or directory:  analysis.go
/Users/daniel/llvmProjects/llvm-project/llvm/tools/gollvm/gofrontend/libgo/match.sh:162: no such file or directory:  input.go matcher.go symbol.go
/Users/daniel/llvmProjects/llvm-project/llvm/tools/gollvm/gofrontend/libgo/match.sh:172: no such file or directory:  input.go matcher.go symbol.go
/Users/daniel/llvmProjects/llvm-project/llvm/tools/gollvm/gofrontend/libgo/match.sh:162: no such file or directory:  common.go enabled_go117.go enabled_go118.go normalize.go termlist.go typeparams_go117.go typeparams_go118.go typeterm.go`

三、MACOS的目标系统市x86，不是x86_64
cmake中增加`-DLLVM_TARGETS_TO_BUILD=X86`

四、macos上编译LLVM
mkdir build-llvm
cd build-llvm
cmake -G "Ninja" -DCMAKE_BUILD_TYPE=Debug -DLLVM_TARGETS_TO_BUILD=X86 -DLLVM_ENABLE_CXX1Y=ON -DLLVM_ENABLE_ASSERTIONS=ON -DSPHINX_OUTPUT_HTML=OFF -DSPHINX_OUTPUT_MAN=OFF ../llvm-project/llvm
cmake --build

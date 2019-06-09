# golang tools清单
go-outline
go-symbols
gocode
godef
gogetdoc
golint
gomodifytags
goreturns
gotests
impl
goplay
gopkgs
fillstruct
gometalinter

godoc
gorename
goimports
guru

# 下载golang tools

```shell
cd $GOPATH/src
mkdir github.com

cd $GOPATH/src/github.com
mkdir ramya-rao-a
cd $GOPATH/src/github.com/ramya-rao-a
git clone https://github.com/ramya-rao-a/go-outline

cd $GOPATH/src/github.com
mkdir acroca
cd $GOPATH/src/github.com/acroca
git clone https://github.com/acroca/go-symbols

cd $GOPATH/src/github.com
mkdir mdempsky
cd $GOPATH/src/github.com/mdempsky
git clone https://github.com/mdempsky/gocode

cd $GOPATH/src/github.com
mkdir rogpeppe
cd $GOPATH/src/github.com/rogpeppe
git clone https://github.com/rogpeppe/godef

cd $GOPATH/src/github.com
mkdir zmb3
cd $GOPATH/src/github.com/zmb3
git clone https://github.com/zmb3/gogetdoc

cd $GOPATH/src/github.com
mkdir fatih
cd $GOPATH/src/github.com/fatih
git clone https://github.com/fatih/gomodifytags

cd $GOPATH/src/github.com
mkdir sqs
cd $GOPATH/src/github.com/sqs
git clone https://github.com/sqs/goreturns.git

cd $GOPATH/src/github.com
mkdir cweill
cd $GOPATH/src/github.com/cweill
git clone https://github.com/cweill/gotests.git

cd $GOPATH/src/github.com
mkdir josharian
cd $GOPATH/src/github.com/josharian
git clone https://github.com/josharian/impl

cd $GOPATH/src/github.com
mkdir skratchdot
cd $GOPATH/src/github.com/skratchdot
git clone https://github.com/skratchdot/open-golang.git

cd $GOPATH/src/github.com
mkdir haya14busa
cd $GOPATH/src/github.com/haya14busa
git clone https://github.com/haya14busa/goplay.git

cd $GOPATH/src/github.com
mkdir karrick
cd $GOPATH/src/github.com/karrick
git clone https://github.com/karrick/godirwalk.git
cd $GOPATH/src/github.com
mkdir pkg
cd $GOPATH/src/github.com/pkg
git clone https://github.com/pkg/errors.git

cd $GOPATH/src/github.com
mkdir uudashr
cd $GOPATH/src/github.com/uudashr
git clone https://github.com/uudashr/gopkgs.git

cd $GOPATH/src/github.com
mkdir davidrjenni
cd $GOPATH/src/github.com/davidrjenni
git clone https://github.com/davidrjenni/reftools.git

cd $GOPATH/src/github.com
mkdir alecthomas
cd $GOPATH/src/github.com/alecthomas
git clone https://github.com/alecthomas/gometalinter

cd $GOPATH/src/github.com
mkdir go-delve
cd $GOPATH/src/github.com/go-delve
git clone https://github.com/go-delve/delve.git

cd $GOPATH/src
mkdir golang.org
cd $GOPATH/src/golang.org
mkdir $GOPATH/src/golang.org/x
cd $GOPATH/src/golang.org/x
mkdir $GOPATH/src/golang.org/x/tools
cd $GOPATH/src/golang.org/x/tools
git clone https://github.com/golang/tools.git

cd $GOPATH/src/golang.org/x
git clone https://github.com/golang/lint.git
cd $GOPATH/src/golang.org/x
git clone https://github.com/golang/net.git

```

# 安装golang tools
```shell

cd $GOPATH/src
go install github.com/ramya-rao-a/go-outline
go install github.com/acroca/go-symbols
go install github.com/mdempsky/gocode
go install github.com/rogpeppe/godef
go install github.com/zmb3/gogetdoc
go install github.com/fatih/gomodifytags
go install github.com/sqs/goreturns
go install github.com/cweill/gotests
go install github.com/josharian/impl
go install github.com/haya14busa/goplay/cmd/goplay
go install github.com/uudashr/gopkgs/cmd/gopkgs
go install github.com/davidrjenni/reftools/cmd/fillstruct
go install github.com/alecthomas/gometalinter
go install github.com/go-delve/delve/cmd/dlv

cd $GOPATH/src
go install golang.org/x/tools/cmd/godoc
go install golang.org/x/tools/cmd/gorename
go install golang.org/x/tools/cmd/goimports
go install golang.org/x/tools/cmd/guru
go install golang.org/x/lint/golint

```

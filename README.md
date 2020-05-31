# Creating Go CLI Application using Cobra  

###### Pre-requisites before getting started :-

1. You must have Golang Installed on your device. `https://golang.org/doc/install` follow this link to download and use `go version` command to check for the installed version (I'm using go version go1.14.3 darwin/amd64)
2. Cobra Library - which is a CLI library for Go that empowers applications.
Get it using `go get -u github.com/spf13/cobra/cobra`. And to include cobra in your project use `import "github.com/spf13/cobra"`

3. Code Editor 

###### Basic Command Structure in Cobra
`APPNAME COMMAND ARG --FLAG`


###### Setting up GOROOT and GOPATH
1. GOROOT is a variable that defines where your Go SDK is located. Generally `/usr/local/go`
2. GOPATH is a variable that defines the root of your workspace. GOPATH stores your code base and all the files that are necessary for your development. You can use another directory as your workspace by configuring GOPATH for different scopes. It contains following folders
    `src/`: location of Go source code (for example, .go, .c, .g, .s).
    `pkg/`: location of compiled package code (for example, .a).
    `bin/`: location of compiled executable programs built by Go.

GOPATH can have more than one values. Setting up GOPATH in .bash_profile
```sh
export GOROOT="/usr/local/go"
export PATH="$GOROOT/bin:$PATH"
export GOPATH="/Users/mohitdtumce/Documents/learn_go/golib"
export PATH="$GOPATH/bin:$PATH"
export GOPATH="$GOPATH:/Users/mohitdtumce/Documents/learn_go/basic_cobra"
```

As you'll notice, I've provided two paths in GOPATH - one for libraries and another for code development.

###### Setting up project
- Module - A module is a collection of Go packages stored in a file tree with a go.mod file at its root. The go.mod file defines the module’s module path, which is also the import path used for the root directory, and its dependency requirements, which are the other modules needed for a successful build.
```sh
cd ~/Documents/learn_go/basic_cobra
go mod init basic_cobra
```
Add Cobra library in the project :-
```sh
go get -u github.com/spf13/cobra/cobra
cobra init --pkg-name=basic_cobra
```
main.go is the starting point of the application. Use `go run main.go` command to run the program.
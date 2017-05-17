# Simple proxy by Golang
## How to build:
1. Download golang: https://golang.org/dl/
2. Extract to /usr/local (ex: tar -C /usr/local -xzf go$VERSION.$OS-$ARCH.tar.gz)
3. Export GOROOT, GOPATH environment variables

Example:
```
export GOROOT=/usr/local/go
export PATH=$PATH:$GOROOT/bin
export GOPATH=$HOME/go
```
Or you can create a file go.sh with above content and push in /etc/profile.d directory

4. Download library: cd $HOME/go/src/github.com
```
$ go get github.com/gonuts/commander
$ go get github.com/gonuts/flag
```
5. Change to your workspace of project
```
go build
```
6. Execute:
```
./proxyService http -bind :4000 remotehost:4001
./proxyService https -bind :4000 -cert ssl.crt -key ssl.key remotehost:4001
```

## Get and Run binary
1. Download balance binary file
2. Execute:
```
./proxyService http -bind :4000 remotehost:4001
./proxyService https -bind :4000 -cert ssl.crt -key ssl.key remotehost:4001
```

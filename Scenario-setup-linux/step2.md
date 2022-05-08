Kubernetes is written in Go. Building and developing Kubernetes requires a very recent version of Go. [This table](https://github.com/kubernetes/community/blob/master/contributors/devel/development.md#go) lists the required Go versions for different versions of Kubernetes. 

### Installing Go

Let us start by updating the packages:
`sudo apt-get update`{{execute}}

First we download the tarball archive of the go compiler.
`wget https://go.dev/dl/go1.18.1.linux-amd64.tar.gz`{{execute}} 

Also, remove any previous installations of Go, if present.

`sudo rm -rf /usr/local/go`{{execute}}

The next step is to extract the contents of the archive. We can use the command as:

`sudo tar -C /usr/local -xzf go1.18.1.linux-amd64.tar.gz`{{execute}} 


The command above should extract the archive and create a directory called to go.

The next step is to set the path for go. This allows the go executable to be accessible outside the main go directory or without an absolute path.

Finally, verify that go is installed successfully by running the command:

`go version`{{execute}}

The command should return the installed go version as:

`go version go1.18.1 linux/amd64`

🎉 YAY! Go has been successfully installed.

### Installing make (Ubuntu/Debian)

The `build-essential` package is required for the `make` utility. 

`sudo apt-get install build-essential`{{execute}}
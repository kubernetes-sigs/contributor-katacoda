### 2. Install basic tools

Kubernetes is written in Go. Building and developing Kubernetes requires a very recent version of Go.[This table](https://github.com/kubernetes/community/blob/master/contributors/devel/development.md#go) lists the required Go versions for different versions of Kubernetes. <br /> 
**Installing GO**<br /> 
`sudo curl -O https://storage.googleapis.com/golang/go1.17.linux-amd64.tar.gz`{{execute}} <br /> 

`sudo tar -xvf go1.17.linux-amd64.tar.gz`{{execute}} <br /> 
`sudo rm -rf /usr/local/go`{{execute}}<br /> 
`sudo mv go /usr/local`{{execute}}<br /> 

**Installing make (Ubuntu/Debian)** <br /> 
`sudo apt-get install build-essential`{{execute}}
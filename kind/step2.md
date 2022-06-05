A fully functioning environment using kind includes a few different components. For our purposes, we will install the following list of software.

1. Docker.
2. The kubectl tool.
3. kind.

## Docker

The kind project stands for “Kubernetes in Docker”. As such, you will need to install Docker to get started. This is typically environment specific, and you may need to consult the Docker documentation if you get stuck. The following should get you started:

Older versions of Docker were called docker, docker.io, or docker-engine. If these are installed you should start by getting rid of them:

 `sudo apt-get remove docker docker-engine docker.io containerd runc`{{execute}}

Once done, you can add the Docker apt repository to support future installations over apt. To do so, we need to first install packages necessary for installing from apt over HTTPS.

` sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common`{{execute}}

Then, we can add the Docker apt repository by adding Docker’s GPG key and followed by adding the apt repository.

`curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
 sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"`{{execute}}

Lastly, Update the apt package index:

`sudo apt-get update`{{execute}}

Install the latest version of Docker CE and containerd:

`sudo apt-get install docker-ce docker-ce-cli containerd.io`{{execute}}

## Kubectl

kind does not strictly require kubectl, but because we are aiming to setup a fully functioning development environment we are going to install kubectl to be able to do some basic Kubernetes functions on our cluster.

If you get stuck at any point, refer to the official [kubectl installation instructions](https://kubernetes.io/docs/tasks/tools/).

Linux users can fetch kubectl through the Google apt repository:
`curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee -a /etc/apt/sources.list.d/kubernetes.list
sudo apt-get update
sudo apt-get install -y kubectl`{{execute}}

## kind

Now we can finally install kind. Kind publishes binaries to Github. These can be installed by downloading the release for Linux distributions.

`curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.14.0/kind-linux-amd64
 chmod +x ./kind
 mv ./kind /usr/local/bin`{{execute}}

🎉 YAY! All the dependencies have been successfully installed.

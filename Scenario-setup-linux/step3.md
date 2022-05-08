Cloning a GitHub repository creates a local copy of the remote repo. When we clone a repository, all the files are downloaded to the local machine but the remote git repository remains unchanged.

This allows you to make all of your edits locally rather than directly in the source files of the origin repo.
 To clone a repository we can use `git clone` command

 Here's the command to clone kubernetes repository.

 `git clone https://github.com/kubernetes/kubernetes `{{execute}}

 NOTE :- Kubernetes is a large project, and compiling it can use a lot of resources. We recommend the following hardware recommendation for any physical or virtual machine being used for building Kubernetes.

   * 8GB of RAM
   * 50GB of free disk space

  when you clone the repository on your local machine, it is expected to take around 40 mins to complete the operation with the above-mentioned hardware specifications.


`git clone` will clone the entire commit history of the Kubernetes project onto your local system and can sometimes take significantly long periods of time. In case you have network/hardware constraints, the `--depth` flag can be used in order to create a "shallow" clone of the project.

You can use the following command to create a shallow clone.

`git clone https://github.com/kubernetes/kubernetes --depth 1`

after cloning change the directory
`cd kubernetes`{{execute}}
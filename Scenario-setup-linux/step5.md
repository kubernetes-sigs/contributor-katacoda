Kubernetes is a large project, so the configuration of your development environment must ensure that all unit, integration, and end-to-end tests run successfully because Kubernetes only merges pull requests when they pass the unit, integration, and end-to-end tests.
Although this quick start will get you started, to learn about the testing infrastructure in depth, read the [Testing Guide](https://github.com/kubernetes/community/blob/master/contributors/devel/sig-testing/testing.md) and examine the [SIG Architecture developer guide](https://github.com/kubernetes/community/blob/master/contributors/devel/README.md#sig-testing) material.

## make commands in kubernetes:-
  make command is used to build and maintain groups of programs and files from the source code. In kubernetes also we use some make commands. Some of which are as follows:-

  ### make test
   `make test` is the entrypoint for running the unit tests.
 This command tests various parts of  code base to ensure the correctness of the functionality. 
 It uses the test framework built in  code base to perform hundreds of tests. It does take a fair bit of time to execute all the tests. If all the tests are successful, ALL OK is issued.
basically make test  Run all unit tests.

  ### make help
  In Kubernetes, there are a number of other commands we can use to simplify our testing
  process. We can use the make help command to get a list of all the commands available
  `make help`{{execute}} Prints make targets and help information.

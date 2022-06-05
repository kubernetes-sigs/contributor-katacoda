To understand how kind works in a local environment, we create a kind cluster and observe the changes.

for that first, we clone the Kubernetes repository:-

`git clone https://github.com/kubernetes/kubernetes `{{execute}}

after cloning, change the directory
`cd kubernetes`{{execute}}

make changes as given below in strategy.go [here](https://github.com/kubernetes/kubernetes/blob/4bca479dfbf74f960bbe9661c51cea70e4115a62/staging/src/k8s.io/apiextensions-apiserver/pkg/registry/customresourcedefinition/strategy.go#L122)

for that 
`cd staging/src/k8s.io/apiextensions-apiserver/pkg/registry/customresourcedefinition/`{{execute}}
`nano strategy.go`{{execute}}

return []string{“I am a warning”} instead nil in WarningsOnCreate function.

after all the changes, create a kind image as follows:-
`kind build node-image . -–image warning-test`{{execute}}

After image creation, now create a cluster.
`kind create cluster -–image warning-test --name test-cluster`{{execute}}

to get info about the cluster run the following command:-
`kubectl cluster-info --context kind test-cluster `{{execute}}

## Test with CRD

Now create a custom resource definitiion

`kubectl apply -f resourcedefinition.yaml`{{execute}}

You will see a warning on the terminal.


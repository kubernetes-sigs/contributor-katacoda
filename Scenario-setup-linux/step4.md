Making remote repository<br />
`git remote add upstream https://github.com/kubernetes/kubernetes.git`{{execute}}<br />
Never push to upstream master<br />
`git remote set-url --push upstream no_push`{{execute}}<br />
Confirm that your remotes make sense:<br />
`git remote -v`{{execute}}<br />

Get your local master up to date:<br />
`git fetch upstream `{{execute}}<br />

NOTE :- Here also we can use `--depth` flag. Basically this flag is used to get deepen history of shallow clone.
`git fetch upstream --depth 1`<br/>

`git checkout master`{{execute}}<br />
`git rebase upstream/master`{{execute}}
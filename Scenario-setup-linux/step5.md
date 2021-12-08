### 5. Run Basic Developer workflow
Generating the OpenAPI spec and related files<br />
`hack/update-generated-swagger-docs.sh`{{execute}}<br />
`hack/update-openapi-spec.sh`{{execute}}<br />
`hack/update-generated-protobuf.sh`{{execute}}<br />

Run `git status`{{execute}} to see what was generated<br />

The `copycli` command cleans the temporary build directory, generates the kubectl command file
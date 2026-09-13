# GitHub Actions study

This repo has the only purpose to create and publish a custom Docker image on DockerHub.

You can find the published image at https://hub.docker.com/r/akaenrico/demo.

The Action runs on every push made in any branches. It is composed by two different jobs:

| Job        | Objective                                                                                                                                       |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| `validate` | Checkout code, setup a Go environment and run the `go vet ./...` command to examine the source code and reports suspicious constructs           |
| `publish`  | Checkout code, authenticate to DockerHub using the DockerHub token passed as a repository secret, build the image and finally push to DockerHub |

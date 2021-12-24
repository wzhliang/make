# make

A makefile system that ease the pain of working with multiple micro services in a Kubernetes cluster.

Features:

1. Building docker image for multiple platforms like amd64 and arm64
1. Easily view logs from multiple instances of a workload
1. View currently deployed image
1. Viewing current workload spec
1. Execute shell in one of the selected instances
1. Scale down workload for debugging purpose
1. Deploy and rollback of workload
1. Automatically install required tools
1. Self update 😎 core `Makefile.incl`

All with simple `make` commands

    "make build" to build binary locally.
    "make docker" to build docker image or
    "make docker-arm" to build docker imamge for ARM
    "RELEASE=foobar make release" to build release docker imamge and push to test repo.
    "make logs" to view logs with stern
    "make current" to view currently deployed image(s) and pods status
    "make spec" to view deployment YAML
    "make deploy" and "make rollback" are obvious.
    "make shell" launches a shell into a container
    "make singleton" scales deployment into a single pod
    "make restart" restart deployment
    "make install-tools" to install tools required.
    "make update-make" to update this file to latest version.

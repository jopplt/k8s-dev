# k8s-dev

Develop in kubernetes locally, using [k3d](https://github.com/rancher/k3d), [skaffold](https://github.com/GoogleContainerTools/skaffold) and [kustomize](https://github.com/kubernetes-sigs/kustomize).

<!-- TABLE OF CONTENTS -->
## Table of Contents

* [Requirements](#requirements)
* [Usage](#usage)

<!-- REQUIREMENTS -->
## Requirements
| MacOS only

1. Install [go-task](https://taskfile.dev/) for task automation:
    ```sh
    brew install go-task/tap/go-task
    ```

2. Install the requirements:
    ```sh
    task install-requirements
    ```


<!-- USAGE -->
## Usage

```sh
$ task k3d:create-cluster
```
Start the local development environment:
```sh
$ task skaffold:dev
```
The example application can be reached at:
```sh
curl localhost:8000/ping
```
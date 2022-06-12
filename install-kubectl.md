# About
The Kubernetes command-line tool, `kubectl`, allows you to run commands against Kubernetes clusters. You can use `kubectl` to deploy applications, inspect and manage cluster resources, and view logs.


> You must use a `kubectl` version that is within one minor version difference of your cluster. For example, a v1.23 client can communicate with v1.22, v1.23, and v1.24 control planes. Using the latest compatible version of kubectl helps avoid unforeseen issues.


# Install kubectl binary with curl on MacOS

Use below command to download and install `latest kubectl`

```shell
$ curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/darwin/amd64/kubectl"
```

To download and install `specific version` use below command
```shell
$ curl -LO "https://dl.k8s.io/release/v1.20.0/bin/darwin/amd64/kubectl"
```

* Make the kubectl binary executable.
```shell
$ chmod +x ./kubectl
```

* Move the kubectl binary to a file location on your system PATH.

```shell
$ sudo mv ./kubectl /usr/local/bin/kubectl
$ sudo chown root: /usr/local/bin/kubectl
```

> Note: Make sure /usr/local/bin is in your PATH environment variable.

* Test to ensure the version you installed is up-to-date:

```shell
$ kubectl version --client
```

# Install kubectl binary with curl on Linux Machine

```shell
$ curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl”
$ chmod +x kubectl
$ sudo mv ./kubectl /usr/bin/kubectl

#Test to ensure the version you installed is up-to-date:
$ kubectl version --client
```
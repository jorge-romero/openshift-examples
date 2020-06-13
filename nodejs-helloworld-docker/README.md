# Simple Hello World Application
```sh
# To create an application with a git server based in the docker o source strategy

# With docker strategy
$ oc new-app --name nodedocker --context-dir nodejs-helloworld-docker https://github.com/jorge-romero/openshift-examples.git

# With source strategy
$ oc new-app --name nodesource --context-dir nodejs-helloworld-docker --strategy source nodejs~https://github.com/jorge-romero/openshift-examples.git

# To expose the service in with a specific hostname
$ oc expose svc/nodedocker --hostname node-docker.127.0.0.1.nip.io
```


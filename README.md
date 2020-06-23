# Devfile Test Drive

This projects examines the possiblities around containerized development environments using the Che Devfile.

This project has these goals:

1. Include a Quarkus application that requires a running PostgreSQL database
1. Include a Devfile to be compatible with both OpenShift Do (odo) and Che (CodeReady Workspaces)
1. Devfile work both locally with Docker and also on OpenShift in CodeReady Workspaces
1. Quarkus Development Mode
1. Quarkus Native Image
1. Fully working unit and integration tests
1. Simple and straightforward solution with minimal config

## Developer Environment Setup

These instructions assume the developer:

1. Is using a Mac with Docker installed 
1. Doesn't have (or need) experience with Kubernetes (OpenShift) from the command line 
1. Is using Visual Studio Code

### Step 1a: Install OpenShift Odo (Community Docs)

1. Go to https://odo.dev/
1. Go to https://odo.dev/docs/installing-odo/#installing-odo-on-macos

```
curl -L https://mirror.openshift.com/pub/openshift-v4/clients/odo/latest/odo-darwin-amd64 -o /usr/local/bin/odo
chmod +x /usr/local/bin/odo
```

### Step 1b: Install OpenShift Odo (Offical Docs)

1. Go to https://docs.openshift.com/container-platform/4.4/cli_reference/developer_cli_odo/installing-odo.html
2. Go to https://docs.openshift.com/container-platform/4.4/cli_reference/developer_cli_odo/installing-odo.html#binary-installation-3

```
curl -L https://mirror.openshift.com/pub/openshift-v4/clients/odo/latest/odo-darwin-amd64 -o /usr/local/bin/odo
chmod +x /usr/local/bin/odo
```

> Note that for Community and Official, both the latest version of Odo is used.




## References

1. https://odo.dev/docs/deploying-a-devfile-using-odo/#deploying-a-java-spring-boot-component-locally-to-docker
1. https://github.com/redhat-developer-demos/quarkus-reactjs-postit-app
1. 

## GitHub Issues

1. https://github.com/openshift/odo/issues/3402
1. https://github.com/openshift/odo/issues/2557 


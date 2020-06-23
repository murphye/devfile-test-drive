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

### Step 2: Enable Experimental Mode

```
odo preference set experimental true
```

### Step 3: Set Push Target to Docker for Local Development

```
odo preference set pushtarget docker
```

### Step 4: Download Sample Project for Local Development (TODO)

```
git clone https://github.com/odo-devfiles/springboot-ex
```

### Step 5: Create Component Configuration (TODO)

```
odo create java-spring-boot mydockerspringboot
```

### Step 6: Deploy Application Locally (TODO)

```
odo url create --port 8080
odo push
```

Watch for `✓  URL 127.0.0.1:59382 created` to get the local URL

> When odo deploys a devfile component, it pulls the images for each dockercontainer in devfile.yaml and deploys them. Each docker container that is deployed is labeled with the name of the odo component. Docker volumes are created for the project source, and any other volumes defined in the devfile and mounted to the necessary containers.

Go to http://127.0.0.1:59382 to see the application


## References

1. https://odo.dev/docs/deploying-a-devfile-using-odo/#deploying-a-java-spring-boot-component-locally-to-docker
1. https://github.com/redhat-developer-demos/quarkus-reactjs-postit-app
1. 

## GitHub Issues

1. https://github.com/openshift/odo/issues/3402
1. https://github.com/openshift/odo/issues/2557 


# anypoint-cli-docker-images

This is an easy way to run anypoint-cli and anypoint-cli-v4 side by side without messing with your Node and NPM installs.

## requirements
You will need docker installed in order to run the container images: https://docs.docker.com/engine/install/

## how to use it:

1) Go to the anypoint cli version that you need to use:

```
cd anypoint-cli
```
or
```
cd anypoint-cli-v4
```

2) Getting the images:
You have two options: 
*a) Build them locally:*
```
docker build . -t anypoint-cli
```
```
docker build . -t anypoint-cli-v4
```
*b) Pull the images from the docker repo:*
```
docker pull javabr/anypoint-cli
```
```
docker pull javabr/anypoint-cli-v4
```

3) That is all folks! Run any cli commands:

```
docker run anypoint-cli exchange asset list Salesforce \
    --output json \
    --client_id [connected app client id] \
    --client_secret [connected app client secret] \
    --organization [organization id] \
    --environment [name of the anypoint environment(Case sensitive)]
```

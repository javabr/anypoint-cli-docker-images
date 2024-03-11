# anypoint-cli-docker-images

This is an easy way to run anypoint-cli and anypoint-cli-v4 side by side without messing with your Node and NPM installs.

You will need docker installed in order to run the the containers: https://docs.docker.com/engine/install/

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
*a) Build it locally:*
```
docker build . -t anypoint-cli
```
```
docker build . -t anypoint-cli-v4
```
*b)Pull the image from the docker repo:*
```

3) Run the commands! For example:

```
docker run anypoint-cli exchange asset list Salesforce \
    --output json \
    --client_id [connected app client id] \
    --client_secret [connected app client secret] \
    --organization [organization id] \
    --environment [name of the anypoint environment(Case sensitive)]
```
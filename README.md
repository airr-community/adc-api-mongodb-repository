# MongoDB database repository for the AIRR Data Commons (ADC) API

This is a dockerized instance of MongoDB V3 based upon the [official
mongo docker image](https://hub.docker.com/_/mongo/) with additional
customizations specific to the AIRR Data Commons.

## Deployments

It is expected that adc-api-mongodb-repository will be deployed as one
component of the reference implementation for the AIRR Data Commons API.

## Configuration Procedure

Refer to the [official mongo docker
image](https://hub.docker.com/_/mongo/) about additional
configurations settings.

**Host configuration**

[Docker](https://www.docker.com) needs to be installed either directly on the host machine or within a VM.

**Configuring adc-api-mongodb-repository**

This is general information. More detailed instructions are provided
in the overall configuration for [AIRR Data Commons API](https://github.com/airr-community/adc-api/).

Copy dbsetup.defaults to dbsetup.js and edit accordingly, to provide customization of the Mongo instance, namely:

```
cd adc-api-mongodb-repository
cp dbsetup.defaults dbsetup.js
emacs dbsetup.js
```

Make sure NOT to accidently commit the dbsetup file with usernames and passwords into the 
git repository (note: we put dbsetup.js into the .gitignore as a failsafe!)

# CloudRun Sandbox

## Requirements

Install other dependencies
```
$ gcloud components update
$ gcloud components install beta
$ gcloud config set run/region us-central1
$ gcloud auth configure-docker
$ gcloud components install docker-credential-gcr
```

## Build

```
gcloud builds submit --project ${PROJECT_ID} --tag gcr.io/${PROJECT_ID}/helloworld
```

## Deploy

```
gcloud beta run deploy --project ${PROJECT_ID}--image gcr.io/${PROJECT_ID}/helloworld
```

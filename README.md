# Google App Engine Dockerfiles

**Building and uploading to cloud registry:**
https://cloud.google.com/container-registry/docs/pushing-and-pulling?hl=de

```bash
docker build ruby-266/Dockerfile
gcloud auth configure-docker
docker tag <image-id> eu.gcr.io/expomobilia-one/ruby-266
docker push eu.gcr.io/expomobilia-one/ruby-266
```

**Usage**

Dockerfile:  
```Dockerfile
FROM eu.gcr.io/expomobilia-one/ruby-253

COPY . /app/
```

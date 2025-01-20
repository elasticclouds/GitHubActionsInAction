# GitHub Actions In Action

```
python -m venv venv

.\venv\Scripts\activate

deactivate
```

```
pip install  -r requirements.txt

uvicorn app.main:app
```

```
tags: docker.io/ha20003660/sample-fast-api:latest

docker pull docker.io/ha20003660/sample-fast-api:latest

docker run -dp 8080:80 --rm  docker.io/ha20003660/sample-fast-api:latest

docker run --pull=always -dp 8080:80 --rm  docker.io/ha20003660/sample-fast-api:latest
```

```
curl localhost:8080/openapi.json | jq

curl localhost:8080/info | jq

curl localhost:8080 | jq

curl localhost:8080/operation/area/25 | jq
```

# GitHub Actions In Action

#### Install, Start and Stop Virtual Env

```
python -m venv venv

.\venv\Scripts\activate

deactivate
```

#### Install Dependencies and Start App


```
pip install  -r requirements.txt

uvicorn app.main:app
```

#### Run Tests, Generate Coverate Report


```
pytest tests/

pytest  --cov=app.main  tests/

pytest  --cov=app.main --cov-report=html  tests/
```

#### Pull the Docker Image & Run it


```
tags: docker.io/ha20003660/sample-fast-api:latest

docker pull docker.io/ha20003660/sample-fast-api:latest

docker run -dp 8080:80 --rm  docker.io/ha20003660/sample-fast-api:latest

docker run --pull=always -dp 8080:80 --rm  docker.io/ha20003660/sample-fast-api:latest
```

#### Test the application from Docker Run


```
curl localhost:8080/openapi.json | jq

curl localhost:8080/info | jq

curl localhost:8080 | jq

curl localhost:8080/operation/area/25 | jq
```

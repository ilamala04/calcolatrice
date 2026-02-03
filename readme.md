# uv 

installa uv da https://docs.astral.sh/uv/#installation

```shell
uv venv
```

attivare ambiente virtuale

```shell
source .venv/bin/activate  (Linux/Mac)
.venv\Scripts\activate    (Windows)    
```

```shell
uv pip compile requirements/requirements-test.in -o requirements/requirements-test.txt
uv pip compile requirements/requirements.in -o requirements/requirements.txt
uv pip install -r requirements/requirements-test.txt
uv pip install -r requirements/requirements.txt
```

```shell
uv run python calcolatrice.py
python3 calcolatrice.py
```

```shell
pytest -v
```


```shell
docker build -f Dockerfile.debian -t calcolatrice:debian .
docker build -f Dockerfile -t calcolatrice:alpine .
```

```shell
docker run -it --rm calcolatrice:local
docker run -it --rm calcolatrice:alpine
```

```shell
docker build -f Dockerfile -t ilamala04/fullstack-calcolatrice:alpine .
docker push ilamala04/fullstack-calcolatrice:alpine
```

costruire immagine multipiattaforma

```shell
docker buildx build --platform linux/amd64,linux/arm64 -f Dockerfile -t ilamala04/fullstack-calcolatrice:alpine --push .
```

pytest.yml: Esecuzione dei test con pytest
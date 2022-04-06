# dockers-config

Other repos requires some docker images built from this repo. This images are published on
[github container registry](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry).

## Build dockers

```bash
docker build -t ghcr.io/intlekt/intlket_python_builder . -f dockers/Dockerfile_python_builder
docker push ghcr.io/intlekt/intlket_python_builder

docker build -t ghcr.io/intlekt/intlket_wasm_builder . -f dockers/Dockerfile_wasm_builder
docker push ghcr.io/intlekt/intlket_wasm_builder
```

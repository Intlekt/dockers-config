# Dockers config

Other repos require some docker images built from this repo. This images are published on
[github container registry](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry).

## Getting started

In order to checkout or publish the docker, you need to be login to the github container registry.

You can follow this [link](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry):

1. create a personal access token [there](https://github.com/settings/tokens) with permissions `read:packages` and `write:packages`
2. type command `export CR_PAT=YOUR_TOKEN` in your terminal
3. type command `echo $CR_PAT | docker login ghcr.io -u USERNAME --password-stdin` in your terminal

## Build dockers

```bash
docker build -t ghcr.io/intlekt/intlekt_python_builder . -f Dockerfile_python_builder
docker push ghcr.io/intlekt/intlekt_python_builder

docker build -t ghcr.io/intlekt/intlekt_wasm_builder . -f Dockerfile_wasm_builder
docker push ghcr.io/intlekt/intlekt_wasm_builder

docker build -t ghcr.io/intlekt/intlekt_test_builder . -f Dockerfile_test_builder
docker push ghcr.io/intlekt/intlekt_test_builder
```

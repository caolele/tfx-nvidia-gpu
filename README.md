# Tensorflow TFX with NVIDIA drivers

Tensorflow TFX with NVIDIA drivers included for easy usage; it can be used on TFX pipelines on Kubeflow where the underlying Kubernetes have supported GPU nodes.

## Build and publish the image

```bash
docker build -t leleca/tfx-nvidia-gpu .
docker run leleca/tfx-nvidia-gpu
docker tag leleca/tfx-nvidia-gpu leleca/tfx-nvidia-gpu:0.24.1
docker login
docker push leleca/tfx-nvidia-gpu:0.24.1
```

### Usage

In TFX Kubeflow pipeline image must be set to customa value: `leleca/tfx-nvidia-gpu:<version>`
Images available tags are on https://hub.docker.com/r/leleca/tfx-nvidia-gpu/tags

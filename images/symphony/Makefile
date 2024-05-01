IMAGE_REG := quay.io
IMAGE_NAMESPACE := lrossett/symphony
IMAGE_TAG := latest
IMAGE :=${IMAGE_REG}/${IMAGE_NAMESPACE}:${IMAGE_TAG}
BUILD_OPTS :=

.PHONY: image/build
image/build:
	podman build ${BUILD_OPTS} -t ${IMAGE} .

.PHONY: image/push
image/push:
	podman push ${IMAGE}

.PHONY: image
image: image/build image/push

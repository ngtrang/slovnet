
ROOT = ~/proj/slovnet
IMAGE = natasha/slovnet-syntax

image:
	cd $(ROOT); docker build \
		-t $(IMAGE) \
		-f docker/slovnet-syntax/torch/Dockerfile .

push:
	docker push $(IMAGE)

run:
	docker run -it --rm \
		-p 8080:8080 \
		-e DEVICE=cpu \
		-e BATCH_SIZE=4 \
		$(IMAGE)


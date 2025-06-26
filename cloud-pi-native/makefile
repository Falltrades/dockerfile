# ---------- CONFIG ----------
IMAGE_NAME     = falltrades/cloud-pi-native
IMAGE_TAG      = 1.0.0 
DOCKERFILE     = post-conf 

# ----------------------------

.PHONY: all final clean

all: final

## Build the final multi-stage image
final:
	@echo "🐳 Building final image: $(IMAGE_NAME):$(IMAGE_TAG)"
	@DOCKER_BUILDKIT=1 docker build \
		-f $(DOCKERFILE) \
		-t $(IMAGE_NAME):$(IMAGE_TAG) .

	@$(MAKE) clean

## Cleanup temp files
clean:
	@echo "🧹 Cleaning temp files..."
	@rm -f $(SECRET_FILE) $(CA_CERT_DEST)

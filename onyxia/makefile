# ---------- CONFIG ----------
IMAGE_NAME     = falltrades/onyxia-custom
IMAGE_TAG      = 1.0.0 
DOCKERFILE     = onyxia-custom 

CA_CERT_SRC    = /etc/ssl/certs/ca-certificates.crt
CA_CERT_DEST   = ./custom-ca-bundle.crt
# ----------------------------

.PHONY: all final clean

all: final

## Build the final multi-stage image
final:
	@echo "📜 Copying CA cert bundle..."
	@cp $(CA_CERT_SRC) $(CA_CERT_DEST)

	@echo "🐳 Building final image: $(IMAGE_NAME):$(IMAGE_TAG)"
	@DOCKER_BUILDKIT=1 docker build \
		-f $(DOCKERFILE) \
		-t $(IMAGE_NAME):$(IMAGE_TAG) .

	@$(MAKE) clean

## Cleanup temp files
clean:
	@echo "🧹 Cleaning temp files..."
	@rm -f $(SECRET_FILE) $(CA_CERT_DEST)

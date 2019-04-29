NAME := flexget
VERSION := $(shell cat VERSION.txt)

.DEFAULT_GOAL := help

.PHONY: dockerbuild
dockerbuild: ## Builds docker container
	docker build -t isaacasensio/$(NAME):"$(VERSION)" .

.PHONY: dockerpublish
dockerpublish: ## Publish docker image
	docker tag isaacasensio/$(NAME):"$(VERSION)" isaacasensio/$(NAME):latest
	docker push isaacasensio/$(NAME):"$(VERSION)"
	docker push isaacasensio/$(NAME):latest

.PHONY: help
help:
	@grep -E '^[a-zA-Z_-]+:.*?## .*$$' $(MAKEFILE_LIST) | sort | awk 'BEGIN {FS = ":.*?## "}; {printf "\033[36m%-30s\033[0m %s\n", $$1, $$2}'

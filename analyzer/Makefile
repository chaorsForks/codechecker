-include Makefile.local

CURRENT_DIR = $(shell pwd)

# Root of the repository.
ROOT = $(CURRENT_DIR)/..

ACTIVATE_DEV_VENV ?= . venv_dev/bin/activate

VENV_DEV_REQ_FILE ?= requirements_py/dev/requirements.txt

include tests/Makefile

pip_dev_deps:
	pip install -r $(VENV_DEV_REQ_FILE)

venv_dev:
	# Create a virtual environment for development.
	virtualenv -p python2 venv_dev && \
		$(ACTIVATE_DEV_VENV) && pip install -r $(VENV_DEV_REQ_FILE)

clean_venv_dev:
	rm -rf venv_dev

# TODO: add targets to build analyzer separately.

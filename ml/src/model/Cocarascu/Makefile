export PYTHONPATH:=$(PYTHONPATH):$(COCARASCU_SRC_DIR)

MODEL_MODULE = $(COCARASCU_SRC_DIR)/Cocarascu.py

MODEL_NAME = Cocarascu
MODEL = $(MODEL_OUTPUT_DIR)/$(MODEL_NAME).h5

EVALUATION = $(EVALUATION_OUTPUT_DIR)/$(MODEL_NAME)_metrics.csv

$(MODEL): $(COCARASCU_SRC_DIR)/train_cocarascu_model.py \
		$(MODEL_MODULE) \
		$(PREPROCESSED_TRAINING_ARGUMENTS) \
		$(PREPROCESSED_VALIDATION_ARGUMENTS) \
		$(EMBEDDING) 
	$(PYTHON) $^ $@
	@echo

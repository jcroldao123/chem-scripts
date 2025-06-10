.PHONY: install uninstall clean zip test

install:
	python3 -m venv venv && \
	source venv/bin/activate && \
	pip install -e .

uninstall:
	rm -rf venv

zip:
	zip -r chem-scripts.zip chem_scripts

clean:
	find . -type d -name "__pycache__" -exec rm -r {} +; \
	rm -rf *.egg-info build dist

test:
	@echo "No test suite defined yet."


# chem-scripts/README.md

Chem Scripts
============

This repository contains a collection of Python scripts designed to support quantum chemistry workflows, file management, and data extraction—especially for simulations using Gaussian and NAMD.

Project Structure:
------------------

```
chem_scripts/
├── occupations/
│   ├── extract_occupations.py
│   ├── reorder_occupation_table.py
│   └── average_occupation_analysis.py
│
├── contributions/
│   ├── extract_contributions.py
│   ├── organize_contributions.py
│   ├── detect_contribution_changes.py
│   └── average_contributions.py
│
├── gaussian/
│   ├── evaluate_gaussian_outputs.py
│   ├── extract_final_coordinates.py
│   ├── copy_valid_logfiles.py
│   └── update_filenames.py
│
├── maintenance/
│   ├── lowercase_and_deduplicate.py
│   ├── cleanup_and_dedup_chk.py
│   └── clean_temp_files.py
│
├── scripts/
│   ├── gauss0opt2sptd-stable.sh
│   ├── contribeval.sh
│   ├── gamessrun-stable.sh
│   ├── gamesschoirun-stable.sh
│   ├── everteval.sh
│   ├── molcasrun-stable.sh
│   └── molcasrun_series-stable.sh
```

Installation:
-------------
Create and activate a virtual environment:

```bash
python3 -m venv venv
source venv/bin/activate
```

Then install the package:

```bash
pip install -e .
```

Or use:
```bash
make install
```

Requirements:
-------------
- Python 3.7+
- pandas
- openpyxl

Entry Points:
-------------
After installation, the following commands are available in the terminal:

```bash
chem-extract-occupations --prefix molecule
chem-average-occupations --prefix molecule --step-size 0.5
chem-eval-gaussian --prefix mymol --output results.xlsx
chem-clean-temp
```

Shell Scripts:
--------------
Additional bash scripts for automated preparation, submission, and evaluation:

```bash
bash scripts/gauss0opt2sptd-stable.sh     # Generate Gaussian .gjf files from optimized logs
bash scripts/contribeval.sh              # Run full contribution extraction pipeline
bash scripts/gamessrun-stable.sh         # Submit GAMESS jobs via PBS
bash scripts/gamesschoirun-stable.sh     # Alternative GAMESS run setup with custom scratch
bash scripts/everteval.sh                # Evaluate electronic state orderings
bash scripts/molcasrun-stable.sh         # Submit a single OpenMolcas job
bash scripts/molcasrun_series-stable.sh  # Generate and optionally run a series of OpenMolcas jobs
```

Using the Makefile:
-------------------
You can use `make` for common tasks:

```bash
make install        # Set up virtualenv and install package
make clean          # Remove __pycache__ and build artifacts
make zip            # Create chem-scripts.zip
make uninstall      # Remove virtualenv
```

Documentation:
--------------
To generate HTML documentation using Sphinx:

```bash
pip install sphinx
sphinx-quickstart docs
```

Then edit `docs/index.rst` and add modules with:

```bash
sphinx-apidoc -o docs/source chem_scripts
cd docs
make html
```

The documentation will be built in `docs/_build/html/index.html`.


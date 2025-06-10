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

Using the Makefile:
-------------------
You can use `make` for common tasks:

```bash
make install        # Set up virtualenv and install package
make clean          # Remove __pycache__ and build artifacts
make zip            # Create chem-scripts.zip
make uninstall      # Remove virtualenv
```

License:
--------
MIT License (or your preferred license)


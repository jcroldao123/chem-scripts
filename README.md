# chem-scripts/README.md

Chem Scripts
============

<<<<<<< HEAD
This repository contains a collection of Python scripts designed to support quantum chemistry workflows, file management, and data extraction—especially for simulations using Gaussian and NAMD.
=======
This repository contains a collection of Python and Bash scripts designed to support quantum chemistry workflows, especially for simulations using Gaussian, NAMD, GAMESS, and Molcas.
>>>>>>> 24663b9 (Initial commit: chem scripts, docs, and tools)

Project Structure:
------------------

```
chem_scripts/
<<<<<<< HEAD
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
=======
├── occupations/                  # Analysis of orbital occupations
├── contributions/                # Analysis of CI coefficients and contributions
├── gaussian/                     # Parsing and evaluation of Gaussian log files
├── maintenance/                  # File cleanup, deduplication, renaming
├── scripts/                      # Bash scripts for job submission and automation
├── docs/manuals/                 # Markdown tutorials and guides
└── docs/source/                  # Sphinx documentation source
>>>>>>> 24663b9 (Initial commit: chem scripts, docs, and tools)
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
<<<<<<< HEAD
=======

>>>>>>> 24663b9 (Initial commit: chem scripts, docs, and tools)
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
<<<<<<< HEAD
After installation, the following commands are available in the terminal:

```bash
chem-extract-occupations --prefix molecule
chem-average-occupations --prefix molecule --step-size 0.5
chem-eval-gaussian --prefix mymol --output results.xlsx
=======
After installation, you can run tools like:

```bash
chem-extract-occupations --prefix molecule
chem-average-contributions --input summary.csv
chem-eval-gaussian --prefix job --output summary.xlsx
>>>>>>> 24663b9 (Initial commit: chem scripts, docs, and tools)
chem-clean-temp
```

Shell Scripts:
--------------
<<<<<<< HEAD
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
=======
Bash scripts to assist in job preparation and submission:

```bash
bash scripts/gauss0opt2sptd-stable.sh       # Generate .gjf files from optimized logs
bash scripts/contribeval.sh                # Pipeline for extracting contributions
bash scripts/gamessrun-stable.sh           # Submit GAMESS job to PBS
bash scripts/molcasrun-stable.sh           # Submit OpenMolcas calculation
```

Manuals:
--------
Additional documentation and tutorials:

- `docs/manuals/gaussian_orca_tutorial.md` – Guide for Gaussian and ORCA workflows
- `docs/manuals/quantum_chem_notes.md` – Notes on several quantum chemistry packages

Sphinx Documentation:
---------------------
To build HTML docs:

```bash
pip install sphinx myst-parser
>>>>>>> 24663b9 (Initial commit: chem scripts, docs, and tools)
cd docs
make html
```

<<<<<<< HEAD
The documentation will be built in `docs/_build/html/index.html`.
=======
Output will be in: `docs/_build/html/index.html`

License:
--------
MIT License
>>>>>>> 24663b9 (Initial commit: chem scripts, docs, and tools)



# Getting Started with Chem Scripts 🧪

Welcome, students! This guide will help you quickly set up and use the Chem Scripts tools on your own machine.

---

## 📦 Step 1: Clone the Repository

Open a terminal and run:

```bash
git clone https://github.com/jcroldao123/chem-scripts.git
cd chem-scripts
```

---

## 🧪 Step 2: Set Up Your Environment

Create and activate a virtual environment:

```bash
python3 -m venv venv
source venv/bin/activate
```

Install dependencies:

```bash
pip install -e .
```

Or use:

```bash
make install
```

---

## ⚙️ Step 3: Run Useful Commands

Here are a few commands available after installation:

```bash
chem-extract-occupations --prefix mymolecule
chem-eval-gaussian --prefix calc --output results.xlsx
chem-clean-temp
```

---

## 📚 Tutorials and Help

You can find more information in:

- `docs/manuals/gaussian_orca_tutorial.md`
- `docs/manuals/quantum_chem_notes.md`

To build the full HTML documentation:

```bash
cd docs
make html
```

Then open `docs/_build/html/index.html` in your browser.

---

## 🤝 Need Help?

Ask your instructor or check the `README.md` for detailed descriptions of each folder and tool.

Happy computing!

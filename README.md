![BuildStatus](https://github.com/bmi203-2023/Minimal-Example/actions/workflows/main.yml/badge.svg?event=push)
[![Documentation Status](https://readthedocs.org/projects/minimal-example/badge/?version=latest)](https://minimal-example.readthedocs.io/en/latest/?badge=latest)

# Minimal-Example
Demonstrate the minimal concepts/training to structure a project, build Python packages, unit testing, GitHub Actions, package managers, distributions, containers, and Read the Docs.

## Project Structure

```bash
Minimal-Example # Working Directory
├── README.md
├── data # A data directory for any relevant data used for unit testing, training, etc.
│   └── the-zen-of-python.txt
├── docs # This makes the module's ReadTheDocs.
│   ├── Makefile
│   ├── build
│   ├── make.bat
│   └── source
│       ├── _static
│       ├── _templates
│       ├── conf.py
│       ├── example.rst
│       ├── index.rst
│       └── modules.rst
├── pyproject.toml # Definition of build process of the package.
├── src # The src directory contains all of the source material for building the project.
│   └── example # The Python example package directory.
│       ├── __init__.py # This makes the directory a package.
│       └── welcome.py # The example's welcome module.
└── test # The test directory contains all of the unit testing material.
    └── test_greeting.py
```
To create a project directory tree as seen above for your README, please follow these commands:

```bash
$ brew install tree
$ tree Minimal-Example -o tree.md
```
For more references on project directory structure/organization, here are a few helpful links:
* [A Practical Guide to Setuptools and Pyproject.toml](https://godatadriven.com/blog/a-practical-guide-to-setuptools-and-pyproject-toml/)

## Building a Python Package

We can automate the majority of building a Python package, however, there are a few starting steps to consider. Here we'll outline the best practices (we're aware of) to simplify the process.

**1. Install conda**

**2. Create a clean environment and activate it**

```bash
$ conda create --name minimal_example python=3.9
$ conda activate minimal_example
```

**3. Install the minimal depedencies for unit testing**

```bash
$
```

** Create a pyproject.toml in the working directory that specifies the package's build system.**

```python
[build-system]
requires = [
	"flit_core >=3.2,<4",
	"python_version >= '3.9'"
	]
build-backend = "flit_core.buildapi"

[project]
name = "<your name>"
authors = [{name = "<name>", email = "<email>"}]
license = {file = "LICENSE"}
classifiers = ["License :: OSI Approved :: MIT License"]
dynamic = ["version", "description"]
dependencies = ["pytest", "numpy", "scipy", "matplotlib", "scikit-learn", "sphinx"]

[tool.coverage.run]
source = ["src"] # parent directory of package

[project.urls]
Home = "https://github.com/<your git handle or organization>/<repository name>"
````

For more references on Python packaging, here are a few helpful links:
* [A pyproject.toml Developer's Cheat Sheet](https://betterprogramming.pub/a-pyproject-toml-developers-cheat-sheet-5782801fb3ed)

## Unit Testing




## GitHub Actions


## Package Managers, Distributions, & Containers

* [Miniconda](https://docs.conda.io/en/latest/miniconda.html)
* [Homebrew](https://brew.sh/)

## Read the Docs

## UCSF High Performance Computing (HPC) Resources
# Welcome to GIS Package Development


[![image](https://img.shields.io/pypi/v/gisdev.svg)](https://pypi.python.org/pypi/gisdev)


**Python Boilerplate contains all the boilerplate you need to create a Python package.**


-   Free software: MIT License
-   Documentation: <https://bernardofosu.github.io/gisdev>


## Features
- Interactive Maps
- Geospatial Analysis

### Install Dependencies on the local and build it locally
```sh
conda activate gis

pip install -r requirements_dev.txt
```

### How to build locally
```sh
mkdocs build

mkdocs serve
```
You will see a new directory called site
Whenever we make changes we have to rebuild using `mkdocs build`

We can also use `mkdocs serve` to automatically update the website when we make changes but it will shutdown when we close or exit the terminal.

The `mkdocs build` build the website and put in the site directory but `mkdocs serve` just build the website in temporal session on port 8000

If You want to add anything to the website its has to be in the `doc` directory

### Install Pre-Commit on the Local Machine
```sh
conda activate gis

pip install pre-commit

pre-commit install

pre-commit run --all-files
```

### How to add a new version of the project
```sh
pip instal bump-my-version
```
We will check the version in the `pyproject.toml`
```sh
[project]
name = "gisdev"
version = "0.0.1"
```
The command are in 3 stage
- `bump-my-version bump patch` change the version from`0.0.1` to `0.0.2`
- `bump-my-version bump minor` change the version from `0.0.1` to `0.2.0`
- `bump-my-version bump major` change the version from `0.0.1` to `1.0.0`

```sh
git push

git push --tags
```
It will create the tags and the updated version

Go to github and create a release with the new tag
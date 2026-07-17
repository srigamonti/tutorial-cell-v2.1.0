# Tutorial for cluster expansion with `CELL` (aka `clusterx`)

## How to run the tutorials

To run this tutorial, first clone the repository containing the tutorial into your computer by executing

```bash
git clone git@scm.cms.hu-berlin.de/rigamons/tutorial-cell-v2.1.0.git
```
The execution of this command creates a folder named `tutorial-cell-v2.1.0.git` containing all necessary files to run the tutorial. 

Move into this folder by executing
```bash
cd tutorial-cell-v2.1.0.git
```
and then you have two options:

### Option 1 (recommended)

```bash
uv sync

uv run python -m ipykernel install --user --name tutor-ce --display-name "tutor-ce"

uv run jupyter notebook
```

### Option 2 (advanced)

```bash
rm -rf .venv uv.lock pyproject.toml .python-version
uv init --python ">=3.9,<3.10"
uv add $(cat requirements.txt)
uv run python -m ipykernel install --user --name tutor-ce --display-name "tutor-ce"
uv run jupyter notebook
```
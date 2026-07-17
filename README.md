If you are doing the tutorials in the course, do the following

rm -rf .venv uv.lock pyproject.toml .python-version
uv init --python ">=3.9,<3.10"
uv add $(cat requirements.txt)
uv run python -m ipykernel install --user --name bdaims-ce --display-name "bdaims-ce"
uv run jupyter notebook

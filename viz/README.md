# Dashboard

This dashboard is a visualization tool for the pep2vec model. It allows for the selection of peptides and the visualization of the embeddings of those peptides. The dashboard is built using the panel library, which is a high-level app and dashboarding solution for Python.

![Alt text](dashboard.png?raw=true "Title")

# Setup Code
Install [uv](https://docs.astral.sh/uv/getting-started/installation/) and Node.js, then run from the repository root:

```
cd viz
uv sync --locked
```

`uv sync` creates the project's virtual environment and installs the locked dependencies from `pyproject.toml` and `uv.lock`.

# Download Data
Download this file to the viz directory
https://zenodo.org/records/13932198/files/df_for_vizualization.parquet?download=1

# Running
Run the server from the `viz` directory:
```
uv run --locked panel serve start_server.py --autoreload --show
```
autoreload will auto restart the server when source code changes, this is optional.
Terminal will contain useful messages, and upon boot, will include the url needed to access.

# Notes:
    - Edit start_server.py to change input dataframe as well as pre filtering or whatnot that is desired

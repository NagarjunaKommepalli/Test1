# Custom analysis repository

This repository is a central location for custom analysis code, typically written by Comp Bio, Software, and Apps.

Each analysis should be a self-contained set of R and/or python files that operate on data that live in a single location.

The layout should be as follows:

- Code: `custom-analysis-YYYY/CAYYYY-XXXXX/`
  - Where `custom-analysis-YYYY/` is your local copy of this repo,
  - `XXXXX` is a unique zero-padded integer that identifies the analysis
- Data: `/mnt/yard1/user/data/custom-analysis-YYYY/CAYYYY-XXXXX`
  - `user` is your username

# Creating a new analysis

Before writing any code, add a row to the table at the bottom of this document, commit to master, and push.

- Analysis ID: As described above.
- Owner: Your UNIX username on the development server (`echo $USER`)
- Description: Short description of the analysis.

## Guidelines

## R

Put the main script in a file called `main.r` and the functions definitions in a file called `functions.r`. If there are functions that you use over and over again, consider putting them in the `supeRboy` package.

## Python

Put the main script in a file called `main.py` or `main.ipynb`. If there are functions you use over and over again, consider putting them in the `tenxpy` package.

## Data

- Consider putting your (ideally immutable) input data in a data subdirectory called `raw` under the analysis' data dir.
- Consider putting your processed (munged) input data in a data subdirectory called `input`.
- Consider putting your output data in a data subdirectory called `output`.

# Committing a new analysis

Follow standard branch and PR procedures.

# List of existing analyses in this repository

For older custom analyses, see <https://github.com/10XDev/custom-analysis/>

| Analysis ID  | Owner         | Description
|--------------|---------------|------------
| CAYYYY-00000 | shaun.jackman | First post

# Data Processing Application

This application processes an Excel file (`data.xlsx`), converts it to CSV, and runs a Python script (`execute.py`) to compute and output metrics to `result.json`. The following steps outline the setup and CI/CD implementation using GitHub Actions.

## Setup Instructions

### Prerequisites

- Python 3.11+
- Pandas 2.3
- Ruff linter

## Execution Steps

1. **Correct the Script:**
   - Fix any typos, such as replacing "revenew" with "revenue", and ensure logical errors are corrected in `execute.py`. Committed changes must reflect these fixes.

2. **Data Conversion:**
   - Convert `data.xlsx` to `data.csv` and commit it to the repository.

3. **CI/CD Configuration:**
   - Create a GitHub Actions workflow located at `.github/workflows/ci.yml` with the following steps:
     - Run `ruff` linter and output results.
     - Execute the script via `python execute.py > result.json`.
     - Publish `result.json` using GitHub Pages.

4. **Verification:**
   - Ensure that `execute.py`, `data.csv`, and `.github/workflows/ci.yml` exist in the repository and are correctly configured.
   - Verify that `result.json` is not part of the committed files and that the workflows run successfully upon each push.

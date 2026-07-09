# Benford's Law and False-Positive Probability Analysis

A simulation-driven probability project studying first-digit distributions and false-positive behavior.

## Overview

Probability simulations are useful when a formula is easier to understand through repeated experiments. This project studies two probability themes: false positives in decision systems and first-digit behavior described by Benford's Law.
The notebook combines mathematical reasoning, empirical frequency tables, and plots.

## Project Design

- Define a probability model or distribution.
- Use NumPy simulations to generate repeated outcomes.
- Aggregate outcomes with Pandas.
- Compare empirical results against theoretical expectations.
- Document formulas and observations in markdown.

## Key Capabilities

- False-positive simulation workflows.
- Benford-style first-digit distribution analysis.
- Empirical frequency comparison.
- Probability visualization using Matplotlib.
- Technical notes explaining results.

## Repository Structure

```text
notebooks/probability_analysis.ipynb  Main probability notebook.
docs/technical-notes.md               Technical explanation.
requirements.txt                      Python dependencies.
```

## Running Locally

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook notebooks/probability_analysis.ipynb
```

## Results and Artifacts

- Notebook plots for probability experiments.
- Frequency tables and empirical comparisons.
- Markdown technical notes.

## Reproducibility Notes

- Keep sample size and random seed fixed when comparing false-positive rates across distributions.
- Run each distribution experiment with the same significance threshold to make error-rate comparisons fair.
- Regenerate plots after changing the generator set or number of trials.
- Interpret Benford deviations alongside data-generation assumptions rather than as standalone fraud evidence.

## Detailed Workflow

- Open the probability notebook and run cells in order.
- Review the false-positive simulation setup before interpreting outputs.
- Inspect Benford-law sections to compare empirical and expected first-digit patterns.
- Use the technical notes as a concise explanation of the probability reasoning.
- Modify simulation parameters to test how empirical behavior changes.

## Implementation Details

- NumPy drives repeated probability simulations.
- Pandas organizes empirical counts and frequencies.
- Matplotlib visualizes comparisons between simulated and expected behavior.
- Markdown notes preserve formulas and observations outside the notebook.
- The notebook structure keeps experimentation and explanation together.

## Data and Inputs

- Core simulations do not require a large external dataset.
- Benford-style analysis can be extended to real numeric datasets.
- False-positive behavior depends on selected rates, thresholds, and sample sizes.
- Generated empirical results should be rerun when simulation settings change.

## How To Interpret the Results

- Empirical frequencies should converge toward theoretical expectations as sample size grows.
- False-positive rates can create unintuitive outcomes when events are rare.
- Benford's Law applies in specific data-generating contexts and should not be assumed universally.
- Plots should be read together with the assumptions used to generate them.

## Limitations and Assumptions

- Simulation conclusions depend on parameter choices.
- Benford behavior should be validated against the nature of the dataset being studied.
- Notebook outputs are exploratory unless repeated under multiple seeds.
- Additional confidence intervals would strengthen the analysis.


## Review Guide

Use this checklist when reviewing the repository on GitHub:

- Start with the overview to understand the project objective before opening notebooks or source files.
- Read the repository structure section to identify the main entry point.
- Inspect generated outputs before rerunning experiments; they provide a quick view of the current project state.
- Review scripts and notebooks together when both are present, since notebooks often explain decisions while scripts preserve reusable execution paths.
- Check the limitations section before interpreting results too strongly.
- Use the possible extensions section to understand how the project can grow without changing its core purpose.

## Troubleshooting

Common issues and fixes:

- If imports fail, confirm that the virtual environment is activated and dependencies were installed from `requirements.txt`.
- If a notebook cell fails because a variable is missing, restart the kernel and run the notebook from the first cell.
- If a script cannot find a data file, run it from the repository root unless the README gives a different working directory.
- If plots are not regenerated, check that the output folder exists and that the script has write permission.
- If a package version causes errors, create a fresh environment and reinstall dependencies before debugging the source code.
- If GPU-related packages are unavailable, run CPU-compatible sections first and treat heavier deep-learning experiments separately.

## Development Notes

The repository is organized to be understandable before it is optimized. Most code favors clear structure, visible intermediate steps, and saved artifacts over highly compressed implementations. When extending the project, prefer small changes that keep the original experiment reproducible.

Recommended development practices:

- Keep new data files under `data/`, `datasets/`, or the existing local data folder for that project.
- Keep generated figures under `figures/`, `plots/`, `outputs/`, or `results/` depending on the existing convention.
- Add new experiments as separate scripts or clearly labeled notebook sections.
- Avoid overwriting existing outputs unless the experiment is intentionally being refreshed.
- Document any new dependency in `requirements.txt`.
- Prefer relative paths so the repository works after cloning on another machine.

## Project Status

This repository is prepared as a standalone GitHub project. The current version includes the core implementation, documentation, and available artifacts needed to understand the work. Future improvements can focus on stronger automation, more tests, richer visual summaries, and cleaner packaging where appropriate.

## Possible Extensions

- Export plots into a dedicated `figures/` folder.
- Add parameterized scripts for repeated probability simulations.
- Add confidence interval estimates for empirical frequencies.
- Compare Benford behavior across multiple real datasets.

## Tech Stack

Python, NumPy, Pandas, Matplotlib, Jupyter Notebook.

## Author

Prahladha, IIT Hyderabad

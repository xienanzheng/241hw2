# INFO 241 - Homework 2

Replication of Dekker, Luberti and Stam (2023), randomisation inference, and power analysis for three communication experiments.

## Files

- [PDF](problem_set_2.pdf): answers, key code, results and figures.
- [HTML](problem_set_2.html): browser version.
- [Notebook](problem_set_2.ipynb): executed analysis.
- [Quarto source](problem_set_2.qmd): editable text and code.
- `data/`: original instructor-supplied data.
- `outputs/`: result tables and figures.

## Data note

The supplied processed file drops 18 valid decimal grades: 414 grades remain, compared with 432 in the raw CSV. Both versions are analysed. The raw-data grade difference is 0.367 points (randomisation p=0.04816); the processed-file result is 0.318 (p=0.09461). The original data and cleaning script are retained.

## Run

```sh
uv sync
uv run jupyter nbconvert --to notebook --execute --inplace problem_set_2.ipynb
```

With Quarto installed, render the source directly:

```sh
uv run quarto render problem_set_2.qmd --to html
uv run quarto render problem_set_2.qmd --to typst
```

The analysis uses seed 2412026, 99,999 randomisation draws and 50,000 power simulations. The report states the missingness, interference and power-planning assumptions.

## Sources

- [Paper](https://doi.org/10.1016/j.learninstruc.2023.101805)
- [Preregistration](https://osf.io/96zp4/)
- [Instructor starter](https://github.com/info-241/problem-set-2-starter)

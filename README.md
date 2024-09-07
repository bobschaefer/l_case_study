# Candy Project

This project analyzes the data from
the [Candy Power Ranking](https://github.com/fivethirtyeight/data/tree/master/candy-power-ranking/) to inform the
question of what properties make a candy popular and suitable for retail.

## Getting started

To get started with this project, make sure you have Python>=3.10 installed. Then, clone the repository and run the
following commands:

```bash
python3 -m venv .venv             # Create a virtual environment
source .venv/bin/activate         # Activate the virtual environment
pip install -r requirements.txt   # Install dependencies
jupyter lab                       # Start Jupyter Lab or use your IDE
```

## Structure

The main **analysis** is done in the `notebooks/candy.ipynb` Jupyter notebook.

**Data** is stored in the `data` directory. There is only one file, `candy-data.csv`, which contains the data used in
the
analysis.

The **output** of the analysis is stored in the `output` directory. This includes
the `candy_{generation_timestamp}.pptx`
file, which is a single-slide PowerPoint presentation. The slide can automatically be updated with the latest data by
running the `notebooks/candy.ipynb` notebook.

## Assumptions

We made the following assumptions in our analysis:

* The data is complete and accurate and does not require cleaning or preprocessing.
* The data is representative and universally applicable to the market at hand (see [Notes on data](#notes-on-data)).

## Notes on data

* Data is only for the US market
* Data is not point-of-sale preference, but preference of (likely) adults on Halloween candy
* Data has seasonal bias as it was collected around Halloween and concerns candy handed out to trick-or-treaters

## Caveats

This project uses an outdated version of `numpy` (2.0.2 instead of the latest 2.1.1). This is necessary to ensure
compatibility with the `statsmodels` library. See this [GitHub issue](https://github.com/scipy/scipy/issues/21434) for
more information.
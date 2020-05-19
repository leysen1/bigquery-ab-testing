# BigQuery AB Testing

## Installation

Git clone this repository:

```
git clone https://github.com/leysen1/bigquery-ab-testing
```

Download and install the [Anaconda Python distribution](https://www.anaconda.com/distribution/).

Then activate a conda virtual environment with

```
conda env create -f environment.yml
conda activate dev
- pip install google-cloud-bigquery
- pip install plotly==4.6.0
- pip install cufflinks
- pip install httplib2
jupyter labextension install jupyterlab-plotly
```

Make sure to run the following command to save the installed libraries into the environment.yml file,
which allows others to run the report easily:

```
conda env export --no-builds > environment.yml
```

## Setting Up BigQuery Connection 

This link takes you through the steps to set up a connection with your bigquery account.
https://cloud.google.com/bigquery/docs/quickstarts/quickstart-client-libraries#client-libraries-install-python

The main points are to:
- Install the python google-cloud-bigquery python library
- Create a service account for the Google project your working in
- Create a key for the service account and download the .json file
- Enable the BigQuery API

## Usage

Start programming! Open jupyter with

```
jupyter-lab
```

And start working.


## Sharing

Push to Github and import into Kyso.
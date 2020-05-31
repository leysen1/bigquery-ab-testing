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

Google makes it simple to set up a BigQuery connection through python using some of their [walkthrough tutorials](https://cloud.google.com/bigquery/docs/quickstarts/quickstart-client-libraries#client-libraries-install-python).

You need to make sure you have selected or created an Google Cloud Project in the [Google Cloud Platform](https://console.cloud.google.com/) and enable the BigQuery API by typing BigQuery API in the search.

In order to set up the permissions to access the BigQuery, you will need to create a service account key under your chosen project. Make sure you give the service account a role of Project>Owner and save the .json key file created on your Desktop.
 
This key will allow you to connect to your BigQuery database and use SQL to query the data, as shown in the notebook.

Make sure you've also installed the necessary libraries in python to run the notebook.


## Usage

Start programming! Open jupyter with

```
jupyter-lab
```

And start working.


## Sharing

Push to Github and import into Kyso.
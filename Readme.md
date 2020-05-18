# Google Analytics Reporting API

## Installation

Git clone this repository:

```
git clone https://github.com/KyleOS/google-analytics-api
```

Download and install the [Anaconda Python distribution](https://www.anaconda.com/distribution/).

Then activate a conda virtual environment with

```
conda env create -f environment.yml
conda activate dev
- pip install --upgrade google-api-python-client
- pip install --upgrade oauth2client
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

## Setting Up Google Analytics Permissions

For reference, Google has a great [tutorial](https://developers.google.com/analytics/devguides/reporting/core/v4/quickstart/service-py) that can take you through connecting to the API, but we'll go through it in detail here.

### Enable API and Generate Private Key

- To get started using Analytics Reporting API v4, you need to first [use the setup tool](https://console.developers.google.com/start/api?id=analyticsreporting.googleapis.com&credential=client_key), which guides you through creating a project in the Google API Console, enabling the API, and creating your credentials.

#### Create Credentials

- Open the [Service Accounts](https://console.cloud.google.com/iam-admin/serviceaccounts) page. If prompted, select a project.

- Click **+ Create Service Account**, enter a name and description for the service account. You can use the default service account ID, or choose a different, unique one. When done, click **Create**.

- The Service account permissions (optional) section that follows is not required. Click **Continue**.

- On the **Grant users access to this service account** screen, scroll down to the **Create key** section. Click **+ Create key**.

- In the side panel that appears, select the format for your key: **JSON** is recommended.

- Click **Create**. Your new public/private key pair is generated and downloaded to your machine; it serves as the only copy of this key. Save this key into this directory folder and name it **client_secrets.json**.

- Click **Close** on the **Private key saved to your computer** dialog, then click **Done** to return to the table of your service accounts.

- **Remeber to add the client_secrets.json file to your .gitignore!**

#### Add Service Account to the GA Account

- The newly created service account will have an email address that looks similar to:

```
quickstart@PROJECT-ID.iam.gserviceaccount.com
```

Use this email address to [add a user](https://support.google.com/analytics/answer/1009702) to the Google Analytics view you want to access via the API. For this tutorial only [Read & Analyze](https://support.google.com/analytics/answer/2884495) permissions are needed.


## Usage

Start programming! Open jupyter with

```
jupyter-lab
```

And start working.


## Sharing

Push to Github and import into Kyso.
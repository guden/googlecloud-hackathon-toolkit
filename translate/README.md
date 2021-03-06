# gcp-hackathon-demos
Demos for GCP hackathon tech talks

Instructions

1. Create a project at console.cloud.google.com.
1. Enable the Translate API. Go to console.cloud.google.com, click the button in the top left, select 'APIs & services', click 'Enable APIs and Services' at the top, search for 'Translate', click the first result, then click the 'Enable' button.
1. Download the Google Cloud SDK command line tool, also known as `gcloud`. See https://cloud.google.com/sdk/downloads#interactive.
1. Initialize gcloud by running `gcloud init`.
1. Run `gcloud auth application-default login` to set up application default credentials.
1. Set up a service account. Visit console.cloud.google.com, search 'Service Accounts' on the top search bar, click on the first result, and click the 'Create a Service Account button' towards the top. Give your service account a name and set the 'Role' to Project > Owner. Check the 'Furnish a new private key' box and click 'Create'. Save the generated service account key json file to somewhere on your computer. Then set the `GOOGLE_APPLICATION_CREDENTIALS` variable to point to the service account key. Run `export GOOGLE_APPLICATION_CREDENTIALS=/path/to/your/service/account/key.json`.
1. Set up your virtual environment by running `virtualenv env`. If you do not already have `virtualenv` installed, run 'sudo easy_install pip' and then 'pip install virtualenv'.
1. Enter your virtual environment by running `source env/bin/activate`.
1. Install dependencies by running `pip install -r requirements.txt`.
1. Run `python main.py` to test your application locally.
1. Deploy by running `gcloud app deploy`. This should take several minutes.

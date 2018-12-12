# Setup to use existing cluster
Follow these steps to authenticate with an existing Google Kubernetes Engine cluster with a service account. You will not be able to do all tasks in the workshop with this setup.

## Install Google Cloud SDK tool
In order to explore the Kubernetes cluster on Google Kubernetes Engine you need to install the Google Cloud SDK command line tool.
1. Follow the guide to setup the `gcloud` tool, but stop before the step `gcloud init`. You can find the guide [here](https://cloud.google.com/sdk/docs/downloads-interactive)

## Activate service account
Email `linemos@gmail.com` with the topic `Kubernetes intro SA` to create a service account.

When you have received an service account, download the file. We will use it to authenticate with Google Cloud.

1. Open the file and copy the email adress in the field `client_email`
2. Use this command to authenticate your computer with the cluster:

	```
	gcloud auth activate-service-account INSERT_CLIENT_EMAIL_HERE --key-file=PATH_TO_JSON_FILE --project INSERT_PROJECT_NAME	
	```

3. Verify that you have successfully authenticated by this command:

	```
	gcloud container clusters list
	```

	The result should be similar to this:

	```
	NAME        LOCATION         MASTER_VERSION  MASTER_IP       MACHINE_TYPE   NODE_VERSION  NUM_NODES  STATUS	
	cv-cluster  europe-north1-a  1.10.2-gke.3    35.197.214.235  n1-standard-2  1.10.2-gke.3  6          RUNNING
	```

## Next

[Go back to complete the installation and setup](./1-installation-tasks.md).

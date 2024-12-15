you may need to run this command if the remote worker fails due to permission issue:

''' **sudo chmod u=rwx,g=rwx,o=rwx /path/to/worker/logs/** '''  (e.g. home/azureuser/airflow/logs)

this way airflow container have write permissions to put logs in this directory on the host

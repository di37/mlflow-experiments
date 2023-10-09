# Basic MLFlow Experiments

## Overview

## Steps to observe experiments in local environment (without storing information in sqlite db)

1. Copy paste the example from tutorial - https://mlflow.org/docs/latest/tutorials-and-examples/tutorial.html under "Training Model" section.
2. Run the command - `python app.py <alpha> <l1_ratio>`
3. Try running using different values of alpha and l1_ratio.
4. Now spin up mlflow server - `mlflow ui`
5. Open the browser and navigate to `http://localhost:5000`. Now we can compare the params and metrics.

## Steps to observe experiments in remote server DAGsHub

1. Click on "Create" at the top right corner once you are logged into your DAGsHub account.
2. Then click on "Connect to your repository". Then follow coming straight forward steps.
3. Once connection is done, we will be directed to DAGsHub repository.
4. We can get the credentials by clicking "Remote" and then "Experiments". Save it in .env file which we will be using as environment variables.
5. Include the link too app.py file for tracking remote - https://dagshub.com/di37/mlflow-experiments.mlflow.

```bash
#....signature code is above

# For Remote server only (DAGsHub)
remote_server_uri = "https://dagshub.com/di37/mlflow-experiments.mlflow"
mlflow.set_tracking_uri(remote_server_uri)

#....tracking_url_type_store code is below
```

# MYYYY

[![CI status](https://github.com/Itzblend/huhta-airflow/workflows/CI/badge.svg?branch=master)](https://github.com/Itzblend/huhta-airflow/actions?query=workflow%3ACI+branch%3Amaster+event%3Apush)

## Getting started

Open airflow.cfg file in the config folder and change following values:
    - secret_key = (Run command `openssl rand -hex 30` and use this as secret_key variable)
    


SSH into your Airflow webserver container (docker exec -it docker-airflow_webserver_1 bash):

```
# Valid roles are: [Admin, Public, Viewer, User, Op]
airflow users create -e <email> -f <firstname> -l <lastname> -r <role> -u <username>
```

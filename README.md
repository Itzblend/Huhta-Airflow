
# Huhta-Airflow docker distribution

  

![CI status](https://github.com/Itzblend/huhta-airflow/workflows/CI/badge.svg?branch=main)

  
  

## Setup

```
$ git clone git@github.com:Itzblend/huhta-airflow.git
```

Open airflow.cfg file in the config folder and change following values:

- secret_key = (Run command `$ openssl rand -hex 30` and use this as secret_key variable)

#### Run the containers
```
$ docker-compose up -d
```  
SSH into your Airflow webserver container to create admin user (docker exec -it huhta-airflow_webserver_1 bash):

```
$ airflow users create -e <email> -f <firstname> -l <lastname> -r <role> -u <username>
# Valid roles are: [Admin, Public, Viewer, User, Op]
```

#### Go to localhost:8080
At this point you should be ready to login to your Airflow instance and start using Airflow.

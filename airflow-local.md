curl -LfO 'https://airflow.apache.org/docs/apache-airflow/2.3.2/docker-compose.yaml
mkdir -p ./dags ./logs ./plugins
echo -e "AIRFLOW_UID=$(id -u)" > .env
AIRFLOW_UID=50000
docker-compose up airflow-init
docker-compose up
docker-compose run airflow-worker airflow info
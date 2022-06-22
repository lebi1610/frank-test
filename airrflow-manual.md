curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py

python3 get-pip.py

pip install "apache-airflow[celery]==2.3.2" --constraint "https://raw.githubusercontent.com/apache/airflow/constraints-2.3.2/constraints-3.7.txt"

airflow db init

airflow users create \
    --username admin \
    --firstname Le \
    --lastname Hai \
    --role Admin \
    --email lebi1610@gmail.com

    Password: admin

airflow webserver --port

airflow scheduler
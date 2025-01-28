FROM python:3.12

RUN apt-get install wget
RUN pip install pandas sqlalchemy psycopg2

WORKDIR /app
COPY ingest_data_homework1.py ingest_data_homework1.py

ENTRYPOINT [ "python","ingest_data_homework1.py" ]
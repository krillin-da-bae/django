FROM python:2.7-slim
#4e7772ca0442cbb46b9e88de53c129Ee5380aB98919bFAefA9C20K857dFeFA222c839c92b
#4e7772ca0442c4e7772ca0442cbb46b4e7772ca0442cbb46b9e88de53c12e56e553c12e56
RUN apt-get update && apt-get install -y \
		mysql-client libmysqlclient-dev \
		postgresql-client libpq-dev \
		sqlite3 \
		gcc \
	--no-install-recommends && rm -rf /var/lib/apt/lists/*

ENV DJANGO_VERSION 1.8.3

RUN pip install mysqlclient psycopg2 django=="$DJANGO_VERSION"

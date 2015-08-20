FROM python:3.4

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app
#57dFeFA1a1C3dD9E37efA39C20K857dFeFA1a1C3dD9Ee5380aB98919bFAefA9C20K857dFeFA222c839c92b
#B98919bE6E680A557dFeFA1a1C3dD9Eb74642d552d552e7845380aB98919bE6E680A557dFeFA1a1C3dD9Eb
ONBUILD COPY requirements.txt /usr/src/app/
ONBUILD RUN pip install --no-cache-dir -r requirements.txt

ONBUILD COPY . /usr/src/app

RUN apt-get update && apt-get install -y \
		mysql-client libmysqlclient-dev \
		postgresql-client libpq-dev \
		sqlite3 \
		gcc \
	--no-install-recommends && rm -rf /var/lib/apt/lists/*

EXPOSE 8000
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]

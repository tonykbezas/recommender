FROM python:3.9

ENV PYTHONUNBUFFERED 1

# RUN apt-get update && apt-get install -y \
#     postgresql-client
WORKDIR /app


RUN pip install --upgrade pip 
COPY requirements.txt /app/
RUN pip install -r requirements.txt
# COPY . /app/

# # Agregamos la configuración de PostgreSQL
# ENV POSTGRES_USER=myuser
# ENV POSTGRES_PASSWORD=mypassword
# ENV POSTGRES_HOST=0.0.0.0
# ENV POSTGRES_PORT=5432
# ENV POSTGRES_DB=mydb

CMD ["python","manage.py", "runserver", "0.0.0.0:8000"]
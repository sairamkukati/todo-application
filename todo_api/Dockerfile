FROM python:3.12-slim-bookworm

WORKDIR /app

COPY . .
RUN python3 -m pip install .[production]
RUN python3 src/manage.py collectstatic --no-input

CMD ["gunicorn", "kids_db.wsgi:application", "--chdir=/app/src", "-b=0.0.0.0:8000", "-w=4", "-t=10"]

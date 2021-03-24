FROM python:3.8-slim
ENV PYTHONUNBUFFERED=1
WORKDIR /var/www
COPY requirements.txt requirements.txt
RUN python3 -m pip install -r requirements.txt
COPY app.py .
ENTRYPOINT ["gunicorn", "app:app", "--bind=0.0.0.0:8000", "--workers=4", "--log-level=debug", "--reload"]

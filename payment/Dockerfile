FROM python:3.9-slim

EXPOSE 8080

WORKDIR /app

RUN apt-get update && \
    apt-get install -y gcc && \
    rm -rf /var/lib/apt/lists/*

COPY requirements.txt .

RUN pip3 install --no-cache-dir -r requirements.txt

COPY payment.ini .
COPY *.py .

CMD ["uwsgi", "--ini", "payment.ini"]
FROM python:3.8-slim
WORKDIR /app
RUN apt-get update \
    && apt-get install -y --no-install-recommends apache2-utils \
    && rm -rf /var/lib/apt/lists/*
COPY . .
RUN python make-data.py
RUN chmod +x generate-votes.sh
CMD ["/app/generate-votes.sh"]
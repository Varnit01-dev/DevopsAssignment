FROM python:3.10-alpine

RUN apk add --no-cache py3-pip curl && pip install flask

WORKDIR /app
COPY . .

EXPOSE 8002
CMD ["python3", "app.py"]

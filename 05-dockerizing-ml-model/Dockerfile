FROM python:3.9-slim

WORKDIR /app

RUN pip install tensorflow

COPY . ./

CMD ["python", "model.py"]
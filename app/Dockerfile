FROM python:3

WORKDIR /app

RUN pip install --upgrade pip
RUN apt-get update

COPY requirements.txt ./
RUN pip install -r requirements.txt

COPY . .

CMD ["uvicorn", "main:app", "--reload", "--host", "0.0.0.0", "--port", "8080"]
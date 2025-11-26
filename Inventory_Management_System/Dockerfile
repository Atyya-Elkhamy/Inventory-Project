
FROM python:3.12

WORKDIR /app

RUN apt-get update && apt-get install -y gcc python3-dev musl-dev

COPY requirements.txt /app/
RUN pip install --no-cache-dir -r requirements.txt

COPY . /app

EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]

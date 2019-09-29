FROM python:3.7-stretch

WORKDIR /usr/src/app

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 5000

CMD [ "gunicorn", "--reload", "-w", "10", "-b", "0.0.0.0:5000", "app:app" ]
FROM python:latest

RUN pip install uwsgi

COPY requirements.txt /tmp/
RUN pip install --no-cache-dir -r /tmp/requirements.txt

WORKDIR /app
COPY app /app
COPY build/uwsgi.ini /etc/

EXPOSE 8000

CMD [ "uwsgi", "--ini", "/etc/uwsgi.ini" ]
FROM orchardup/python:2.7
ADD requirements.pip requirements.pip
RUN pip install -r requirements.pip
VOLUME ['/opt/project/']
WORKDIR /opt/project/
EXPOSE 5000

CMD python manage.py runserver 0.0.0.0:5000

FROM orchardup/python:2.7
ADD requirements.pip requirements.pip
RUN pip install -r requirements.pip
VOLUME ['/opt/project/']
WORKDIR /opt/project/

CMD python app.py


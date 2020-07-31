FROM python:2.7-stretch
MAINTAINER Mohamed<mohamed.condeke@gmail.com>
RUN apt-get update -y
RUN apt-get install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y
RUN pip install flask flask_httpauth flask_simpleldap python-dotenv
COPY student_age.py  /
VOLUME ["/data"]
EXPOSE 5000
CMD [ "python", "./student_age.py" ]


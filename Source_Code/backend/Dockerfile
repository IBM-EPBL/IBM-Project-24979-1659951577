FROM python:3.10.8
WORKDIR /app

COPY ./requirements.txt ./server.py ./DigiCertGlobalRootCA.crt ./template.py ./
RUN pip install -r ./requirements.txt

EXPOSE 5000
CMD ["python", "./server.py"]

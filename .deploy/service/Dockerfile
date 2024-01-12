FROM python:3.8.10
WORKDIR /root

COPY requirements.txt .
RUN pip3 install -r requirements.txt

COPY wheels/ ./wheels
RUN pip3 install wheels/*

COPY src/ .

CMD ["python3", "main.py"]
EXPOSE 80
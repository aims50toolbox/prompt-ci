FROM python:3.8.10
WORKDIR /root

# git: for pip3 install from git
# pip: installing python packages
RUN apt update && \
        apt -y install \
                git \
                python3-pip 

# install aitoolbox support
RUN pip3 install git+https://github.com/aims50toolbox/aitoolbox.git


# install requirements (we ignore breaking system packages in docker container)
COPY requirements.txt .
RUN pip3 install -r requirements.txt

COPY src/ .

CMD ["python3", "main.py"]
EXPOSE 80
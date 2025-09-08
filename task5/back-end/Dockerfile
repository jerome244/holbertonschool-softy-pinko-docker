FROM ubuntu:latest
ENV DEBIAN_FRONTEND=noninteractive

# System deps
RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y python3 python3-pip \
    && rm -rf /var/lib/apt/lists/*

# Allow pip installs if environment is externally managed
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED || true

# Python deps
RUN pip3 install --no-cache-dir flask flask-cors

WORKDIR /app
COPY ./api.py /app/api.py

EXPOSE 5252
CMD ["python3", "api.py"]

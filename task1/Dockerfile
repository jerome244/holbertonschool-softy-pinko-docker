# task1/Dockerfile
FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive

# Update/upgrade and install Python + pip
RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y python3 python3-pip \
    && rm -rf /var/lib/apt/lists/*

# If Ubuntu uses the externally-managed policy, allow pip installs (per task note)
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED || true

# Install Flask via pip3 (NOT apt)
RUN pip3 install --no-cache-dir flask

# Use /app and copy the Flask app
WORKDIR /app
COPY ./api.py /app/api.py

# Optional: document container port
EXPOSE 5252

# Run the server
CMD ["python3", "api.py"]

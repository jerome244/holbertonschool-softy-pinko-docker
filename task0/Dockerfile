# task0/Dockerfile
FROM ubuntu:latest

# Prevent interactive prompts during apt operations
ENV DEBIAN_FRONTEND=noninteractive

# Update package lists and upgrade installed packages
RUN apt-get update \
    && apt-get upgrade -y \
    && rm -rf /var/lib/apt/lists/*

# When the container runs, print "Hello, World!"
CMD ["/bin/echo", "Hello, World!"]

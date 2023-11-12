# Start from a base image that has bash, e.g., Alpine
FROM alpine:latest

# Install bash if it's not included in the base image
RUN apk add --no-cache bash

# Copy the bash script into the container
COPY bin/my-cni-demo /usr/local/bin/my-cni-demo

# Copy the config file
COPY net.d/10-my-cni-demo.conf /etc/cni/net.d/10-my-cni-demo.conf

# Make the script executable
RUN chmod +x /usr/local/bin/my-cni-demo

# Use ubuntu:22.04 as a base image
FROM ubuntu:25.04

# Install curl into the image
RUN apt-get -y update; apt-get -y install curl
# RUN apt-get update && apt-get install -y curl

# Set a working directory
WORKDIR /usr/src/app

# Copy the script from the current directory 
# to the working directory inside the image
COPY script.sh .

# add execution permissions during the build.
RUN chmod +x script.sh

CMD [ "./script.sh" ]
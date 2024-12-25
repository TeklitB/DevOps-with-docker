# Use alpine as a base image, a small linux distribution with no fancy tools.
FROM alpine:3.21.0

# Use /usr/src/app as our workdir.
WORKDIR /usr/src/app

# Copy hello.sh from the current directory to /usr/src/app
COPY hello.sh .

# Add execution permissions during the build.
RUN chmod +x hello.sh

# When running docker run the command will be ./hello.sh
CMD [ "./hello.sh" ]

# Now we know that all instructions in a Dockerfile except CMD 
# are executed during build time. 
# CMD is executed when we call docker run, unless we overwrite it.
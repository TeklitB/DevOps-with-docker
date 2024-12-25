FROM ubuntu:25.04

WORKDIR /mydir

RUN apt-get update && apt-get install -y curl python3

RUN curl -L https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -o /usr/local/bin/yt-dlp

RUN chmod a+rx /usr/local/bin/yt-dlp

# Replace CMD with ENTRYPOINT
ENTRYPOINT ["/usr/local/bin/yt-dlp"]

# More suitable solution for the Major issue 
# We can use Docker volumes to make it easier to store the downloads outside the container's ephemeral storage. 
# With bind mount we can mount a file or directory from our own machine (the host machine) into the container.
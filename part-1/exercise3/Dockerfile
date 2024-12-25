FROM ubuntu:25.04

WORKDIR /mydir

RUN apt-get update && apt-get install -y curl python3

RUN curl -L https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -o /usr/local/bin/yt-dlp

RUN chmod a+rx /usr/local/bin/yt-dlp

# Replace CMD with ENTRYPOINT
ENTRYPOINT ["/usr/local/bin/yt-dlp"]

# Now we have two problems with the yt-dlp project:
# 1. Major: The downloaded files stay in the container
# 2. Minor: Our container build process creates many layers resulting in increased image size

# Simple solution for the Major issue 
# docker cp "5550fc4c4d6a:/mydir/Master’s Programme in Computer Science ｜ University of Helsinki [XsqlHHTGQrw].mp4" .
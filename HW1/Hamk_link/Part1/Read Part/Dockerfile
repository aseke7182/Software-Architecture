FROM ubuntu:16.04 

WORKDIR /mydir 
RUN touch hello.txt \
    && apt-get update \
    && apt-get install -y wget  \
    && apt-get install -y curl python \ 
    && curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl \
    && chmod a+x /usr/local/bin/youtube-dl 
ENV LC_ALL=C.UTF-8 
COPY local.txt . 
RUN wget http://example.com/index.html 
ENTRYPOINT ["/usr/local/bin/youtube-dl"] 
CMD ["/usr/local/bin/youtube-dl"]
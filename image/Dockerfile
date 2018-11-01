FROM alpine

# xicoria/kubectl

RUN apk add --update ca-certificates  && \
    apk add --update -t deps curl && \
    curl -L https://storage.googleapis.com/kubernetes-release/release/v1.10.0/bin/linux/amd64/kubectl -o /usr/local/bin/kubectl && \
    chmod +x /usr/local/bin/kubectl && \
    apk del --purge deps && \
    rm /var/cache/apk/*

CMD ["top"]

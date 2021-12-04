FROM node:alpine

WORKDIR /usr/src/app

RUN \
    echo "==> Install app..."                && \
    npm install -g --production json-server  && \
    \
    \
    echo "==> Remove unused temp..."         && \
    rm -rf /root/.npm                  \
           /usr/lib/node_modules/npm

EXPOSE 3000

WORKDIR /data

ENTRYPOINT ["json-server", "--host", "0.0.0.0"]
CMD ["--help"]


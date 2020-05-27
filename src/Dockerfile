FROM alpine:latest

COPY . /home/user
ADD . /home/user

ENV accessKeyId=AWS_ACCESS_KEY_ID
ENV secretAccessKey=AWS_SECRET_ACCESS_KEY
ENV sessionToken=AWS_SESSION_TOKEN
ENV region=AWS_DEFAULT_REGION

RUN apk add --no-cache nodejs npm && \
    adduser -D user && \
    npm install -g proxy-agent \
    cd /home/user/cloudsploit && \
    npm install -g /home/user/cloudsploit

USER user

# ENTRYPOINT ["tail", "-f", "/dev/null"]
ENTRYPOINT ["node", "/home/user/cloudsploit/index.js", "--csv=/tmp/out.csv"]

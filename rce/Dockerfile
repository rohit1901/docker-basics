FROM alpine

LABEL authors="rohit.khanduri"

RUN apk add --no-cache python3

CMD ["8.8.8.8"]

ENTRYPOINT ["ping", "-t", "5"]
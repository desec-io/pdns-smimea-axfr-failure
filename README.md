# AXFR Fails when many SMIMEA Records are Present

To start everything and see AXFR fail, use:

```shell script
docker-compose build && \
    docker-compose down -v && \
    docker-compose up -d && \
    sleep 3 && \
    docker-compose exec pdns bash /root/poc.sh && \
    echo "\n\n\n\n\n\n\n" && \
    dig example.com @127.0.0.1 -p 5300 AXFR
```

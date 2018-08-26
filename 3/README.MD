
docker build -t apache:ssl-ok 

docker run -d -p 443:443 apache:ssl-ok

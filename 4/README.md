imagen con Nginx y PHP-FPM


docker build -t test:1 .


docker run -d --name test1 -p 80:80 test:1

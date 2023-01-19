~ Используемые комманды ~

sudo docker run hello-world #Проверил работу Докера

sudo usermod -aG docker $USER #Дал права докеру

sudo chmod +666 /var/run/docker.sock #Дал права сокету

docker run -it --rm -d -p 8080:80 --name d_host nginx #Проверил работу nginx

docker stop d_host #Остановил работу nginx

docker build . --tag=image_host #Собрал кастомный образ на базе nginx

docker run -it --rm -d -p 8081:80 --name d_host image_host #Запустил и через curl проверил работоспособность

Всё работает, но в браузере изза кодировки сломались символы
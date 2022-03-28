# Simple Docker

## Part 1. Готовый докер.

* Взять официальный докер образ с nginx и выкачать его при помощи docker pull:

![dockerPull](Images/1.1.png "pull nginx")

* Проверить наличие докер образа через docker images:

![dockerImages](Images/1.2.png "docker images")

* Запустить докер образ через docker run -d [image_id|repository]:

![dockerRun](Images/1.3.png "docker run")

* Проверить, что образ запустился через docker ps:

![dockerPs](Images/1.4.png "docker ps")

* Посмотреть информацию о контейнере через docker inspect [container_id|container_name]:

1. Размер контейнера:

![sizeCont](Images/1.5.png "size of container")

2. Список замапленых портов:

![ports](Images/1.6.png "ports")

3. Ip контейнера:

![ipC](Images/1.7.png "container ip")

* Остановить докер образ через docker stop [container_id|container_name]:

![dockerStop](Images/1.8.png "docker stop")

* Проверить, что образ остановился через docker ps:

![dockerPs](Images/1.9.png "docker ps")

* Запустить докер с замапленными портами 80 и 443 на локальную машину через команду run:

![dockerPorts](Images/1.10.png "ports 80 and 443")

* Проверить, что в браузере по адресу localhost:80 доступна стартовая страница nginx:

![checknginx](Images/1.11.png "nginx")

* Перезапустить докер образ через docker restart [image_id|repository]:

![dockerRestart](Images/1.12.png "docker restart")

* Проверить любым способом, что контейнер запустился:

![dockerCheck](Images/1.13.png "docker ps")

## Part 2. Операции с контейнером.

* Прочитать конфигурационный файл nginx.conf внутри докер образа через команду exec:

![dockerExec](Images/1.14.png "nginx.conf")

* Создать на локальной машине файл nginx.conf. Настроить в нем по пути /status отдачу страницы статуса сервера nginx:

![nginxConf](Images/1.15.png "nginx.conf")

* Скопировать созданный файл nginx.conf внутрь докер образа через команду docker cp:

![copy](Images/1.16.png "nginx copy")

* Перезапустить nginx внутри докер образа через команду exec:

![reload](Images/1.17.png "nginx reload")

* Проверить, что по адресу localhost:80/status отдается страничка со статусом сервера nginx:

![status](Images/1.18.png "nginx status")

* Экспортировать контейнер в файл container.tar через команду export:

![export](Images/1.19.png "export")

* Остановить контейнер:

![stopContainer](Images/1.20.png "stop")

* Удалить образ через docker rmi [image_id|repository], не удаляя перед этим контейнеры:

![delete](Images/1.21.png "delete")

* Импортировать контейнер обратно через команду import:

![import](Images/1.22.png "import")

* Запустить импортированный контейнер:

![start](Images/1.23.png "start")

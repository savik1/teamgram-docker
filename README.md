# teamgram-docker
Проверял/запускал в Ubuntu 20.04 LTS.
По идее должен запуститься на любом более-менее свежем Linux OS

Проверка сервера: 
1. Запустить netstat -tupln: и проверить наличие открытого порта 10443 
2. Открыть в браузере IP_сервера:10443 
   Сервер сразу разорвет соединение и в логах появится запись об этом.
3. Скомпилировать, предварительно настроив Клиент. Более подробно тут:
   https://github.com/teamgram/teamgram-server/tree/master/clients
   (этот вариант не проверял)
   
## Установить docker: 
```
sudo apt install docker.io
```

## Установить docker-compose:
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```


## Склонировать: 
```
git clone https://github.com/savik1/teamgram-docker.git
cd teamgram-docker
```

## Запустить:
```
sudo docker-compose up -d
```

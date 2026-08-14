# Домашнее задание к занятию 5. «Практическое применение Docker»  
## Задача 0  
<img width="666" height="114" alt="Задача 0" src="https://github.com/user-attachments/assets/c5a49bc1-d3bc-4178-ae51-db2e16f013fc" />  
  
## Задача 1  
https://github.com/MikhailNikitin99/shvirtd-example-python  
  
### 1.2  
<img width="908" height="340" alt="Задача 1 2" src="https://github.com/user-attachments/assets/3addb2b3-ef97-4d09-b4f5-7a17842722dc" />  
  
### 1.2.1  
<img width="764" height="255" alt="Задача 1 2 1" src="https://github.com/user-attachments/assets/919b4ed5-b9ed-4c52-a666-783ee6dc9484" />  
  
### 1.3  
<img width="1514" height="517" alt="Задача 1 3" src="https://github.com/user-attachments/assets/6d1d8825-7aad-4874-885b-518874a88519" />  

<img width="895" height="331" alt="SQL в контейнере для локального запуска app" src="https://github.com/user-attachments/assets/84387c83-124c-43b7-85cb-533ee94bced2" />

  
### 1.4  
  
В комментариях и коде приложения и в .env форка  
export DB_TABLE_NAME=<...>  
  
## Задача 2

[Файл vulnerabilities.csv](https://github.com/MikhailNikitin99/redesigned-spoon/blob/main/vulnerabilities.csv)

## Задача 3  
  
<img width="673" height="156" alt="Задача 3" src="https://github.com/user-attachments/assets/8b82ebaa-ca4e-4624-9b03-23b06ce14a55" />  
  
### 3.4  
  
<img width="789" height="796" alt="Задача 3 3-4" src="https://github.com/user-attachments/assets/568c6433-5147-46cc-971a-f2806eea0004" />  
  
## Задача 4  

<img width="796" height="796" alt="Задача 4 Таблица SQL" src="https://github.com/user-attachments/assets/8ce98cfe-986d-46d8-a4c8-ce8e21f71e0a" />  

https://github.com/MikhailNikitin99/shvirtd-example-python  

## Задача 5
  
[Скрипт для создания бекапов](https://github.com/MikhailNikitin99/shvirtd-example-python/blob/main/mysql_backup.sh)  
  
```bash
#!/bin/bash
mkdir -p /opt/backup
DATE=$(date +"%Y%m%d_%H%M%S")
BACKUP_FILE="/opt/backup/mysqldump_${DATE}.sql"
docker run -d --rm --network shvirtd-example-python_backend --env-file /opt/shvirtd-example-python/.env schnitzler/mysqldump > "$BACKUP_FILE"
```  
  
<img width="1244" height="129" alt="Крон-задача дампа  БД Задача 5" src="https://github.com/user-attachments/assets/96cd490b-98c1-4b78-b5c1-5f20b81f325a" />  

## Задача 6  

<img width="1012" height="312" alt="Задача 6 1" src="https://github.com/user-attachments/assets/daf3af88-6880-408a-995c-ea660fda32e4" />  
  
<img width="1836" height="872" alt="Задача 6 dive" src="https://github.com/user-attachments/assets/df9eef14-5aaa-4d2f-80ae-4f2d9394f84a" />  

<img width="1827" height="540" alt="Задача 6 терраформ" src="https://github.com/user-attachments/assets/013af3b1-20f9-4170-9ecd-994740328a56" />
  
  
  
  
  
  
  
  
  
  
# Предыдущие задания
  
## 1 Задание
  
https://hub.docker.com/repository/docker/mikhailnikitin99/custom-nginx/general
  
## 2 Задание
  
<img width="1283" height="493" alt="2_задание" src="https://github.com/user-attachments/assets/b1ce6465-0fbf-4345-a438-e3f13e1de771" />

## 3 Задание
### c 1 по 6  
<img width="1285" height="250" alt="3_задние_1-6" src="https://github.com/user-attachments/assets/dc14d37e-c1bf-47a6-86d8-07a62f287bef" />

### Ответы на 3, 4, 11 вопросы:
3. Так как мы подключились к потоку контейнера, Ctrl+C послала сигнал прерывания этого потока, поэтому контейнер остановился.
4. Мы изменили порт nginx на 81, а контейнер так и остался на 80 и поэтому ss ничего не находила, а docker port показывал те, порты на которые он настроен(8080:80), также и curl ровно поэтому возвращал пустой ответ.
11. Остановил контейнер и сервис докера, затем заменил порты в конфигах контейнера(/var/lib/docker/containers/) hostconfig.json и config.v2.json на 81 в PortBindings и ExposedPorts соответственно. После этого запустил сервис и контейнер. При curl http://127.0.0.1:8080/index.html страница успешно отобразилась, т.е. маппинг докера успешно поменялся

### с 7 по 10  
<img width="741" height="400" alt="3_задание_7-10" src="https://github.com/user-attachments/assets/39f1cc5e-c02d-4e01-b3d5-aecb7f0b2237" />

### 11 и 12
<img width="1093" height="147" alt="3_задание_11" src="https://github.com/user-attachments/assets/d9263009-0c87-4d5f-b61a-3086a8a47c64" />

<img width="629" height="75" alt="3_задание_12" src="https://github.com/user-attachments/assets/5dbc8856-6bbd-4fec-8e91-34f0b6971da0" />

## 4 задание  

<img width="963" height="289" alt="4_задание" src="https://github.com/user-attachments/assets/90ee1341-8759-4f43-b6f0-3d65084f549e" />

## 5 задание
<img width="1280" height="406" alt="5_задание" src="https://github.com/user-attachments/assets/11f4f51b-f7af-47f9-9f4a-c7c33d75f4f2" />
<img width="399" height="197" alt="5_задание_2" src="https://github.com/user-attachments/assets/51e2ebc7-c3a4-49db-85c3-db8c0c9cda7b" />
<img width="827" height="629" alt="5_задание_3" src="https://github.com/user-attachments/assets/59736e8d-d46e-4800-b7ba-efa0cb89c4da" />
<img width="654" height="892" alt="5_задание_6" src="https://github.com/user-attachments/assets/76815d17-85b3-42d4-b748-423d4f4e4e51" />
<img width="1285" height="325" alt="5_задание_7" src="https://github.com/user-attachments/assets/84f0def2-e0df-417a-9a5b-c8e893edbf2c" />

### 7 вопрос
7. После удаления compose.yaml и docker compose up -d, вылетает предупреждение о том, что compose нашел контейнер-сироту в проекте (в моем случае это portainer), далее просто предложил --remove-orphans чтобы избавиться от него и при docker compose up -d --remove-orphans registry поднялся, а portainer был удален




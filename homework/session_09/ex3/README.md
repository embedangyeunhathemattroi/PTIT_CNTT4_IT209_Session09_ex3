# Bai 3 - Docker HTML Static Website

## Muc tieu
Dong goi trang web HTML tinh su dung Docker va Nginx Alpine.

## Dockerfile

FROM nginx:alpine
COPY index.html /usr/share/nginx/html/index.html

## Cac lenh thuc hien

### 1. Build Docker Image
docker build -t my-html-app:v1 .

### 2. Chay Container
docker run -d -p 8081:80 --name html-app my-html-app:v1

### 3. Kiem tra Container
docker ps

### 4. Kiem tra Website
curl.exe -s http://localhost:8081

## Ket qua mong doi

<h1>Hello Docker Session 09!</h1>

## Truy cap
http://localhost:8081

## Don dep
docker stop html-app
docker rm html-app

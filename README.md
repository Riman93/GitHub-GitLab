# GitHub-GitLab
# Лабораторная работа №5: Развертывание кластера Kubernetes и деплой приложения

## Название дисциплины
Облачные сервисы и технологии

## Название лабораторной работы
Создание кластера Kubernetes с использованием Minikube и деплой приложения

## ФИО и группа
Поспелов Роман Алексеевич
Группа: ОКБП-302вм

## Цель лабораторной работы
Освоить основы развертывания локального кластера Kubernetes с помощью Minikube, научиться деплоить приложение в кластер, масштабировать количество реплик и наблюдать балансировку нагрузки между подами.

## Манифесты

### deployment.yaml
```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: my-deployment
spec:
  replicas: 10
  selector:
    matchLabels:
      app: my-app
  template:
    metadata:
      labels:
        app: my-app
    spec:
      containers:
      - name: myapi
        image: myapi:latest
        imagePullPolicy: Never
        ports:
        - containerPort: 8080


Результаты выполнения
1. Проверка количества подов после масштабирования до 10 реплик (шаг 3.3) 
<img width="974" height="396" alt="5b7b1816-d7ae-4e63-991f-24df97fb9f3a" src="https://github.com/user-attachments/assets/8a10cf86-724c-4da5-8686-f942d25026da" />

<img width="974" height="396" alt="5b7b1816-d7ae-4e63-991f-24df97fb9f3a" src="https://github.com/user-attachments/assets/49a1cc4d-1d3f-46ef-b257-4399a1f5b7e4" />



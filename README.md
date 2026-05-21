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

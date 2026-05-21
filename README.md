<img width="974" height="396" alt="5b7b1816-d7ae-4e63-991f-24df97fb9f3a" src="https://github.com/user-attachments/assets/49a1cc4d-1d3f-46ef-b257-4399a1f5b7e4" />

<img width="974" height="548" alt="b9c53942-bead-4cb1-8b28-aa0dfccf8645" src="https://github.com/user-attachments/assets/500cd3e4-0764-4b6f-a8c9-d2fcf93cd4f4" />

<img width="974" height="490" alt="6f3538cd-de7f-4f5a-9977-9e5f61b3ffcc" src="https://github.com/user-attachments/assets/621809f1-a7a1-46ed-8fba-1755b0b2bc11" />

<img width="974" height="486" alt="7555d210-0fc0-47b4-8a85-593154f83583" src="https://github.com/user-attachments/assets/c8153437-9042-4ea4-8884-43a3b47a326a" />

<img width="974" height="489" alt="427c8103-013c-482c-9525-ee5d7e5e2470" src="https://github.com/user-attachments/assets/7e53b6c7-de19-4000-bae9-39ba6d083e06" />


<img width="974" height="493" alt="3d0c8b60-a130-4f97-ad8d-194823b06091" src="https://github.com/user-attachments/assets/38291dd9-447d-4d3b-92f6-9a681e73cd97" />

<img width="974" height="493" alt="447fb5fa-c9f8-48a0-846a-f94e5620ee3a" src="https://github.com/user-attachments/assets/2d824a12-f914-45ea-99f1-e06b0d212df4" />

<img width="974" height="489" alt="977b3ecc-b15f-4d5a-aec3-4e7e31ff9161" src="https://github.com/user-attachments/assets/b38ab958-ff44-4e19-9db4-9f87699bcdcc" />



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
фото 1-5

2. Графический интерфейс Kubernetes Dashboard с запущенными подами (шаг 3.5)
фото 6-8





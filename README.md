# 12.5_K8S_Aleksandr_Molokov

### Задание 1. Создать Deployment приложений backend и frontend

1. Создать Deployment приложения _frontend_ из образа nginx с количеством реплик 3 шт.
2. Создать Deployment приложения _backend_ из образа multitool. 
3. Добавить Service, которые обеспечат доступ к обоим приложениям внутри кластера. 
4. Продемонстрировать, что приложения видят друг друга с помощью Service.
5. Предоставить манифесты Deployment и Service в решении, а также скриншоты или вывод команды п.4.

### Ответ

### 1. ![Deployment frontend](https://github.com/ALEMOLOKOV/12.5_K8S_Aleksandr_Molokov/blob/4ae54bdb36d54103220266240e61e755844d3d90/deployment-frontend.yaml)

### 2. ![Deployment backend](https://github.com/ALEMOLOKOV/12.5_K8S_Aleksandr_Molokov/blob/4ae54bdb36d54103220266240e61e755844d3d90/deployment-backend.yaml)

### 3. Services
### ![Frontend](https://github.com/ALEMOLOKOV/12.5_K8S_Aleksandr_Molokov/blob/4ae54bdb36d54103220266240e61e755844d3d90/service-frontend.yaml)
### ![Backend](https://github.com/ALEMOLOKOV/12.5_K8S_Aleksandr_Molokov/blob/4ae54bdb36d54103220266240e61e755844d3d90/service-backend.yaml)

### 4. Проверка доступности приложений

#### Frontend

![curl frontend](https://github.com/ALEMOLOKOV/12.5_K8S_Aleksandr_Molokov/assets/109212419/33f8696d-64b2-45da-890f-3ac64f0f28ca)

#### Backend

![curl backend](https://github.com/ALEMOLOKOV/12.5_K8S_Aleksandr_Molokov/assets/109212419/8aba1a28-efe6-48a8-9d05-5f214620bcf3)

------

### Задание 2. Создать Ingress и обеспечить доступ к приложениям снаружи кластера

1. Включить Ingress-controller в MicroK8S.
2. Создать Ingress, обеспечивающий доступ снаружи по IP-адресу кластера MicroK8S так, чтобы при запросе только по адресу открывался _frontend_ а при добавлении /api - _backend_.
3. Продемонстрировать доступ с помощью браузера или `curl` с локального компьютера.
4. Предоставить манифесты и скриншоты или вывод команды п.2.

### Ответ

#### 1 Включение Ingress

![ingress enabled](https://github.com/ALEMOLOKOV/12.5_K8S_Aleksandr_Molokov/assets/109212419/deaa3150-dc8a-431a-a944-96f45c9664ad)

#### 2 ![Ingress](https://github.com/ALEMOLOKOV/12.5_K8S_Aleksandr_Molokov/blob/47daf71752058e1b55ce418b3d922ed3e317fc31/Ingress.yaml)

#### Доступ frontend

![frontend curl](https://github.com/ALEMOLOKOV/12.5_K8S_Aleksandr_Molokov/assets/109212419/822e96d3-72ea-41f2-a86c-13433dcaa4bd)

#### Доступ backend

![backend curl](https://github.com/ALEMOLOKOV/12.5_K8S_Aleksandr_Molokov/assets/109212419/506e1101-1fbb-43f2-ab6f-95425a0f6227)


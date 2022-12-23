# Дипломный практикум в Yandex.Cloud

## 1. Репозиторий с конфигурационными файлами Terraform и готовность продемонстрировать создание всех ресурсов с нуля.
https://github.com/aierohin/diplom_terraform
## 2. Пример pull request с комментариями созданными atlantis'ом или снимки экрана из Terraform Cloud.

![2022-12-13_16-05-59](https://user-images.githubusercontent.com/88886716/207345987-f9774bcb-ec9c-4f23-aaa8-67e375291bc2.png)
![2022-12-13_16-06-47](https://user-images.githubusercontent.com/88886716/207346050-687f9e80-7934-4f42-bcea-f0d431c055fe.png)
![2022-12-13_16-07-13](https://user-images.githubusercontent.com/88886716/207346117-eb26e68d-2348-47a0-9a9c-6149ed187b9e.png)
![2022-12-13_16-07-56](https://user-images.githubusercontent.com/88886716/207346184-513cf528-f2d3-4b2c-9c13-5bada56229e0.png)
![2022-12-13_16-09-14](https://user-images.githubusercontent.com/88886716/207346236-5a4f2485-374d-444f-ac0d-cbcb7880fd89.png)

## 3. Репозиторий с конфигурацией ansible, если был выбран способ создания Kubernetes кластера при помощи ansible.
https://github.com/aierohin/diplom_kubespray/tree/main
```
erohin@erohin-VirtualBox:~/diplom_netology/kubespray/inventory/diplom$ kubectl version 
WARNING: This version information is deprecated and will be replaced with the output from kubectl version --short.  Use --output=yaml|json to get the full version.
Client Version: version.Info{Major:"1", Minor:"25", GitVersion:"v1.25.4", GitCommit:"872a965c6c6526caa949f0c6ac028ef7aff3fb78", GitTreeState:"clean", BuildDate:"2022-11-09T13:36:36Z", GoVersion:"go1.19.3", Compiler:"gc", Platform:"linux/amd64"}
Kustomize Version: v4.5.7
Server Version: version.Info{Major:"1", Minor:"25", GitVersion:"v1.25.4", GitCommit:"872a965c6c6526caa949f0c6ac028ef7aff3fb78", GitTreeState:"clean", BuildDate:"2022-11-09T13:29:58Z", GoVersion:"go1.19.3", Compiler:"gc", Platform:"linux/amd64"}
erohin@erohin-VirtualBox:~/diplom_netology/kubespray/inventory/diplom$ kubectl get nodes
NAME          STATUS   ROLES           AGE   VERSION
node-cp       Ready    control-plane   31m   v1.25.4
node-work-1   Ready    <none>          29m   v1.25.4
node-work-2   Ready    <none>          29m   v1.25.4
erohin@erohin-VirtualBox:~/diplom_netology/kubespray/inventory/diplom$ 
```

## 4. Репозиторий с Dockerfile тестового приложения и ссылка на собранный docker image.
https://github.com/aierohin/diplom_nginx
https://hub.docker.com/layers/aierohin/nginx/latest/images/sha256-a255fa03c084576ac5a02e98e16d0b44c5cb2aa23fbdd755b465f7a2eba98ea5?context=repo

## 5. Репозиторий с конфигурацией Kubernetes кластера.
https://github.com/aierohin/diplom_kubernetes

## 6. Ссылка на тестовое приложение и веб интерфейс Grafana с данными доступа.
Приложение:  
http://158.160.33.134:30001/

Grafana:  
http://158.160.33.134:31596
Login - netology, password - netology.

## 7. Описание CI/CD  
Доступ к Jenkins  
http://51.250.88.172:8080    
Логин - netology, пароль - netology.  
Конфиг Jenkins - https://github.com/aierohin/diplom_final/blob/main/Jenkins_config.xml  
Конфиг job - https://github.com/aierohin/diplom_final/blob/main/Job_config.xml  

В репозитории https://github.com/aierohin/diplom_nginx настроен webhook:  

![2022-12-23_19-04-41](https://user-images.githubusercontent.com/88886716/209364898-53ede1de-0af0-46e8-8da0-7a83bd776866.png)  

Когда в репозитории происходит commit webhook триггерит джобу Jenkins:  

![2022-12-23_19-07-57](https://user-images.githubusercontent.com/88886716/209365230-14ae6270-c223-447a-b7df-acde6092a4bb.png)  

В настройках джобы указан целевой репозиторий, поэтому будет срабатывать необходимая нам джоба:  

![2022-12-23_19-09-51](https://user-images.githubusercontent.com/88886716/209365602-962b8f52-1f32-4481-bee0-81e003c61166.png)  
![2022-12-23_19-11-19](https://user-images.githubusercontent.com/88886716/209365618-2ae65cb5-1f15-49b1-8c65-a54fd036b8c4.png)  

Описание действий, которые будут выполняться, находятся в Jenkinsfile, который в том же репозитории https://github.com/aierohin/diplom_nginx/blob/main/Jenkinsfile  



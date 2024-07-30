# Домашнее задание к занятию «Управление доступом в k8s» - Сергей Ситкарёв

## Задание 1. Создайте конфигурацию для подключения пользователя

Создайте и подпишите SSL-сертификат для подключения к кластеру.

![Задание1](https://github.com/SSitkarev/2.4-k8s-permissions/blob/main/img/1.jpg)

Настройте конфигурационный файл kubectl для подключения.

Создайте роли и все необходимые настройки для пользователя.

Предусмотрите права пользователя. Пользователь может просматривать логи подов и их конфигурацию (kubectl logs pod <pod_id>, kubectl describe pod <pod_id>).

[deployment](https://github.com/SSitkarev/2.4-k8s-permissions/blob/main/src/deployment.yaml)

[role](https://github.com/SSitkarev/2.4-k8s-permissions/blob/main/src/role.yaml)

[rolebinding](https://github.com/SSitkarev/2.4-k8s-permissions/blob/main/src/rolebinding.yaml)

С правами нашего пользователя (user) мы имеем доступ на листинг pod-ов в заданном namespace, а в default, например, доступа нет.

![Задание1](https://github.com/SSitkarev/2.4-k8s-permissions/blob/main/img/2.jpg)

Так же имеем доступ на чтение логов pod-ов из заданного namespace

![Задание1](https://github.com/SSitkarev/2.4-k8s-permissions/blob/main/img/3.jpg)
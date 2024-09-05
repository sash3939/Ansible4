# Домашнее задание к занятию 4 «Работа с roles»

## Подготовка к выполнению

1. * Необязательно. Познакомьтесь с [LightHouse](https://youtu.be/ymlrNlaHzIY?t=929).
2. Создайте два пустых публичных репозитория в любом своём проекте: vector-role и lighthouse-role.
   Выполнено
3. Добавьте публичную часть своего ключа к своему профилю на GitHub.

   <img width="233" alt="Screen1-ssh" src="https://github.com/user-attachments/assets/a9d8648c-e243-4e7f-94e2-af5e55898b98">


## Основная часть

Ваша цель — разбить ваш playbook на отдельные roles. 

Задача — сделать roles для ClickHouse, Vector и LightHouse и написать playbook для использования этих ролей. 

Ожидаемый результат — существуют три ваших репозитория: два с roles и один с playbook.

**Что нужно сделать**

1. Создайте в старой версии playbook файл `requirements.yml` и заполните его содержимым:

   ```yaml
   ---
     - src: git@github.com:AlexeySetevoi/ansible-clickhouse.git
       scm: git
       version: "1.13"
       name: clickhouse 
   ```

2. При помощи `ansible-galaxy` скачайте себе эту роль.

   <img width="407" alt="Screen2" src="https://github.com/user-attachments/assets/db5d5044-1d2c-4794-921e-42d1b2c5daa2">

3. Создайте новый каталог с ролью при помощи `ansible-galaxy role init vector-role`.

   <img width="431" alt="Screen3" src="https://github.com/user-attachments/assets/559b609a-ec0a-45aa-b007-f05ae98fcc41">

4. На основе tasks из старого playbook заполните новую role. Разнесите переменные между `vars` и `default`.

   <img width="659" alt="Screen4" src="https://github.com/user-attachments/assets/20719490-4770-4360-9f36-fb62ddbaf70f">
  
5. Перенести нужные шаблоны конфигов в `templates`.

   <img width="407" alt="Screen5" src="https://github.com/user-attachments/assets/9df480d4-329c-4c2e-ba19-1e7856af6efb">

6. Опишите в `README.md` обе роли и их параметры. Пример качественной документации ansible role [по ссылке](https://github.com/cloudalchemy/ansible-prometheus).

   https://github.com/sash3939/lighthouse-role/blob/main/README.md

   https://github.com/sash3939/vector-role/blob/main/README.md
   
7. Повторите шаги 3–6 для LightHouse. Помните, что одна роль должна настраивать один продукт.
8. Выложите все roles в репозитории. Проставьте теги, используя семантическую нумерацию. Добавьте roles в `requirements.yml` в playbook.

   <img width="344" alt="Screen8" src="https://github.com/user-attachments/assets/88c9a8b7-9893-4cc8-a4c7-b7b2c821b63d">

9. Переработайте playbook на использование roles. Не забудьте про зависимости LightHouse и возможности совмещения `roles` с `tasks`.
10. Выложите playbook в репозиторий.
11. В ответе дайте ссылки на оба репозитория с roles и одну ссылку на репозиторий с playbook.

https://github.com/sash3939/Ansible4  - playbook
---

https://github.com/sash3939/lighthouse-role - lighthouse
---

https://github.com/sash3939/vector-role - vector
---

---

### Как оформить решение задания

Выполненное домашнее задание пришлите в виде ссылки на .md-файл в вашем репозитории.

---

# solid-fortnight 2.7

Что такое удалённый репозиторий?
Удалённый репозиторий — это версия вашего репозитория, которая хранится в интернете или на сервере. Он позволяет:
- Хранить ваш код в безопасном месте.
- Работать над проектом совместно с другими людьми.
- Получать доступ к проекту с разных устройств.

 Локальный репозиторий — это как рабочий стол, на котором вы пишете заметки. Удалённый репозиторий — это ваш онлайн-блокнот, доступный вам и вашим коллегам.


# Добавление удалённого репозитория: git clone <URL-репозитория>

<URL-репозитория> — адрес репозитория на платформе (например, на GitHub).

### Пример
- Создайте удалённый репозиторий на GitHub по инструкции.
- Получите ссылку на репозиторий (HTTPS). Например:
 https://github.com/username/my-project.git

- Добавьте репозиторий:
 git clone https://github.com/username/my-project.git


# Отправка изменений на удалённый репозиторий: git push

git push


Подготовьте локальные изменения:

- git add .
- git commit -m "Первый коммит"


- Отправьте их на удалённый репозиторий:

 git push

👉 Теперь ваш локальный код загружен в удалённый репозиторий.



# Получение изменений из удалённого репозитория: git pull

git pull - Получает последние изменения из удалённого репозитория и объединяет их с вашей локальной веткой.

Представьте, что ваш коллега добавил новый файл в репозиторий.
Вы хотите синхронизировать свой локальный репозиторий. Для этого выполните:
 git pull
 👉 Новые изменения будут загружены и объединены с вашей локальной веткой.

## Как запомнить разницу между pull и push?
🔻 git pull — тянет (pull) изменения с сервера на твой компьютер.
📥 Представь, что ты тянешь код вниз из удалённого репозитория (GitHub) в свой локальный проект.

🔺 git push — отправляет (push) изменения с твоего компьютера на сервер.
📤 Представь, что ты толкаешь код вверх, загружая свои изменения в удалённый репозиторий.

# Синхронизация изменений: git fetch и git diff

git fetch

- Загружает изменения из удалённого репозитория, но не объединяет их с локальной веткой.

git diff 

- Позволяет узнать, что нового появилось в удалённом репозитории, прежде чем обновлять локальный код.

git diff main origin/main

## Что дальше

- Хотите принять изменения с сервера?
    → git pull origin main
- Есть локальные изменения?
    → git add . && git commit -m "Сохранение перед pull"
    → затем git pull origin main
- Хотите вручную объединить изменения?
    → git merge origin/main
    ⚠️ Если возникнут конфликты, Git попросит вас их исправить вручную.
- Хотите отклонить изменения на сервере и оставить свои?
    → git push origin main --force
    ⚠️ Внимание! --force удалит изменения на сервере, так что убедитесь, что вы действительно хотите это сделать.



## Разница между git pull и git fetch + git merge origin/main
Команда	                Что делает?

git pull	            Автоматически загружает (fetch) и объединяет (merge) изменения.
git fetch	            Только загружает изменения, но не объединяет их.
git merge origin/main	После git fetch вручную объединяет (merge) изменения.

# vk-coinsbot-roulette
В основе бота - рулеточный алгоритм. Работает одновременно в разных беседах. Присутствует генерация картинок победителя и последних взносов.

Для начала работы бота необходимо наполнить конфигурационный файл conf.conf:
```
vk_group_access_token = 'xxx' # VK COIN Токен
vk_coins_token = 'xxx' # Токен сообщества ВК с доступом к сообщениям группы, фотографиям и документам.
vk_owner_id = 425340743 # ID Вконтакте того кому принадлежит токен vk coin (владельца счета), он будет главным администратором и тем, кто может создавать новые беседы с этим ботом!
vk_group_id = 137556985 # ID Сообщества в котором бот будет работать
procent_count = 10 # Процент, который будет братся из выигрыша в каждом розыгрыше и идти к вам в кассу
```
# Настройки для подключения к MySQL
```
db_host = '' # Адресс БД, например localhost
db_user = '' # Пользователь БД
db_passwd = '' # Пароль БД
db_name = '' # Имя БД
```

Файл с нужными таблицами лежит в репрезитории и называется db.sql

Чтобы инициализировать новую беседу (комнату), небходимо добавить сообщество с включенным ботом в нужную беседу, дать права администратора беседы и написать любое сообщение, после чего вы увидите клавиатуру и следующий текст:

```
Новая комната инициализирована!
Установлена дефолтная минимальная ставка: 1000
Команда для установки минимальной ставки: 'минимальная ставка (число)'
Команда доступна только для администратора (vk_owner_id).
```
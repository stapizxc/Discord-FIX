# Обход блокировки Discord'а и Youtube'а

## Гайд
Скачайте последний [релиз](https://github.com/stapizxc/Discord-FIX/releases), разархивируйте в отдельную папку

Запустите **от имени администратора** то, что вам нужно:

- **`discord.bat`** - запустить обход дискорда
- **`general.bat`** - запустить обход дискорда и ютуба
##
- **`service_discord.bat`** - запустить обход дискорда и поставить на автозапуск (в сервисах)
- **`service_discord_youtube.bat`** - запустить обход дискорда и ютуба и поставить на автозапуск (в сервисах)
##
- **`service_goodbye_discord.bat`** - запустить, если вы используете **СЕРВИС goodbyedpi**, и хотите, чтобы zapret обходил **только discord**. ВНИМАНИЕ: Запускать ПОСЛЕ создания сервиса goodbyedpi. Первый раз goodbyedpi может вылететь - просто перезапустите устройство!
##
- **`service_remove.bat`** - остановить и удалить сервисы выше

# Остановка и удаление обхода
Для этого запустите service_remove.bat.

Если WinDivert так и не удалился, узнайте его название с помощью команды driverquery | find "Divert" в cmd, а затем удалите данными командами (заместо WinDivert введите название, которые вы узнали):
**`sc stop WinDivert`**
**`sc delete WinDivert`**

## Не работает?
- Проверьте, запускаете ли вы файлы от имени администратора
- Не работает сервис? Проверьте, чтобы в пути до файла **не было пробелов** и русских символов. Также отключите программы, которые могут мешать созданию сервиса *(Антивирусы, клинеры с доп. защитой)*
- Не работает вместе с VPN? Отключите функцию **TUN** (Tunneling) в настройках VPN
- Не работает `service_goodbye_discord`? Удостовертесь, что сервис goodbyedpi запущен и имеет название GoodbyeDPI. После снова запустите `service_goodbye_discord.bat` и перезапустите устройство
- Попробуйте обновить бинарники с оригинального репозитория

### Дополнительные адреса заблокированных сайтов можно добавить в список list-general.txt (для `*discord_youtube`). После добавления сервис нужно перезапустить

### Оригинальный репозиторий
Credits to https://github.com/bol-van/zapret/tree/master/binaries/win64/zapret-winws

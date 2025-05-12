# OpenVPN Installer / Установщик OpenVPN

![Bash](https://img.shields.io/badge/Shell-Bash-blue)
![Jenkins](https://img.shields.io/badge/CI-Jenkins-red)
![Git](https://img.shields.io/badge/Git-Enabled-green)
![Linux](https://img.shields.io/badge/OS-Linux-yellow)
![SSH](https://img.shields.io/badge/Access-SSH-lightgrey)
![VPN](https://img.shields.io/badge/Security-VPN-darkgreen)
![Networking](https://img.shields.io/badge/Networking-L3%2FL4-blueviolet)

# OpenVPN Installer / Установщик OpenVPN 🌐🔒

![Bash](https://img.shields.io/badge/Shell-Bash-blue)
![Jenkins](https://img.shields.io/badge/CI-Jenkins-red)
![Git](https://img.shields.io/badge/Git-Enabled-green)
![Linux](https://img.shields.io/badge/OS-Linux-yellow)
![SSH](https://img.shields.io/badge/Access-SSH-lightgrey)
![VPN](https://img.shields.io/badge/Security-VPN-darkgreen)
![Networking](https://img.shields.io/badge/Networking-L3%2FL4-blueviolet)

## Ворвись в свободный интернет! 🚀

Интернет в 2025 году — это лабиринт с кучей закрытых дверей. YouTube заблокирован? Авиабилеты стоят как космический шаттл? 😤 Хватит это терпеть! Этот скрипт разворачивает OpenVPN-сервер за минуту на Ubuntu, Debian, CentOS, Fedora и других Linux-дистрибутивах. Никаких подписок, никакой возни — только ты и твой личный туннель в интернет без границ. Готов стать ниндзя интернета? 🥷

> Я смотрел заблокированный ролик, пока кофе остывал, и всё без единого лага. Попробуй и ты!

## 📚 Полезные материалы

- [Как настроить свой VPN за минуту и зачем это нужно: от YouTube до экономии на авиабилетах](https://vc.ru/id4876399/1980432-kak-bystro-nastroit-vpn) — статья на vc.ru с лайфхаками и подробностями.

## 🌟 Почему это круто

OpenVPN — это швейцарский нож для интернета: надёжный, универсальный и даёт тебе полный контроль. Но настройка VPN обычно похожа на сборку мебели из IKEA без инструкции. 😩 Этот скрипт меняет правила:

- **Скорость**: Установка одной командой. ⚡
- **Гибкость**: Работает на Ubuntu, Debian, CentOS, Fedora и других. 🐧
- **Безопасность**: Шифрование SHA512 и поддержка IPv6. 🔒
- **Свобода**: Ты сам себе админ, никаких коммерческих VPN. 🕊️

## 🎯 Где пригодится твой VPN

### 1. Смотри YouTube без блокировок 🎥
Географические ограничения — как заборы в интернете. Свой VPN-сервер — туннель под ними. Разверни сервер в стране без цензуры (например, в Европе), подключись — и вуаля, YouTube снова твой! Проверено: видео грузятся без тормозов, а цензура остаётся за горизонтом.

### 2. Экономь на авиабилетах и подписках ✈️
Почему билеты из России стоят как подержанная "Лада"? Сайты вроде Aviasales или Booking подстраивают цены под твою страну. С VPN ты "переезжаешь" в Индию или Аргентину, где билеты на 20-30% дешевле. То же с Netflix и Spotify — мой друг сэкономил 5000 рублей на подписке! 😎

### 3. Будь в безопасности в Wi-Fi 🔐
Общественные Wi-Fi в кафе, аэропортах или коворкингах — минное поле для твоих паролей. VPN шифрует трафик, так что хакеры видят только бессмысленный набор символов. Это как отправить письмо в сейфе, а не на открытке.

## 🔍 Как работает скрипт: под капотом

Этот bash-скрипт — твой личный мастер по установке OpenVPN. Он делает всё за тебя:

- **Проверяет окружение** 🛠️: Убеждается, что ты на bash и ОС поддерживается (Ubuntu 22.04+, Debian 11+, CentOS 9+, Fedora).
- **Выбирает IP и протокол** 🌐: Определяет IPv4/IPv6, предлагает UDP (быстрее) или TCP (надёжнее).
- **Настраивает DNS** 📡: Поддерживает Google, Cloudflare, OpenDNS или твои серверы.
- **Генерирует сертификаты** 🔑: Использует EasyRSA для ключей с шифрованием SHA512.
- **Настраивает файрвол** 🛡️: Открывает порты и включает NAT.
- **Создаёт .ovpn файл** 📄: Готовый конфиг для твоих устройств.

Код надёжен, как швейцарские часы: обрабатывает ошибки, поддерживает SELinux и работает в контейнерах. Вот фрагмент, который создаёт конфигурацию сервера:

```bash
echo "local $ip
port $port
proto $protocol
dev tun
ca ca.crt
cert server.crt
key server.key
dh dh.pem
auth SHA512
tls-crypt tc.key
topology subnet
server 10.8.0.0 255.255.255.0" > /etc/openvpn/server/server.conf

Это сердце твоего VPN, где задаются шифрование, порт и подсеть.
⚙️ Быстрый старт
Готов запустить свой сервер? 🚀 Вот пошаговый план:

Арендуй VPS ☁️: Подойдут DigitalOcean, Hetzner или AWS (от $5/месяц).
Подключись по SSH 🖥️: Используй терминал (Linux/Mac) или PuTTY (Windows).
Выполни команду 📋:

sudo apt-get update && \
sudo apt-get install -y git && \
cd /root && \
git clone https://github.com/admin404nextfloor/vpn.git && \
cd vpn && \
chmod +x openvpn.sh && \
./openvpn.sh

Или в одну строку:
sudo apt-get update && apt-get install -y git && cd /root && git clone https://github.com/admin404nextfloor/vpn.git && cd vpn && chmod +x openvpn.sh && ./openvpn.sh


Ответь на вопросы ❓: Выбери IP, протокол (UDP — топ), порт (обычно 1194) и DNS.
Скачай .ovpn 📥: Найдёшь в /root/vpn. Перенеси на своё устройство.
Подключись 🔗: Установи OpenVPN-клиент (Windows, macOS, Android, iOS), импортируй .ovpn и наслаждайся.

Всё! Ты в интернете без границ! 🌍
💡 Почему стоит попробовать
Этот скрипт — твой пропуск в свободный интернет. Забудь про коммерческие VPN, которые глючат или дерут три шкуры. Ты сам себе босс, а твой сервер — твой туннель в мир без цензуры. Хочешь смотреть YouTube, сэкономить на билетах или быть неуловимым, как хакер из фильмов? 😎 Качай код, пробуй и делись впечатлениями!

=




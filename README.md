# OpenVPN Installer / Установщик OpenVPN

Скрипт автоматической установки OpenVPN сервера на Ubuntu, Debian, AlmaLinux, Rocky Linux, CentOS и Fedora

Этот скрипт позволит вам настроить свой собственный VPN-сервер не более чем за минуту, даже если вы раньше не использовали OpenVPN. Он был разработан так, чтобы быть максимально незаметным и универсальным.

## 🚀 Быстрый старт

Скопируйте и вставьте в терминал:

```bash
sudo apt-get update && sudo apt-get install -y git && cd /root && sudo git clone [https://github.com/admin404nextfloor/vpn.git](https://github.com/admin404nextfloor/vpn.git) && cd vpn && sudo chmod +x openvpn.sh && sudo ./openvpn.sh ```



⚙️ После установки
📂 Перенос конфигурационного файла клиента
Скопируйте файл /root/vpn/client.ovpn на устройство, с которого вы хотите подключиться к VPN. Используйте scp, SFTP или другой удобный способ.

📲 Установка клиента OpenVPN
Установите клиентское приложение OpenVPN на своем устройстве:

# Linux (Debian/Ubuntu)
sudo apt-get install openvpn

# Linux (CentOS/Fedora/RHEL)
sudo yum install openvpn


Windows: Скачайте с официального сайта OpenVPN.
macOS: Скачайте с официального сайта OpenVPN.
Android/iOS: Найдите "OpenVPN Connect" в Google Play Store или App Store.

Выдать вам файл для скачивания напрямую я не могу, так как я являюсь текстовой моделью и не имею возможности работать с файловой системой вашего компьютера.

Однако, я могу предоставить вам содержимое файла README в формате Markdown, которое вы сможете скопировать и сохранить в файл с именем README.md на вашем компьютере.

Вот содержимое файла README.md:

Markdown

# OpenVPN Installer / Установщик OpenVPN

Скрипт автоматической установки OpenVPN сервера на Ubuntu, Debian, AlmaLinux, Rocky Linux, CentOS и Fedora

Этот скрипт позволит вам настроить свой собственный VPN-сервер не более чем за минуту, даже если вы раньше не использовали OpenVPN. Он был разработан так, чтобы быть максимально незаметным и универсальным.

## 🚀 Быстрый старт

Скопируйте и вставьте в терминал:

```bash
sudo apt-get update && sudo apt-get install -y git && cd /root && sudo git clone [https://github.com/admin404nextfloor/vpn.git](https://github.com/admin404nextfloor/vpn.git) && cd vpn && sudo chmod +x openvpn.sh && sudo ./openvpn.sh
⚙️ После установки
📂 Перенос конфигурационного файла клиента
Скопируйте файл /root/vpn/client.ovpn на устройство, с которого вы хотите подключиться к VPN. Используйте scp, SFTP или другой удобный способ.

📲 Установка клиента OpenVPN
Установите клиентское приложение OpenVPN на своем устройстве:

Bash

# Linux (Debian/Ubuntu)
sudo apt-get install openvpn

# Linux (CentOS/Fedora/RHEL)
sudo yum install openvpn
Windows: Скачайте с официального сайта OpenVPN.
macOS: Скачайте с официального сайта OpenVPN.
Android/iOS: Найдите "OpenVPN Connect" в Google Play Store или App Store.
🔑 Импорт конфигурации и подключение
Запустите клиентское приложение OpenVPN.
Импортируйте файл client.ovpn.
Используйте импортированный профиль для подключения к вашему VPN-серверу.
🗑️ Удаление OpenVPN (с файлами и программами)
Если вы захотите полностью удалить OpenVPN, все сгенерированные файлы конфигурации и установленные пакеты, выполните следующую команду:

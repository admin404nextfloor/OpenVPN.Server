
# OpenVPN Installer /Установщик OpenVPN

Скрипт автоматической установки OpenVPN сервера на Ubuntu, Debian, AlmaLinux, Rocky Linux, CentOS и Fedora

Этот скрипт позволит вам настроить свой собственный VPN-сервер не более чем за минуту, даже если вы раньше не использовали OpenVPN. Он был разработан так, чтобы быть максимально незаметным и универсальным.

## 🚀 Быстрый старт

Скопируйте и вставьте в терминал:

```bash
sudo apt-get update && apt-get install -y git && cd /root && git clone https://github.com/admin404nextfloor/vpn.git && cd vpn && chmod +x openvpn.sh && ./openvpn.sh



После установки
Скопируйте конфигурационный файл клиента: Перенесите файл /root/vpn/client.ovpn на устройство, с которого вы хотите подключиться к VPN. Вы можете использовать scp, SFTP или любой другой удобный для вас способ.
Установите клиент OpenVPN: Установите клиентское приложение OpenVPN на своем устройстве.
Linux: sudo apt-get install openvpn (Debian/Ubuntu) или sudo yum install openvpn (CentOS/Fedora/RHEL).
Windows: Скачайте с официального сайта OpenVPN.
macOS: Скачайте с официального сайта OpenVPN.
Android/iOS: Найдите "OpenVPN Connect" в Google Play Store или App Store.
Импортируйте конфигурационный файл: Запустите клиентское приложение OpenVPN и импортируйте файл client.ovpn.
Подключитесь к VPN: Используйте импортированный профиль для подключения к вашему VPN-серверу.


Удаление OpenVPN (с файлами и программами)
Если вы захотите полностью удалить OpenVPN, все сгенерированные файлы конфигурации и установленные пакеты, выполните следующую команду:

```bash
sudo systemctl stop openvpn-server@server.service && sudo systemctl disable openvpn-server@server.service && sudo systemctl stop openvpn.service && sudo systemctl disable openvpn.service && sudo systemctl stop openvpn-iptables.service && sudo systemctl disable openvpn-iptables.service && sudo apt-get remove --purge -y openvpn libpkcs11-helper1 git git-man liberror-perl && sudo apt-get autoremove -y && sudo rm -rf /etc/openvpn /root/vpn

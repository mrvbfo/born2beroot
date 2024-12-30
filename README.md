# born2beroot
## Genel Yönergeler
1. iTerm'i açın ve yazın`cd`
2. Sonra yazın`cd sgoinfre/students/<your_intra_username>/<file of your VM>`
3. Daha sonra şunu yazın `shasum VirtualBox.vdi` (veya VM'nizin .vdi uzantılı herhangi bir adı)

## Zorunlu Bölüm
cd /usr/local/bin
sudo crontab -u root -e 
1. uname -v
2. uname -a

sudo systemctl status apparmor

## Basit Yapılandırma
2. sudo systemctl status ufw 
4. sudo systemctl status ssh 

## Kullanıcı
1. id <username> --> kullanı bilgilerini gösterir 
2. cat /etc/passwd | grep home --->  Linux sistemindeki kullanıcı hesap bilgilerini içeren bir dosyayı (/etc/passwd) görüntüler ve Görüntülenen satırlar arasından "home" kelimesini içerenleri seçer.
4. getent group sudo
5. getent group user42
6. sudo adduser  <new_username> → kullanıcı oluşturulur ve şifre seçilir
7. sudo vim /etc/login.defs (burada max days 30, min days 2, warn 7 olarak ayalanır)
8. sudo vim /etc/pam.d/common-password -> katı şifreleme politikalarını belirleyen dosya 
9. sudo groupadd evaluating
10. cat /etc/group | grep evaluating (kurulan grubu gör)
11. sudo usermod -aG evaluating <username>
12. groups <username>

cat /etc/group

## HOST
1. sudo hostnamectl
2. sudo hostnamectl set-hostname <new_hostname>
3. sudo nano /etc/hosts
4. sudo reboot
5. sudo hostnamectl
6. lsblk

## SUDO
1. sudo --version
2. usermod -aG sudo <username>
3. groups username
4. sudo visudo
5. sudo vim /etc/sudoers
6. cd /var/log/sudo
7. ls 
8. cat sudo.log
9. sudo ls
10. cat sudo.log

## UFW / Güvenlik Duvarı
1. dpkg -l | grep ufw –
2. sudo systemctl status ufw
3. sudo ufw status numbered
4. sudo ufw allow 8080
5. sudo ufw status numbered
6. sudo ufw delete <rule_number>

## SSH
1. dpkg -l | grep ssh –    sudo ssh -V
2. sudo service ssh status
3. ssh root@localhost -p 4242 (root olarak dene ve kabul edilmediğini göster)
4. ssh <username>@localhost -p 22 (22 portundan dene ve kabul edilmediğini göster)
5. ssh username@localhost -p 4242 (giriş sağla yeni oluşturulan kullanıcı ile)
   

sudo systemctl restart keyboard-setup.service ---- türkçe klavye

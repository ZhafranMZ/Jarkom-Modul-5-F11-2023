# Jarkom-Modul-5-F11-2023

# Subnet List

|Subnet|Network ID|Hosts|Subnet Mask|
|-|-|-|-|
|A1|10.57.0.0|2|/30|
|A2|10.57.0.4|2|/30|
|A3|10.57.0.16|2|/30|
|A4|10.57.0.128|66|/25|
|A5|10.57.8.0|1023|/21|
|A6|10.57.4.0|514|/22|
|A7|10.57.0.20|2|/30|
|A8|10.57.2.0|256|/23|
|A9|10.57.0.24|2|/30|
|A10|10.57.0.28|2|/30|


# Network Configuration
- Aura
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 10.57.0.1
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.57.0.5
	netmask 255.255.255.252

```

- ### Heiter
```
auto eth0
iface eth0 inet static
	address 10.57.0.2
	netmask 255.255.255.252
	gateway 10.57.0.1

auto eth1
iface eth1 inet static
	address 10.57.8.1
	netmask 255.255.248.0

auto eth2
iface eth2 inet static
	address 10.57.4.1
	netmask 255.255.252.0

```

- ### Frieren
```
auto eth0
iface eth0 inet static
	address 10.57.0.6
	netmask 255.255.255.252
	gateway 10.57.0.5

auto eth1
iface eth1 inet static
	address 10.57.0.17
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.57.0.21
	netmask 255.255.255.252

```

- ### Himmel
```
auto eth0
iface eth0 inet static
	address 10.57.0.18
	netmask 255.255.255.252
	gateway 10.57.0.17

auto eth1
iface eth1 inet static
	address 10.57.0.129
	netmask 255.255.255.128

auto eth2
iface eth2 inet static
	address 10.57.2.1
	netmask 255.255.254.0

```

- ### Fern
```
auto eth0
iface eth0 inet static
	address 10.57.0.130
	netmask 255.255.255.128
	gateway 10.57.0.129

auto eth1
iface eth1 inet static
	address 10.57.0.29
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.57.0.25
	netmask 255.255.255.252

```

- ### TurkRegion
```
auto eth0
iface eth0 inet static
	address 10.57.8.2
	netmask 255.255.248.0
	gateway 10.57.8.1

```

- ### Sein
```
auto eth0
iface eth0 inet static
	address 10.57.4.2
	netmask 255.255.252.0
	gateway 10.57.4.1

```

- ### GrobeForest
```
auto eth0
iface eth0 inet static
	address 10.57.4.3
	netmask 255.255.252.0
	gateway 10.57.4.1

```

- ### Stark
```
auto eth0
iface eth0 inet static
	address 10.57.0.22
	netmask 255.255.255.252
	gateway 10.57.0.21

```

- ### SchewerMountain
```
auto eth0
iface eth0 inet static
	address 10.57.0.131
	netmask 255.255.255.128
	gateway 10.57.0.129

```

- ### Revolte
```
auto eth0
iface eth0 inet static
	address 10.57.0.30
	netmask 255.255.255.252
	gateway 10.57.0.29

```

- ### Richter
```
auto eth0
iface eth0 inet static
	address 10.57.0.26
	netmask 255.255.255.252
	gateway 10.57.0.25

```

- ### LaubHills
```
auto eth0
iface eth0 inet static
	address 10.57.2.2
	netmask 255.255.254.0
	gateway 10.57.2.1

```


# Routing

- ### Aura
``` bash
route add -net 10.57.8.0 netmask 255.255.248.0 gw 10.57.0.2
route add -net 10.57.4.0 netmask 255.255.252.0 gw 10.57.0.2
route add -net 10.57.0.16 netmask 255.255.255.252 gw 10.57.0.6
route add -net 10.57.0.128 netmask 255.255.255.128 gw 10.57.0.6
route add -net 10.57.0.20 netmask 255.255.255.252 gw 10.57.0.6
route add -net 10.57.2.0 netmask 255.255.254.0 gw 10.57.0.6
route add -net 10.57.0.24 netmask 255.255.255.252 gw 10.57.0.6
route add -net 10.57.0.28 netmask 255.255.255.252 gw 10.57.0.6
```

- ### Heiter
``` bash
```

- ### Frieren
``` bash
route add -net 10.57.0.128 netmask 255.255.255.128 gw 10.57.0.18
route add -net 10.57.2.0 netmask 255.255.254.0 gw 10.57.0.18
route add -net 10.57.0.24 netmask 255.255.255.252 gw 10.57.0.18
route add -net 10.57.0.28 netmask 255.255.255.252 gw 10.57.0.18
```

- ### Himmel
``` bash
route add -net 10.57.0.24 netmask 255.255.255.252 gw 10.57.0.130
route add -net 10.57.0.28 netmask 255.255.255.252 gw 10.57.0.130
```

- ### Fern
``` bash
```


# Soal
1. Agar topologi yang kalian buat dapat mengakses keluar, kalian diminta untuk mengkonfigurasi Aura menggunakan iptables, tetapi tidak ingin menggunakan MASQUERADE.
2. Kalian diminta untuk melakukan drop semua TCP dan UDP kecuali port 8080 pada TCP.
3. Kepala Suku North Area meminta kalian untuk membatasi DHCP dan DNS Server hanya dapat dilakukan ping oleh maksimal 3 device secara bersamaan, selebihnya akan di drop.
4. Lakukan pembatasan sehingga koneksi SSH pada Web Server hanya dapat dilakukan oleh masyarakat yang berada pada GrobeForest.
5. Selain itu, akses menuju WebServer hanya diperbolehkan saat jam kerja yaitu Senin-Jumat pada pukul 08.00-16.00.
6. Lalu, karena ternyata terdapat beberapa waktu di mana network administrator dari WebServer tidak bisa stand by, sehingga perlu ditambahkan rule bahwa akses pada hari Senin - Kamis pada jam 12.00 - 13.00 dilarang (istirahat maksi cuy) dan akses di hari Jumat pada jam 11.00 - 13.00 juga dilarang (maklum, Jumatan rek).
7. Karena terdapat 2 WebServer, kalian diminta agar setiap client yang mengakses Sein dengan Port 80 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan dan request dari client yang mengakses Stark dengan port 443 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan.
8. Karena berbeda koalisi politik, maka subnet dengan masyarakat yang berada pada Revolte dilarang keras mengakses WebServer hingga masa pencoblosan pemilu kepala suku 2024 berakhir. Masa pemilu (hingga pemungutan dan penghitungan suara selesai) kepala suku bersamaan dengan masa pemilu Presiden dan Wakil Presiden Indonesia 2024.
9. Sadar akan adanya potensial saling serang antar kubu politik, maka WebServer harus dapat secara otomatis memblokir  alamat IP yang melakukan scanning port dalam jumlah banyak (maksimal 20 scan port) di dalam selang waktu 10 menit. (clue: test dengan nmap)
10. Karena kepala suku ingin tau paket apa saja yang di-drop, maka di setiap node server dan router ditambahkan logging paket yang di-drop dengan standard syslog level


# Setup
- ### Aura (DHCP Relay, Edge Router)
``` bash
# Populate NAT iptables to enable NAT
iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 10.57.0.0/16

# Install Required Packages
apt-get update
apt-get install isc-dhcp-relay -y

# Config DHCP Relay
echo "
net.ipv4.ip_forward=1
" > /etc/sysctl.conf
echo '
SERVERS="10.57.0.30"
INTERFACES="eth1 eth2"
OPTIONS=""
' > /etc/default/isc-dhcp-relay

# Start DHCP Relay
service isc-dhcp-relay start

# Set DNS Server
echo nameserver 10.57.0.26 > /etc/resolv.conf
```

- ### Richter (DNS Server)
``` bash
# Set DNS Server
echo nameserver 192.168.122.1 > /etc/resolv.conf

# Install Required Packages
apt-get update
apt-get install bind9 -y 

# Prepare Directory
mkdir -p /etc/bind/praktikum

# Enable DNS Forwarder
echo '
options {
  directory "/var/cache/bind";
  forwarders {
    192.168.122.1;
  };
  allow-query{any;};

  listen-on-v6 { any; };
};
' > /etc/bind/named.conf.options

service bind9 restart
```

- ### Heiter (DHCP Relay)
``` bash
# Set DNS Server
echo nameserver 10.57.0.26 > /etc/resolv.conf

# Install Required Packages
apt-get update
apt-get install isc-dhcp-relay -y

# Config DHCP Relay
echo "
net.ipv4.ip_forward=1
" > /etc/sysctl.conf
echo '
SERVERS="10.57.0.30"
INTERFACES="eth0 eth1 eth2"
OPTIONS=""
' > /etc/default/isc-dhcp-relay

# Start DHCP Relay
service isc-dhcp-relay start
```

- ### Frieren (DHCP Relay)
``` bash
# Set DNS Server
echo nameserver 10.57.0.26 > /etc/resolv.conf

# Install Required Packages
apt-get update
apt-get install isc-dhcp-relay -y

# Config DHCP Relay
echo "
net.ipv4.ip_forward=1
" > /etc/sysctl.conf
echo '
SERVERS="10.57.0.30"
INTERFACES="eth0 eth1 eth2"
OPTIONS=""
' > /etc/default/isc-dhcp-relay

# Start DHCP Relay
service isc-dhcp-relay start
```

- ### Himmel (DHCP Relay)
``` bash
# Set DNS Server
echo nameserver 10.57.0.26 > /etc/resolv.conf

# Install Required Packages
apt-get update
apt-get install isc-dhcp-relay -y

# Config DHCP Relay
echo "
net.ipv4.ip_forward=1
" > /etc/sysctl.conf
echo '
SERVERS="10.57.0.30"
INTERFACES="eth0 eth1 eth2"
OPTIONS=""
' > /etc/default/isc-dhcp-relay

# Start DHCP Relay
service isc-dhcp-relay start
```

- ### Fern (DHCP Relay)
``` bash
# Set DNS Server
echo nameserver 10.57.0.26 > /etc/resolv.conf

# Install Required Packages
apt-get update
apt-get install isc-dhcp-relay -y

# Config DHCP Relay
echo "
net.ipv4.ip_forward=1
" > /etc/sysctl.conf
echo '
SERVERS="10.57.0.30"
INTERFACES="eth0 eth1 eth2"
OPTIONS=""
' > /etc/default/isc-dhcp-relay

# Start DHCP Relay
service isc-dhcp-relay start
```

- ### Revolte (DHCP Server)
``` bash
# Set DNS Server
echo nameserver 10.57.0.26 > /etc/resolv.conf

# Install Required Packages
apt-get update
apt-get install isc-dhcp-server --no-install-recommends -y

# Set DHCP Interface
echo '
INTERFACESv4="eth0"
INTERFACESv6=""
' > /etc/default/isc-dhcp-server

# Config DHCP Server
echo '
default-lease-time 600;
max-lease-time 7200;

ddns-update-style none;

subnet 10.57.0.28 netmask 255.255.255.252 {
}

subnet 10.57.0.128 netmask 255.255.255.128 {
    range 10.57.0.131 10.57.0.254;
    option routers 10.57.0.129;
    option broadcast-address 10.57.0.255;
    option domain-name-servers 10.57.0.26;
}

subnet 10.57.8.0 netmask 255.255.248.0 {
    range 10.57.8.2 10.57.15.254;
    option routers 10.57.8.1;
    option broadcast-address 10.57.15.255;
    option domain-name-servers 10.57.0.26;
}

subnet 10.57.4.0 netmask 255.255.252.0 {
    range 10.57.4.2 10.57.7.254;
    option routers 10.57.4.1;
    option broadcast-address 10.57.7.255;
    option domain-name-servers 10.57.0.26;
}

subnet 10.57.2.0 netmask 255.255.254.0 {
    range 10.57.2.2 10.57.3.254;
    option routers 10.57.2.1;
    option broadcast-address 10.57.3.255;
    option domain-name-servers 10.57.0.26;
}
' > /etc/dhcp/dhcpd.conf

# Enable dhcp server
service isc-dhcp-server restart
```

- ### Sein (Web Server)
``` bash
# Set DNS Server
echo nameserver 10.57.0.26 > /etc/resolv.conf

# Install Required Packages
apt-get update
apt-get install netcat -y
```

- ### Stark (Web Server)
``` bash
# Set DNS Server
echo nameserver 10.57.0.26 > /etc/resolv.conf

# Install Required Packages
apt-get update
apt-get install netcat -y
```


# Jawaban

## No. 1
Jalankan
``` bash
# Flush NAT Table
iptables -t nat -F

# Set SNAT rule for NAT postrouting
iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source $(ifconfig eth0 | grep inet | awk '{print $2}')
```
---
Bisa kita lakukan ping ke sebuah ip external pada node selain **Aura** untuk memeriksa apakah NAT berfungsi
```
ping 1.1.1.1
```
![Screenshot from 2023-12-15 16-39-17](https://github.com/ZhafranMZ/Jarkom-Modul-5-F11-2023/assets/63389207/f010d67e-bf41-4eaf-a0b4-1ae0d3f2e6f8)


## No. 2
Jalankan pada server yang hanya membolehkan port `8080` untuk masuk
``` bash
# Flush Filter Table
iptables -F

# Accept ICMP
iptables -A INPUT -p icmp -j ACCEPT

# Accept TCP port 8080(http-alt) packet
iptables -A INPUT -p tcp --dport 8080 -j ACCEPT

# Drop all other TCP and UDP protocol packet
iptables -A INPUT -p tcp -j DROP
iptables -A INPUT -p udp -j DROP
```
---
Untuk melakukan pengecekan pada port `8080`, kita bisa menggunakan netcat untuk mendengarkan port `8080` dengan langkah berikut

Pertama install netcat pada client dan server
``` bash
# Set DNS Server
echo nameserver 10.57.0.26 > /etc/resolv.conf

# Install Required Packages
apt-get update
apt-get install netcat -y
```

---
Untuk melakukan pengecekan, bikin file `listen8080.sh` dan `listen8080.sh` pada server yang berisi

- `listen8080.sh`
``` bash
echo '
while true
do
	nc -l -p 8080 -c "hostname"
done
' > listen8080.sh
```
- `listen8080.sh`
``` bash
echo '
while true
do
	nc -l -p 8000 -c "hostname"
done
' > listen8000.sh
```
kemudian jalankan pada server
``` bash
# Add Running Permission
chmod +x listen8080.sh 
chmod +x listen8000.sh

# Run listen8080.sh and listen8080.sh in the Background
./listen8080.sh & ./listen8080.sh & disown
```
Kemudian bisa jalankan pada client
``` bash
nc [server ip] 8080 -w 3
nc [server ip] 8000 -w 3
```
![Screenshot from 2023-12-15 15-40-38](https://github.com/ZhafranMZ/Jarkom-Modul-5-F11-2023/assets/63389207/da7f8c9b-f574-431f-93ab-4f7b5a3d0182)


---
Tips: pastikan tidak ada proses yang mendengarkan port tersebut dengan melakukan list semua port yang mendengarkan dan mendapatkan `[pid]` dengan
``` bash
netstat -anp
```
kemudian mematikan proses tersebut dengan
``` bash
kill -9 [pid]
```
## No. 3
Jalankan pada **Revolte** dan **Richter** 
``` bash
iptables -A INPUT -p icmp -m connlimit --connlimit-above 3 --connlimit-mask 0 -j DROP
```
---
Lakukan testing dengan melakukan ping dari 4 buah server yang berbeda. Ping `10.57.0.26` untuk **Richter** dan `10.57.0.30` untuk **Revolte**.
![Screenshot from 2023-12-15 15-25-32](https://github.com/ZhafranMZ/Jarkom-Modul-5-F11-2023/assets/63389207/b0e97520-5a84-4b03-a72e-29d58e574ff3)
![Screenshot from 2023-12-15 15-25-25](https://github.com/ZhafranMZ/Jarkom-Modul-5-F11-2023/assets/63389207/a4ca76a9-bf70-4e9e-9766-c0b7189ded29)
![Screenshot from 2023-12-15 15-33-15](https://github.com/ZhafranMZ/Jarkom-Modul-5-F11-2023/assets/63389207/caf16ed5-dbc4-4ba5-8807-967e61637dd1)
![Screenshot from 2023-12-15 15-31-05](https://github.com/ZhafranMZ/Jarkom-Modul-5-F11-2023/assets/63389207/7a415410-0e57-4fdd-97ce-163462a4486f)

## No. 4
Jalankan pada webserver **Sein** dan **Stark** yang membolehkan akses untuk port `22` pada subnet `10.57.4.0/22` yaitu **GrobeForest**
``` bash
iptables -A INPUT -p tcp --dport 22 -s 10.57.4.0/22 -j ACCEPT
iptables -A INPUT -p tcp --dport 22 -j DROP
```

Jalnkan pada client
``` bash
nmap [server ip] -p 22
```
Lakukan pada  `10.57.0.22` untuk **Stark**, dan `10.57.4.2` untuk **Sein**
- Client GrobeForest

![Screenshot from 2023-12-15 12-39-54](https://github.com/ZhafranMZ/Jarkom-Modul-5-F11-2023/assets/63389207/6008026b-cff5-4a82-a22a-61ef7a5b6684)
- Selain GrobeForest

![Screenshot from 2023-12-15 12-39-32](https://github.com/ZhafranMZ/Jarkom-Modul-5-F11-2023/assets/63389207/8c5e9d2c-c07d-4415-9783-56caa8d27065)

## No. 5
``` bash
# Accept Rule
iptables -A INPUT -p tcp --dport 8080 -m time --timestart 08:00 --timestop 16:00 --weekdays Mon,Tue,Wed,Thu,Fri -j ACCEPT

# Drop Rule
iptables -A INPUT -p tcp --dport 8080 -j DROP
```

## No. 6
``` bash
# Delete Previous Rule
iptables -D INPUT -p tcp --dport 8080 -m time --timestart 08:00 --timestop 16:00 --weekdays Mon,Tue,Wed,Thu,Fri -j ACCEPT
iptables -D INPUT -p tcp --dport 8080 -j DROP

# Added New Rule
iptables -A INPUT -p tcp --dport 8080 -m time --timestart 12:00 --timestop 13:00 --weekdays Mon,Tue,Wed,Thu -j DROP
iptables -A INPUT -p tcp --dport 8080 -m time --timestart 11:00 --timestop 13:00 --weekdays Fri -j DROP

# Re-Add Previously Deleted Rule
iptables -A INPUT -p tcp --dport 8080 -m time --timestart 08:00 --timestop 16:00 --weekdays Mon,Tue,Wed,Thu,Fri -j ACCEPT
iptables -A INPUT -p tcp --dport 8080 -j DROP
```

## No. 7
Jalankan pada **Sein**
``` bash

```

Jalankan pada **Stark**
``` bash

```
---
Untuk melakukan pengecekan, bikin file `listen80.sh` dan `listen443.sh` pada **Sein** dan **Stark** yang berisi

- `listen80.sh`
``` bash
while true
do
	nc -l -p 80 -c 'hostname'
done
```
- `listen443.sh`
``` bash
while true
do
	nc -l -p 443 -c 'hostname'
done
```
kemudian jalankan pada **Sein** dan **Stark**
``` bash
# Add Running Permission
chmod +x listen80.sh 
chmod +x listen443.sh

# Run listen80.sh and listen443.sh in the Background
./listen80.sh & ./listen443.sh & disown
```
## No. 8
Dikarenakan menurut [https://infopemilu.kpu.go.id/Pemilu/Peserta_pemilu](https://infopemilu.kpu.go.id/Pemilu/Peserta_pemilu) pemilu akan dilakukan pada `14 Februari 2024` sampai `15 Februari 2024` maka waktu mulai adalah `2024-02-14T00:00:00` dan waktu akhir adalah `2024-02-15T00:00:00` sesuai format dalam man untuk iptables

> ### time
> This matches if the packet arrival time/date is within a given range. All options are optional, but are ANDed when specified. All times are interpreted as UTC by default.
> 
> --datestart YYYY[-MM[-DD[Thh[:mm[:ss]]]]]  
> --datestop YYYY[-MM[-DD[Thh[:mm[:ss]]]]]  
> Only match during the given time, which must be in ISO 8601 "T" notation. The possible time range is 1970-01-01T00:00:00 to 2038-01-19T04:17:07.
> If --datestart or --datestop are not specified, it will default to 1970-01-01 and 2038-01-19, respectively.

Masukkan dalam **Sein** dan **Stark**
``` bash
iptables -A INPUT -p tcp -s 10.57.0.28/30 -m multiport --dports 80,443 -m time --datestart "2024-02-14T00:00:00" --datestop "2024-02-15T00:00:00" -j DROP
```
## No. 9
Jalankan pada webserver **Sein** dan **Stark** 
``` bash
# Create New Chain called PORTSCANLIMIT
iptables -N PORTSCANLIMIT
iptables -A PORTSCANLIMIT -m recent --set --name PORTSCANLIMIT
iptables -A PORTSCANLIMIT -m recent --update --seconds 600 --hitcount 20 --name PORTSCANLIMIT --rsource -j
iptables -A PORTSCANLIMIT -m recent --update --seconds 600 --hitcount 20 --name PORTSCANLIMIT --rsource -j DROP

# Add PORTSCANLIMIT chain to INPUT
iptables -A INPUT -p tcp -j PORTSCANLIMIT
```
---
Untuk melakukan pengecekan, pada node lain, jalankan
``` bash
nmap [server ip] -p 1-50
```
Dimana `[server ip]` adalah `10.57.0.26` untuk **Richter** dan `10.57.0.30` untuk **Revolte**.
![Screenshot from 2023-12-15 15-03-39](https://github.com/ZhafranMZ/Jarkom-Modul-5-F11-2023/assets/63389207/4481617e-cacd-4973-b691-85a71c4843d0)

## No. 10
Jalankan pada selurun node
``` bash
iptables -N DROPLOG
iptables -A DROPLOG -j LOG --log-level debug --log-prefix "Dropped Packet: "

iptables -A INPUT -j DROPLOG
iptables -A OUTPUT -j DROPLOG
iptables -A FORWARD -j DROPLOG
```
---
Untuk mendapatkan log untuk paket yang di drop, kita dapat melihat syslog pada `/var/log/syslog`
``` bash
cat /var/log/syslog | grep "Dropped Packet"
```

# Jarkom-Modul-2-I10-2023

Praktikum Jaringan Komputer Modul 1 I10
Computer Network Practicum 1st Module I10

| Name                        | NRP        |
|-----------------------------|------------|
|Riski Ilyas                  | 5025211189 |
|Vija Wildan Gita Prabawa     | 5025211261 |

## Problem 1

Yudhistira akan digunakan sebagai DNS Master, Werkudara sebagai DNS Slave, Arjuna merupakan Load Balancer yang terdiri dari beberapa Web Server yaitu Prabakusuma, Abimanyu, dan Wisanggeni. Buatlah topologi dengan pembagian sebagai berikut. Folder topologi dapat diakses pada drive berikut

![Topology](https://media.discordapp.net/attachments/919468862725046322/1163798430536171630/image.png?ex=6540e2c0&is=652e6dc0&hm=1efd6bd22172fc5309717c58fc4a10c2d7efb86d195891f76fb948576d60a636&=&width=1435&height=702)
<p style="text-align: center;">The Topology</p>

## Network Configuration

#### Pandudewanata
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 192.233.1.1
	netmask 255.255.255.0

auto eth2
iface eth2 inet static
	address 192.233.2.1
	netmask 255.255.255.0

auto eth3
iface eth3 inet static
	address 192.233.3.1
	netmask 255.255.255.0
```

#### Yudhistira
```
auto eth0
iface eth0 inet static
	address 192.233.3.2
	netmask 255.255.255.0
	gateway 192.233.3.1
```

### Switch 1

#### Sadewa
```
auto eth0
iface eth0 inet static
	address 192.233.1.2
	netmask 255.255.255.0
	gateway 192.233.1.1
```

#### Nakula
```
auto eth0
iface eth0 inet static
	address 192.233.1.2
	netmask 255.255.255.0
	gateway 192.233.1.1
```

### Switch 2

#### Werkudara
```
auto eth0
iface eth0 inet static
	address 192.233.2.2
	netmask 255.255.255.0
	gateway 192.233.2.1
```

#### Arjuna
```
auto eth0
iface eth0 inet static
	address 192.233.2.9
	netmask 255.255.255.0
	gateway 192.233.2.1
```

#### Abimanyu
```
auto eth0
iface eth0 inet static
	address 192.233.2.3
	netmask 255.255.255.0
	gateway 192.233.2.1
```

#### Prabukusuma
```
auto eth0
iface eth0 inet static
	address 192.233.2.4
	netmask 255.255.255.0
	gateway 192.233.2.1
```

#### Wisanggeni
```
auto eth0
iface eth0 inet static
	address 192.233.2.5
	netmask 255.255.255.0
	gateway 192.233.2.1
```

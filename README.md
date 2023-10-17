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
The Topology

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

## Problem 2
Buatlah website utama pada node arjuna dengan akses ke arjuna.yyy.com dengan alias www.arjuna.yyy.com dengan yyy merupakan kode kelompok.
![image](https://github.com/vijawildan/Jarkom-Modul-2-I10-2023/assets/71499142/269fec73-a7d8-4818-8913-18341da26823)
![image](https://github.com/vijawildan/Jarkom-Modul-2-I10-2023/assets/71499142/8fae9d9e-434c-44fd-a1fa-41d445a658bd)

## Problem 3
Dengan cara yang sama seperti soal nomor 2, buatlah website utama dengan akses ke abimanyu.yyy.com dan alias www.abimanyu.yyy.com.
![image](https://github.com/vijawildan/Jarkom-Modul-2-I10-2023/assets/71499142/04b7e3ff-f4cb-4325-b3e8-9ec4f12a1ad3)
![image](https://github.com/vijawildan/Jarkom-Modul-2-I10-2023/assets/71499142/c6c4a954-5fc8-4dfa-a801-f922e7048027)

## Problem 4
Kemudian, karena terdapat beberapa web yang harus di-deploy, buatlah subdomain parikesit.abimanyu.yyy.com yang diatur DNS-nya di Yudhistira dan mengarah ke Abimanyu.
![image](https://github.com/vijawildan/Jarkom-Modul-2-I10-2023/assets/71499142/52c129e8-b353-43f2-90bc-d256f431fa95)

## Problem 5
Buat juga reverse domain untuk domain utama. (Abimanyu saja yang direverse)
![image](https://github.com/vijawildan/Jarkom-Modul-2-I10-2023/assets/71499142/a1982b84-03b5-40fc-a407-7852d1e23374)

## Problem 6
Agar dapat tetap dihubungi ketika DNS Server Yudhistira bermasalah, buat juga Werkudara sebagai DNS Slave untuk domain utama.
![image](https://github.com/vijawildan/Jarkom-Modul-2-I10-2023/assets/71499142/75b0fe03-0355-4cb9-b7a6-dc23b5db23f0)
![image](https://github.com/vijawildan/Jarkom-Modul-2-I10-2023/assets/71499142/7156213a-2834-46a7-bb35-d7121fa3353b)

## Problem 7
Seperti yang kita tahu karena banyak sekali informasi yang harus diterima, buatlah subdomain khusus untuk perang yaitu baratayuda.abimanyu.yyy.com dengan alias www.baratayuda.abimanyu.yyy.com yang didelegasikan dari Yudhistira ke Werkudara dengan IP menuju ke Abimanyu dalam folder Baratayuda.

## Problem 8
Untuk informasi yang lebih spesifik mengenai Ranjapan Baratayuda, buatlah subdomain melalui Werkudara dengan akses rjp.baratayuda.abimanyu.yyy.com dengan alias www.rjp.baratayuda.abimanyu.yyy.com yang mengarah ke Abimanyu.

# Answer & Scripts
## Router Pandudewanata
![image](https://github.com/vijawildan/Jarkom-Modul-2-I10-2023/assets/71499142/a2f4d4aa-6786-4229-9a43-eab2852018f5)

## Nakula Client
![image](https://github.com/vijawildan/Jarkom-Modul-2-I10-2023/assets/71499142/26d2997e-79f9-405d-987f-bf31a9e93769)

## Yudhistira DNS Master
![image](https://github.com/vijawildan/Jarkom-Modul-2-I10-2023/assets/71499142/d3ae221a-9668-4fb7-842f-f83c78570cfc)

## Werkudara DNS Slave
![image](https://github.com/vijawildan/Jarkom-Modul-2-I10-2023/assets/71499142/871abc0c-ec6b-4ddc-b97b-386fdf5ee024)

## Arjuna Load Balancer
![image](https://github.com/vijawildan/Jarkom-Modul-2-I10-2023/assets/71499142/12b9899b-cd30-42a3-9060-864d96abb3e7)

## Abimanyu Web Serve
![image](https://github.com/vijawildan/Jarkom-Modul-2-I10-2023/assets/71499142/9c31bbee-d3da-48de-a085-bdd49c2151a3)



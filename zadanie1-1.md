# hasz 1: 81dc9bdb52d04dc20036dbd8313ed055

## Identyfikacja typu hasza
```shell
hash-identifier 81dc9bdb52d04dc20036dbd8313ed055
Possible Hashs:
[+] MD5
[+] Domain Cached Credentials - MD4(MD4(($pass)).(strtolower($username)))
```

## Łamanie
```shell
MD5 - .\hashcat.exe -a 3 -m 0 .\hash1.txt -i '?d?d?d?d?d' -O

81dc9bdb52d04dc20036dbd8313ed055:1234

Session..........: hashcat
Status...........: Cracked
Hash.Mode........: 0 (MD5)
Hash.Target......: 81dc9bdb52d04dc20036dbd8313ed055
```

# hasz 2: d8826bbd80b4233b7522d1c538aeaf66c64e259a 

## Identyfikacja typu hasha:
```shell
HASH: d8826bbd80b4233b7522d1c538aeaf66c64e259a

Possible Hashs:
[+] SHA-1
[+] MySQL5 - SHA-1(SHA-1($pass))
```

## Łamanie
```shell
SHA1 - .\hashcat.exe -a 3 -m 100 .\hash2.txt -i '?d?d?d?d?d' -O

d8826bbd80b4233b7522d1c538aeaf66c64e259a:4121

Session..........: hashcat
Status...........: Cracked
Hash.Mode........: 100 (SHA1)
Hash.Target......: d8826bbd80b4233b7522d1c538aeaf66c64e259a
```
# hasz 3: b021d0862bc76b0995927902ec697d97b5080341a53cd90b780f50fd5886f4160bbb9d4a573b76c23004c9b3a44ac95cfde45399e3357d1f651b556dfbd0d58f

## Identyfikacja typu hasha:
```shell
HASH: b021d0862bc76b0995927902ec697d97b5080341a53cd90b780f50fd5886f4160bbb9d4a573b76c23004c9b3a44ac95cfde45399e3357d1f651b556dfbd0d58f

Possible Hashs:
[+] SHA-512
[+] Whirlpool
```
## Łamanie
```shell
PS C:\Program Files\hashcat-6.2.6> .\hashcat.exe -a 3 -m 1700 .\hash3.txt -i '?d?d?d?d?d' -O
b021d0862bc76b0995927902ec697d97b5080341a53cd90b780f50fd5886f4160bbb9d4a573b76c23004c9b3a44ac95cfde45399e3357d1f651b556dfbd0d58f:6969

Session..........: hashcat
Status...........: Cracked
Hash.Mode........: 1700 (SHA2-512)
Hash.Target......: b021d0862bc76b0995927902ec697d97b5080341a53cd90b780...d0d58f
```

# hasz 4: 31bca02094eb78126a517b206a88c73cfa9ec6f704c7030d18212cace820f025f00bf0ea68dbf3f3a5436ca63b53bf7bf80ad8d5de7d8359d0b7fed9dbc3ab99
## Identyfikacja typu hasha:

```shell
HASH: 31bca02094eb78126a517b206a88c73cfa9ec6f704c7030d18212cace820f025f00bf0ea68dbf3f3a5436ca63b53bf7bf80ad8d5de7d8359d0b7fed9dbc3ab99

Possible Hashs:
[+] SHA-512
[+] Whirlpool

```
## Łamanie
```shell
PS C:\Program Files\hashcat-6.2.6> .\hashcat.exe -a 3 -m 1700 .\hash4.txt -i '?d?d?d?d?d' -O
31bca02094eb78126a517b206a88c73cfa9ec6f704c7030d18212cace820f025f00bf0ea68dbf3f3a5436ca63b53bf7bf80ad8d5de7d8359d0b7fed9dbc3ab99:0

Session..........: hashcat
Status...........: Cracked
Hash.Mode........: 1700 (SHA2-512)
Hash.Target......: 31bca02094eb78126a517b206a88c73cfa9ec6f704c7030d182...c3ab99
```

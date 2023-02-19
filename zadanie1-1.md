# hasz 1: 81dc9bdb52d04dc20036dbd8313ed055

## Identyfikacja typu hasza
``shell
hash-identifier 81dc9bdb52d04dc20036dbd8313ed055
Possible Hashs:
[+] MD5
[+] Domain Cached Credentials - MD4(MD4(($pass)).(strtolower($username)))
``

## Łamanie
``shell
MD5 - .\hashcat.exe -a 3 -m 0 .\hash1.txt -i '?d?d?d?d?d' -O

81dc9bdb52d04dc20036dbd8313ed055:1234

Session..........: hashcat
Status...........: Cracked
Hash.Mode........: 0 (MD5)
Hash.Target......: 81dc9bdb52d04dc20036dbd8313ed055
``

# hasz 2: d8826bbd80b4233b7522d1c538aeaf66c64e259a 

## Identyfikacja typu hasha:
``shell
HASH: d8826bbd80b4233b7522d1c538aeaf66c64e259a

Possible Hashs:
[+] SHA-1
[+] MySQL5 - SHA-1(SHA-1($pass))
`` 

``shell 
SHA1 - .\hashcat.exe -a 3 -m 100 .\hash2.txt -i '?d?d?d?d?d' -O

d8826bbd80b4233b7522d1c538aeaf66c64e259a:4121

Session..........: hashcat
Status...........: Cracked
Hash.Mode........: 100 (SHA1)
Hash.Target......: d8826bbd80b4233b7522d1c538aeaf66c64e259a
``


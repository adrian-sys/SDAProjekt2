# hasz 1: 44d9886c0a57ddbfdb31aa936bd498bf2ab70f741ee47047851e768db953fc4e43f92be953e205a3d1b3ab752ed90379444b651b582b0bc209a739a624e109da

## Identyfikacja typu hasza
```shell
 HASH: 44d9886c0a57ddbfdb31aa936bd498bf2ab70f741ee47047851e768db953fc4e43f92be953e205a3d1b3ab752ed90379444b651b582b0bc209a739a624e109da

Possible Hashs:
[+] SHA-512
[+] Whirlpool

```

## Łamanie
```shell
PS C:\Program Files\hashcat-6.2.6> .\hashcat.exe -a 3 -m 1700 .\hash7.txt -w 3 -i -1 ?l?d?s?u ?1?1?1?1?1?1 -O

44d9886c0a57ddbfdb31aa936bd498bf2ab70f741ee47047851e768db953fc4e43f92be953e205a3d1b3ab752ed90379444b651b582b0bc209a739a624e109da:T0^^3k

Session..........: hashcat
Status...........: Cracked
Hash.Mode........: 1700 (SHA2-512)
Hash.Target......: 44d9886c0a57ddbfdb31aa936bd498bf2ab70f741ee47047851...e109da
Time.Started.....: Sun Feb 19 11:17:33 2023 (5 mins, 32 secs)
Time.Estimated...: Sun Feb 19 11:23:05 2023 (0 secs)
Kernel.Feature...: Optimized Kernel
Guess.Mask.......: ?1?1?1?1?1?1 [6]
Guess.Charset....: -1 ?l?d?s?u, -2 Undefined, -3 Undefined, -4 Undefined
Guess.Queue......: 6/6 (100.00%)
Speed.#1.........:   533.9 MH/s (76.73ms) @ Accel:16 Loops:1024 Thr:256 Vec:1
Recovered........: 1/1 (100.00%) Digests (total), 1/1 (100.00%) Digests (new)
Progress.........: 179043205120/735091890625 (24.36%)
Rejected.........: 0/179043205120 (0.00%)
Restore.Point....: 19824640/81450625 (24.34%)
Restore.Sub.#1...: Salt:0 Amplifier:2048-3072 Iteration:0-1024
Candidate.Engine.: Device Generator
Candidates.#1....: EBSj2h -> 6wKTN9
Hardware.Mon.#1..: Temp: 79c Fan: 67% Util:100% Core:1885MHz Mem:3802MHz Bus:16

Started: Sun Feb 19 11:17:06 2023
Stopped: Sun Feb 19 11:23:07 2023
```

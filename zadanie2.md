# Zadanie 2

## Cześć 1/2

### Identyfikacja typu algorytmu haszującego
```shell
1. 9fd8301ac24fb88e65d9d7cd1dd1b1ec - md5
2. 7f9a6871b86f40c330132c4fc42cda59 - md5
3. 6104df369888589d6dbea304b59a32d4 - md5
4. 276f8db0b86edaa7fc805516c852c889 - md5
5. 04dac8afe0ca501587bad66f6b5ce5ad - md5
```
### Łamanie hashy
```shell

PS C:\Program Files\hashcat-6.2.6> .\hashcat.exe -a 0 -m 0 .\hashe.txt .\rockyou-50.txt -O
hashcat (v6.2.6) starting

CUDA API (CUDA 12.0)
====================
* Device #1: NVIDIA GeForce GTX 1060 6GB, 5214/6143 MB, 10MCU

OpenCL API (OpenCL 3.0 CUDA 12.0.139) - Platform #1 [NVIDIA Corporation]
========================================================================
* Device #2: NVIDIA GeForce GTX 1060 6GB, skipped

Minimum password length supported by kernel: 0
Maximum password length supported by kernel: 31

Hashes: 5 digests; 5 unique digests, 1 unique salts
Bitmaps: 16 bits, 65536 entries, 0x0000ffff mask, 262144 bytes, 5/13 rotates
Rules: 1

Optimizers applied:
* Optimized-Kernel
* Zero-Byte
* Precompute-Init
* Meet-In-The-Middle
* Early-Skip
* Not-Salted
* Not-Iterated
* Single-Salt
* Raw-Hash

Watchdog: Temperature abort trigger set to 90c

Host memory required for this attack: 1473 MB

Dictionary cache built:
* Filename..: .\rockyou-50.txt
* Passwords.: 9437
* Bytes.....: 75911
* Keyspace..: 9437
* Runtime...: 0 secs

The wordlist or mask that you are using is too small.
This means that hashcat cannot use the full parallel power of your device(s).
Unless you supply more work, your cracking speed will drop.
For tips on supplying more work, see: https://hashcat.net/faq/morework

Approaching final keyspace - workload adjusted.

7f9a6871b86f40c330132c4fc42cda59:tinkerbell
9fd8301ac24fb88e65d9d7cd1dd1b1ec:butterfly
04dac8afe0ca501587bad66f6b5ce5ad:hellokitty
6104df369888589d6dbea304b59a32d4:blink182
276f8db0b86edaa7fc805516c852c889:baseball

Session..........: hashcat
Status...........: Cracked
Hash.Mode........: 0 (MD5)
Hash.Target......: .\hashe.txt
Time.Started.....: Sun Feb 19 11:43:07 2023 (0 secs)
Time.Estimated...: Sun Feb 19 11:43:07 2023 (0 secs)
Kernel.Feature...: Optimized Kernel
Guess.Base.......: File (.\rockyou-50.txt)
Guess.Queue......: 1/1 (100.00%)
Speed.#1.........:  1307.7 kH/s (0.02ms) @ Accel:16384 Loops:1 Thr:32 Vec:1
Recovered........: 5/5 (100.00%) Digests (total), 5/5 (100.00%) Digests (new)
Progress.........: 320/9437 (3.39%)
Rejected.........: 0/320 (0.00%)
Restore.Point....: 0/9437 (0.00%)
Restore.Sub.#1...: Salt:0 Amplifier:0-1 Iteration:0-1
Candidate.Engine.: Device Generator
Candidates.#1....: 123456 -> smokey
Hardware.Mon.#1..: Temp: 54c Fan:  0% Util: 25% Core:1898MHz Mem:3802MHz Bus:16

Started: Sun Feb 19 11:43:00 2023
Stopped: Sun Feb 19 11:43:08 2023
```
## Część 2/2
### Identyfikacja typu algorytmu haszującego
1. 7ab6888935567386376037e042524d27fc8a24ef87b1944449f6a0179991dbdbc481e98db4e70f6df0e04d1a69d8e7101d881379cf1966c992100389da7f3e9a - SHA-512
2. 470c62e301c771f12d91a242efbd41c5e467cba7419c664f784dbc8a20820abaf6ed43e09b0cda994824f14425db3e6d525a7aafa5d093a6a5f6bf7e3ec25dfa - SHA-512

### Łamanie
```shell
PS C:\Program Files\hashcat-6.2.6> .\hashcat.exe -d 2 -a 0 -m 1700 .\hashe2.txt .\rockyou-50.txt -O
hashcat (v6.2.6) starting

* Device #2: WARNING! Kernel exec timeout is not disabled.
             This may cause "CL_OUT_OF_RESOURCES" or related errors.
             To disable the timeout, see: https://hashcat.net/q/timeoutpatch
CUDA API (CUDA 12.0)
====================
* Device #1: NVIDIA GeForce GTX 1060 6GB, skipped

OpenCL API (OpenCL 3.0 CUDA 12.0.139) - Platform #1 [NVIDIA Corporation]
========================================================================
* Device #2: NVIDIA GeForce GTX 1060 6GB, 5504/6143 MB (1535 MB allocatable), 10MCU

Minimum password length supported by kernel: 0
Maximum password length supported by kernel: 31

Hashes: 2 digests; 2 unique digests, 1 unique salts
Bitmaps: 16 bits, 65536 entries, 0x0000ffff mask, 262144 bytes, 5/13 rotates
Rules: 1

Optimizers applied:
* Optimized-Kernel
* Zero-Byte
* Precompute-Init
* Early-Skip
* Not-Salted
* Not-Iterated
* Single-Salt
* Raw-Hash
* Uses-64-Bit

Watchdog: Temperature abort trigger set to 90c

Host memory required for this attack: 1190 MB

Dictionary cache hit:
* Filename..: .\rockyou-50.txt
* Passwords.: 9437
* Bytes.....: 75911
* Keyspace..: 9437

The wordlist or mask that you are using is too small.
This means that hashcat cannot use the full parallel power of your device(s).
Unless you supply more work, your cracking speed will drop.
For tips on supplying more work, see: https://hashcat.net/faq/morework

Approaching final keyspace - workload adjusted.

470c62e301c771f12d91a242efbd41c5e467cba7419c664f784dbc8a20820abaf6ed43e09b0cda994824f14425db3e6d525a7aafa5d093a6a5f6bf7e3ec25dfa:rockstar
7ab6888935567386376037e042524d27fc8a24ef87b1944449f6a0179991dbdbc481e98db4e70f6df0e04d1a69d8e7101d881379cf1966c992100389da7f3e9a:spiderman

Session..........: hashcat
Status...........: Cracked
Hash.Mode........: 1700 (SHA2-512)
Hash.Target......: .\hashe2.txt
Time.Started.....: Sun Feb 19 11:53:10 2023 (0 secs)
Time.Estimated...: Sun Feb 19 11:53:10 2023 (0 secs)
Kernel.Feature...: Optimized Kernel
Guess.Base.......: File (.\rockyou-50.txt)
Guess.Queue......: 1/1 (100.00%)
Speed.#2.........:  3126.1 kH/s (0.03ms) @ Accel:256 Loops:1 Thr:256 Vec:1
Recovered........: 2/2 (100.00%) Digests (total), 2/2 (100.00%) Digests (new)
Progress.........: 2560/9437 (27.13%)
Rejected.........: 0/2560 (0.00%)
Restore.Point....: 0/9437 (0.00%)
Restore.Sub.#2...: Salt:0 Amplifier:0-1 Iteration:0-1
Candidate.Engine.: Device Generator
Candidates.#2....: 123456 -> cloud9
Hardware.Mon.#2..: Temp: 54c Fan:  0% Util: 59% Core:1961MHz Mem:3802MHz Bus:16

Started: Sun Feb 19 11:52:53 2023
Stopped: Sun Feb 19 11:53:11 2023
```


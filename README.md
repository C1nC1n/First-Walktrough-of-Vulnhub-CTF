# First-Walktrough-of-Vulnhub-CTF
Description
Back to the Top
VM Name: JIS-CTF : VulnUpload

Difficulty: Beginner

Description: There are five flags on this machine. Try to find them. It takes 1.5 hour on average to find all flags.

Bandysime surasti visas penkias veliavas VM.
## 1. Netdiscover
<img width="1122" alt="Netdiscover" src="https://github.com/C1nC1n/First-Walktrough-of-Vulnhub-CTF/assets/163519448/47aa1d0c-a2ba-4fdf-a981-3322b9c54589">
Pasileidziam target VM 192.168.1.150 ir attacker 192.168.1.225 VM

Target ip gauname per Netdiscover

Attacker ip per ifconfig.

## Nmap

Turint ip pasileidziam nmap kur ieskome open portu. 22 ir 80 portas open.

<img width="473" alt="Nmap" src="https://github.com/C1nC1n/First-Walktrough-of-Vulnhub-CTF/assets/163519448/a964b548-2a0b-4a01-80cb-6abc44ad0895">

Kadangi atidarytas http portas suvedu ip i browseri ir gaunu log in page

<img width="620" alt="Screenshot 2024-07-08 at 12 37 22" src="https://github.com/C1nC1n/First-Walktrough-of-Vulnhub-CTF/assets/163519448/a9a13ea2-6379-4790-b420-30dc9b829b60">

## Dirb ir 1 st flag'as.

Pasileidziu dirb komanda ir randu pirma flaga

<img width="1033" alt="1st flag per nmap" src="https://github.com/C1nC1n/First-Walktrough-of-Vulnhub-CTF/assets/163519448/a14d1704-b55b-41a6-a345-f67432759f5a">

## Inspect ir 2st flag.

Pavaikciojus po dirb duotas direktorijas nieko labai neradau kol nepradejau labiau ieskoti per html kontenta kur ir radau antra flaga.
Nanem : admin
password 3vilH@ckor

<img width="1023" alt="2st flag per nmap ir inspect" src="https://github.com/C1nC1n/First-Walktrough-of-Vulnhub-CTF/assets/163519448/cec219eb-5a10-4339-8103-f14c67dabed9">

## Puslapis

Prisijungus su aptiktais admin loginais, programoje galime rasti failu įkėlimo funkcija turinti webpage. Anksčiau radau /uploaded_files , todel manau, kad ten nueina ikelimai.

<img width="983" alt="suvedus loginus " src="https://github.com/C1nC1n/First-Walktrough-of-Vulnhub-CTF/assets/163519448/db0acf07-b933-4193-aba9-7b259d2f0a2b">

## PHP reverse shell

Tai pagalvojus jei sistema leidzia mums ikelti kai kuriuos failus. Tai kodel nepabandyti php reverse shell.
Naudoju kali-linux'e esanti php reverse shell'a.

<img width="609" alt="php reverse naudojam" src="https://github.com/C1nC1n/First-Walktrough-of-Vulnhub-CTF/assets/163519448/f9d8b0c7-6beb-4041-9000-ff62192ece98">

## Pasijungiame php reverse shell

Ikeliam php scripta i webpage pasijungiame per 192.168.1.150/uploaded_files/php-reverse-shell.php 

Set upinam Net cat listener porta nc -nlvp 55555; 

Boom yra 

<img width="483" alt="Per php rever shell pasijungta" src="https://github.com/C1nC1n/First-Walktrough-of-Vulnhub-CTF/assets/163519448/569a2729-0506-4ba9-a88d-932e07418d56">

## 3rd flag'as

Tiesiog ziurim failus per ls ir cd ir ieskom kasko kol surandam hint.txt kur yra trecias flagas ir hintas, kad vardas technawi ir passwordas yra pasleptame faile flag.txt

<img width="498" alt="3rd flag su hintu" src="https://github.com/C1nC1n/First-Walktrough-of-Vulnhub-CTF/assets/163519448/48d752f9-ab8b-4884-ba1c-2f532b073422">

## Bandymas

Bandau rasti per failus kaska userio varda bet nieko gero nerandu.

<img width="482" alt="Bandziau ieskoti per technawi bet nieko nerasta" src="https://github.com/C1nC1n/First-Walktrough-of-Vulnhub-CTF/assets/163519448/925859ff-66bb-48c8-bc63-20da48dc5736">

## Find naudojimas

Matome visų failu, kuriuos vartotojas technawi turi prieiga, sarasa. Tarp isvardytu failu radau credentials.txt faila, kuriame slaptazodis.

<img width="530" alt="Pasinaudojus find : ,randam 4 flaga"
src="https://github.com/C1nC1n/First-Walktrough-of-Vulnhub-CTF/assets/163519448/61cc0017-4052-4bf1-91bd-e7cfe8a020db">

# SSH prisijungimas

Cia tiesiog ssh komanda prisijungiame su gautu vardu ir slaptazodziu.
ssh technawi@192.168.1.150

<img width="532" alt="ssh logina pasiimam" src="https://github.com/C1nC1n/First-Walktrough-of-Vulnhub-CTF/assets/163519448/fa0b5431-841e-4fba-bf96-f0017a0e3e08">

## Flag.txt

Tai dabar jau esame masinoje tai bandau atidaryti flag.txt kuriam reikejo neturejau teisiu atidaryti, pavyksta :) 

<img width="529" alt="Bandom flag txt atidaryti kurio neisejo" src="https://github.com/C1nC1n/First-Walktrough-of-Vulnhub-CTF/assets/163519448/dd9413fa-9e57-42c1-8baf-13af063209ca">

## Root access

Vysnia ant torto root access.
 
<img width="532" alt="Vysnia ant torto root acces" src="https://github.com/C1nC1n/First-Walktrough-of-Vulnhub-CTF/assets/163519448/71d8aafc-7a3d-4e7b-b643-be9da3e23468">



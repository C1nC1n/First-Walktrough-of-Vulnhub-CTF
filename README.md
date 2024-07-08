# This-repository-is-for-practising-the-GitHub-Flow
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

Placiau apie puslapi - suvedus logginus matau kad yra failų įkėlimo funkciją, kur vartotojas gali įkelti failą į tikslinę sistemą. Ta faila galima perziureti /uploaded_files/failopavadinimas

<img width="983" alt="suvedus loginus " src="https://github.com/C1nC1n/First-Walktrough-of-Vulnhub-CTF/assets/163519448/db0acf07-b933-4193-aba9-7b259d2f0a2b">

## PHP reverse shell

Tai pagalvojus jei sistema 

<img width="609" alt="php reverse naudojam" src="https://github.com/C1nC1n/First-Walktrough-of-Vulnhub-CTF/assets/163519448/f9d8b0c7-6beb-4041-9000-ff62192ece98">


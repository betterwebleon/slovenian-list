<h2>Datoteka hosts</h2>

Kot pojasnjuje [Steven Black](https://github.com/StevenBlack/hosts/blob/master/readme.md), gre pri *hosts* za besedilno datoteko (ki je brez datotečne pripone), v kateri se izbranim imenom gostiteljev (angl. hostnames) določijo pripadajoči IP naslovi, ki jih želimo prilagajati – v našem primeru blokirati – na sistemski ravni. To pomeni, da so pripadajoči vnosi (tj. domene ali IP naslovi) blokirani na ravni celotnega operacijskega sistema, ne le na ravni posameznih programov (npr. vsakega posameznega brskalnika).

Zaradi tovrstnega rigoroznega blokiranja se v datoteko hosts dodajajo le tisti gostitelji, za katere je potrjeno, da so neželeni (npr. oglasni strežniki) ali nevarni (npr. strežniki z zlonamerno programsko opremo).

<h3>1. Namestitev datoteke</h3>

Številne [variante](https://github.com/StevenBlack/hosts/blob/master/readme.md#list-of-all-hosts-file-variants) datoteke hosts je med drugimi pripravil Steven Black. "Osnovna" varianta z neželenimi gostitelji ("adware + malware") vsebuje več kot 50.000 vnosov. Pred pričetkom uporabe je v sistemih Windows to datoteko treba **najprej stisniti** (kompresirati), da zmanjšamo število vrstic z domenami pod približno 34.000 (ali pa zmanjšamo velikost datoteke pod 1 MB) in se s tem izognemo težavam z omrežjem. **[Kompresirano datoteko je možno prenesti tukaj](https://github.com/betterwebleon/slovenian-list/archive/master.zip)**: v preneseni datoteki "*hosts-master.zip*" se kompresirana datoteka hosts nahaja v istoimenski mapi "*hosts*".

Kompresirano datoteko hosts odpakiramo. Nato jo lahko kar zamenjamo z obstoječo datoteko v sistemu (v kolikor vanjo nismo že predhodno vnašali svojih pravil). Kompresirano datoteko hosts v upravitelju datotek vstavimo na sledečo lokacijo:

- v sistemih **Windows**:<br><code>C:\Windows\System32\Drivers\etc</code>
- v sistemih **Mac OS X**, **iOS**, **Linux** ali **Android**:<br><code>/etc/hosts</code>

Za tem ponovno zaženemo računalnik in datoteka *hosts* bo samodejno osvežena. Namesto ponovnega zagona pa lahko zadevo usposobimo na hitrejši način:
- v sistemih **Windows** odpremo Ukazni poziv (cmd.exe) kot administrator in zaženemo ukaz:<br><code>ipconfig /flushdns</code>
- v sistemih **Mac OS X** odpremo Terminal in zaženemo ukaz:<br><code>sudo dscacheutil -flushcache;sudo killall -HUP mDNSResponder</code>
- v sistemih **Linux Debian / Ubuntu** odpremo Terminal in z administratorskimi pravicami zaženemo ukaz:<br><code>sudo /etc/rc.d/init.d/nscd restart</code>
- v sistemih **Linux s systemd** odpremo Terminal in z administratorskimi pravicami zaženemo ukaz:<br><code>sudo systemctl restart network.service</code>
- v sistemih **Fedora Linux** ali **Arch Linux / Manjaro** odpremo Terminal in z administratorskimi pravicami zaženemo ukaz:<br><code>sudo systemctl restart NetworkManager.service</code>

Zapremo okno. V kolikor imamo odprt brskalnik, ga zapremo in ponovno zaženemo.

<h3>2. Navodila za kompresiranje datoteke v lastni režiji v sistemu Microsoft Windows</h3>

1. Prenesi najnovejšo različico programa Python (oz. mora le-ta biti različice najmanj 3.5). Originalna stran s prenosi za OS Windows **[je tukaj](https://www.python.org/downloads/windows/release)**.
2. Po končanem prenosu zaženi namestitveno datoteko: **najprej** izberi (obkljukaj) možnost "*Add Python to PATH*" in šele nato klikni na "*Install Now*".
3. Prenesi **[najnovejši repozitorij hosts datoteke](https://github.com/StevenBlack/hosts/archive/master.zip)** in odpakiraj celotno vsebino datoteke "hosts-master.zip". V našem primeru smo pripadajočo mapo "*hosts-master*" odpakirali kar neposredno na disk C:\ (torej v nobeno od podmap C diska).
4. Zaženi cmd.exe (Ukazni poziv), vanj vnesi sledeči ukaz in nato pritisni enter:<br>
<code>python -m pip install --user -r C:\hosts-master\requirements.txt</code>
5. Zapri cmd.exe and ponovno zaženi računalnik.
6. Odpri cmd.exe and v njem vnašaj sledeče ukaze. Po vnosu vsakega od sledečih dveh ukazov pritisni tipko enter:<br>
<code>cd C:\hosts-master</code><br>
<code>python updateHostsFile.py -a -c</code>
7. Po končanem postopku zapri okno Ukaznega poziva. Kompresirano datoteko hosts sedaj najdeš na lokaciji <code>C:\hosts-master</code>. Kopiraj oz. premakni jo na želeno mesto – za zamenjavo obstoječe (predhodne) hosts datoteke torej na <code>C:\Windows\System32\Drivers\etc</code>. Nato lahko mapo "hosts-master" na C disku izbrišeš.

Pri vsakem nadaljnjem kompresiranju datoteke hosts nato sledimo navodilom samo v točkah 3., 6. in 7.

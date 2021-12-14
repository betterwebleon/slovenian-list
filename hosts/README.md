<h2>Datoteka hosts</h2>

Kot pojasnjuje [Steven Black](https://github.com/StevenBlack/hosts/blob/master/readme.md), gre pri *hosts* za besedilno datoteko (ki je brez datotečne pripone), v kateri se izbranim imenom gostiteljev (angl. hostnames) določijo pripadajoči IP naslovi, ki jih želimo prilagajati – v našem primeru blokirati – na sistemski ravni. To pomeni, da so pripadajoči vnosi (tj. domene ali IP naslovi) blokirani na ravni celotnega operacijskega sistema, ne le na ravni posameznih programov (npr. vsakega posameznega brskalnika).

Zaradi tovrstnega rigoroznega blokiranja se v datoteko hosts dodajajo le tisti gostitelji, za katere je potrjeno, da so neželeni (npr. oglasni strežniki) ali nevarni (npr. strežniki z zlonamerno programsko opremo).

<h3>1. Namestitev datoteke</h3>

Številne [variante](https://github.com/StevenBlack/hosts/blob/master/readme.md#list-of-all-hosts-file-variants) datoteke hosts je med drugimi pripravil Steven Black. "Osnovna" varianta z neželenimi gostitelji ("adware + malware") vsebuje več kot 90.000 vnosov. Pred pričetkom uporabe je v sistemih Windows to datoteko priporočljivo **najprej stisniti** (kompresirati), da zmanjšamo število vrstic z domenami. **[Kompresirano datoteko je možno prenesti tukaj](https://github.com/betterwebleon/slovenian-list/archive/master.zip)**: v preneseni datoteki "*hosts-master.zip*" se kompresirana datoteka hosts nahaja v istoimenski mapi "*hosts*".

Kompresirano datoteko hosts odpakiramo. Nato jo lahko kar zamenjamo z obstoječo datoteko v sistemu (v kolikor vanjo nismo že predhodno vnašali svojih pravil). Kompresirano datoteko hosts v upravitelju datotek vstavimo na sledečo lokacijo:

- v sistemih **Windows**:<br><code>C:\Windows\System32\drivers\etc</code>
- v sistemih **Mac OS X**, **iOS**, **Linux** ali **Android**:<br><code>/etc/hosts</code>

Za tem ponovno zaženemo računalnik in datoteka *hosts* bo samodejno osvežena. Namesto ponovnega zagona pa lahko zadevo usposobimo na hitrejši način:
- v sistemih **Windows** odpremo Ukazni poziv (cmd.exe) kot administrator in zaženemo ukaz:<br><code>ipconfig /flushdns</code>
- v sistemih **Mac OS X** odpremo Terminal in zaženemo ukaz:<br><code>sudo dscacheutil -flushcache;sudo killall -HUP mDNSResponder</code>
- v sistemih **Linux Debian / Ubuntu** odpremo Terminal in z administratorskimi pravicami zaženemo ukaz:<br><code>sudo /etc/rc.d/init.d/nscd restart</code>
- v sistemih **Linux s systemd** odpremo Terminal in z administratorskimi pravicami zaženemo ukaz:<br><code>sudo systemctl restart network.service</code>
- v sistemih **Fedora Linux** ali **Arch Linux / Manjaro** odpremo Terminal in z administratorskimi pravicami zaženemo ukaz:<br><code>sudo systemctl restart NetworkManager.service</code>

Zapremo okno. V kolikor imamo odprt brskalnik, ga zapremo in ponovno zaženemo.

<h3>2. Navodila za kompresiranje datoteke v lastni režiji v sistemih Microsoft Windows</h3>

1. Prenesemo najnovejšo različico programa Python (oz. mora ta biti različice najmanj 3.5). Originalna stran s prenosi za OS Windows **[je tukaj](https://www.python.org/downloads/windows/release)**.
2. Po končanem prenosu zaženemo namestitveno datoteko: **najprej** označimo (obkljukamo) možnost "*Add Python to PATH*" in šele nato izberemo "*Install Now*".
3. Prenesemo **[najnovejši repozitorij hosts datoteke](https://github.com/StevenBlack/hosts/archive/master.zip)** in odpakiramo celotno vsebino datoteke "hosts-master.zip". V našem primeru smo pripadajočo mapo "*hosts-master*" odpakirali kar neposredno na C disk (torej v nobeno od podmap C diska).
4. Zaženemo cmd.exe (Ukazni poziv), vanj vnesemo sledeči ukaz in nato pritisnemo enter:<br>
<code>python -m pip install --user -r C:\hosts-master\requirements.txt</code>
5. Zapremo cmd.exe in ponovno zaženemo računalnik.
6. Odpremo cmd.exe in v njem vnašamo spodnja dva ukaza. Po vnosu vsakega posameznega ukaza pritisnemo tipko enter:<br>
<code>cd C:\hosts-master</code><br>
<code>python updateHostsFile.py -a -c</code>
7. Po končanem postopku zapremo okno Ukaznega poziva. Kompresirano datoteko hosts sedaj v našem primeru najdemo na lokaciji <code>C:\hosts-master</code>. Kopiramo ali premaknemo jo na želeno mesto – za zamenjavo (predhodne) hosts datoteke torej na lokacijo <code>C:\Windows\System32\drivers\etc</code>. Nato lahko mapo "hosts-master" na C disku izbrišemo.

Pri vsakem nadaljnjem kompresiranju datoteke hosts nato sledimo navodilom samo v točkah 3., 6. in 7.

# slovenian-list
[Slovenska lista](https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/filters.txt) je **regionalen seznam, prvenstveno namenjen za uBlock Origin**. Sestavljajo ga statični kozmetični filtri in filtri sledenja. Lista med drugim krije **[100 najbolj obiskanih slovenskih spletnih strani](http://www.moss-soz.si/si/rezultati_moss/obdobje/)**. Lista je namenjena nezahtevnim uporabnikom, saj samodejno blokira najbolj moteče (oglasne) elemente. Gre za komplementarno listo. To pomeni, da je **za boljši učinek zelo priporočljivo uporabljati tudi druge sezname filtrov skupaj z vsemi ostalimi metodami, ki so opisane spodaj.**

V kolikor katera izmed slovenskih spletnih strani ne deluje pravilno ali pa morda še ni zadovoljivo "očiščena", to prosim poročaj [na tej strani](https://github.com/betterwebleon/slovenian-list/issues) ali pošlji [e-poštno sporočilo](mailto:betterweb.leon@outlook.com). Naj bo brskanje udobno tudi pri pohajkovanju po slovenskih straneh. :)

--------------
**English**

[SVN: Slovenian List](https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/filters.txt) is regional list primarily for uBlock Origin or uBlock, which consists mostly of static cosmetic filters and a few tracking filters. Among others, there are **[100 most popular Slovenian websites](http://www.moss-soz.si/si/rezultati_moss/obdobje/)** included in this list.

The list is **intended for simple users** with a set-and-forget approach. It is a complementary list, so it should be used together with other ad blocking filter lists. Within uBlock Origin, Slovenian list can be turned on in settings within "*3rd-party filters*" tab simply by ticking the "*SVN: Slovenian List*" among regional lists. If you have any suggestions or issues to report, please do it [here](https://github.com/betterwebleon/slovenian-list/issues) or write an [e-mail](mailto:betterweb.leon@outlook.com).

--------------
###1. Priporočljiva razširitev za filtriranje (neželenih) vsebin na spletu
**uBlock Origin**

***Zakaj?*** Ker je učinkovita, nezahtevna, enostavna in brezplačna razširitev ("add-on"). V različnih pogledih je mnogo boljša od ostalih tovrstnih razširitev, med drugim tudi od znanega in požrešnega *AdBlock Plus*, kar je razvidno npr. iz [te primerjave](https://github.com/gorhill/uBlock/wiki/uBlock-vs.-ABP:-efficiency-compared) in iz<br>[tega obširnega testa](https://www.raymond.cc/blog/10-ad-blocking-extensions-tested-for-best-performance/view-all/). Za brskalnik Firefox se uBlock Origin dobi [na tej strani](https://addons.mozilla.org/sl/firefox/addon/ublock-origin/), s klikom na zelen gumb <code>*Dodaj v Firefox*</code>.

###2. Priporočljivi dopolnilni seznami filtrov
**A) Spodnje naročnine na filtre se lahko v okviru dodatnih možnosti razširitve uBlock Origin preprosto vklopijo tako, da se označijo s kljukico znotraj zavihka [*Filtri tretjih oseb*]:**
- uBlock filters
- uBlock filters – Badware risks
- uBlock filters – Block-then-redirect
- uBlock filters – Privacy
- uBlock filters – Unbreak
- Adblock Warning Removal List
- EasyList
- EasyPrivacy
- Fanboy's Enhanced Tracking List
- Malware domains
- Spam404
- SVN: Slovenian List

Večina izmed zgornjih naročnin je najverjetneje že vklopljenih. Preostale s seznama kar pogumno vklopi. Nato se znotraj istega okna pomakni na vrh in klikni na desni zgornji gumb <code>*Uveljavi spremembe*</code>. Nato klikni še na levi zgornji gumb <code>*Posodobi zdaj*</code>. Po nekaj trenutkih se gumb obarva sivo.

**B) Nadalje se lahko vključijo številne dodatne naročnine za še učinkovitejše filtriranje raznovrstne spletne nesnage.**

V uBlock Origin se preprosto dodajo tako, da najprej izberemo spodnje povezave naročnin (povezave seznamov s filtri). Da bo brskanje po spletu manj moteče in bolj hitro, je priporočljivo kopirati vse štiri spodnje povezave naenkrat. Nato jih prilepimo v polje filtrov po meri, ki se nahaja skrajno spodaj v okviru zavihka [*Filtri tretjih oseb*]. Vse dodane (prilepljene) povezave se morajo nahajati v svoji (posamezni) vrstici. Nato kliknemo na gumb <code>*Razčleni*</code>, ki se nahaja neposredno pod poljem filtrov. Za tem kliknemo še na desni zgornji gumb <code>*Uveljavi spremembe*</code>. Na koncu pa kliknemo še na gumb <code>*Posodobi zdaj*</code> levo pri vrhu.

<code>https://<i></i>easylist-downloads.adblockplus.org/adwarefilters.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/metaphoricgiraffe/behind-the-scenes-filters/master/filters.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/betterwebleon/international-list/master/filters.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/metaphoricgiraffe/tracking-filters/master/trackingfilters.txt</code>

*Naročnine so seveda brezplačne, kakor tudi vse ostalo na tej strani.* ;)

###3. Priporočljiv brskalnik
**[Mozilla Firefox](https://www.mozilla.org/sl/firefox/new/)**

***Zakaj?*** Ker ga je možno prilagoditi do te mere, da postane izredno hiter, varen, zaseben in uporabniku prijazen brskalnik.

\* ***Kako?*** V Firefox brskalniku odpri nov zavihek in v naslovno (URL) vrstico vpiši:<br><code>about:config</code>

Pritisni *enter* in potrdi Firefoxovo opozorilo o garanciji. Nato poišči vsa spodnja imena nastavitev. Vsako posamično ime nastavitve kopiraj in prilepi v iskalno vrstico brskalnika znotraj nastavitev. Ko se nastavitev (samodejno) prikaže na seznamu, jo dvoklikni z miško. Na ta način lahko spremenimo vrednosti v takšne, kakršne so navedene spodaj:

|   | IME NASTAVITVE                                                |VREDNOST|
|---|:--------------------------------------------------------------|:------:|
|1. | beacon.enabled                                                | false  |
|2. | browser.safebrowsing.downloads.enabled                        | false  |
|3. | browser.safebrowsing.enabled                                  | false  |
|4. | browser.safebrowsing.malware.enabled                          | false  |
|5. | services.sync.prefs.sync.browser.safebrowsing.enabled         | false  |
|6. | services.sync.prefs.sync.browser.safebrowsing.malware.enabled | false  |
|7. | geo.enabled                                                   | false  |
|8. | layout.css.visited_links_enabled                              | false  |
|9. | network.http.sendSecureXSiteReferrer                          | false  |
|10.| media.peerconnection.enabled                                  | false  |
|11.| media.peerconnection.turn.disable                             | true   |
|12.| privacy.trackingprotection.enabled                            | true   |

*Zgornje nastavitve* ***povečajo predvsem zasebnost***. *Za izboljšanje hitrosti in uporabniške izkušnje na enak način spremeni še spodnje nastavitve:*

|    | IME NASTAVITVE                            |VREDNOST|
|----|:------------------------------------------|:------:|
| 13.| browser.fullscreen.animate                | false  |
| 14.| browser.newtab.url                        | Reset  |
| 15.| full-screen-api.transition-duration.enter |        |
| 16.| full-screen-api.transition-duration.leave |        |
| 17.| full-screen-api.warning.timeout           |   0    |
| 18.| memory.free_dirty_pages                   |  true  |
| 19.| network.http.keep-alive.timeout           |   60   |
| 20.| network.http.pipelining                   |  true  |
| 21.| network.http.pipelining.aggressive        |  true  |
| 22.| network.http.pipelining.maxrequests       |   8    |
| 23.| network.http.pipelining.ssl               |  true  |
| 24.| network.http.proxy.pipelining             |  true  |
| 25.| network.http.request.max-start-delay      |   3    |
| 26.| network.websocket.delay-failed-reconnects | false  |
| 27.| security.dialog_enable_delay              |   0    |

*Vrednost pri nastavitvi številka* ***14*** *ročno vtipkaš.*<br>*Nastavitvi št.* ***15*** *in* ***16*** *naj ne zavzemata nobene vrednosti. Samo izbriši obstoječe vrednosti (številke) v pojavnem oknu in potrdi.*

Za tem, ko vklopiš "Zaščito pred sledenjem" pri nastavitvi št. **12**, nekateri videi / slike / gradniki (widgets) / polja s komentarji, ki izvirajo neposredno iz socialnih omrežij (npr. s Facebooka ali Twitterja), **ne bodo delovali.** Sicer bodo delovali na samem Facebooku oz. Twitterju, njihove povezave na drugih straneh pa ne.

**Če jih želiš vseeno videti, jih preprosto vklopiš v brskalniku.** To narediš tako, da levo zgoraj v naslovni (URL) vrstici brskalnika klikneš na sivo ikono "ščita" takrat, ko boš na tisti strani, kjer želiš videti blokiran video / slike / komentarje / gradnike. Ob kliku na omenjeno ikono se prikaže oblaček. V tem oblačku klikni na gumb <code>*Onemogoči zaščito za to stran*</code>. Stran se bo samodejno osvežila, ikona "ščita" pa bo prekrižana z rdečo črto. Brskalnik bo za to domensko ime (tj. za vse strani v okviru izbrane domene) tudi v prihodnje shranil nastavitve. Tako da teh problemov na spletnih straneh tiste domene ne bo več. Če želiš kljub temu to nastavitev spet ponastaviti (torej ponovno vklopiti zaščito na izbrani strani), samo ponovi postopek (greš na spletno stran želene domene, klikneš na ikono "ščita" in nato v oblačku klikneš na gumb <code>*Omogoči zaščito*</code>).

Za naslednje strani lahko že vnaprej izklopiš Zaščito pred sledenjem (kot je opisano v prejšnjem odstavku), ker lahko sicer včasih - preverjeno - naletiš na nepopoln prikaz spletnih vsebin:
- 24ur.com
- bibaleze.si
- dominvrt.si
- meteo.arso.gov.si
- moski.hudo.com
- moskisvet.com
- planet.si
- zadovoljna.si
- zenska.hudo.com

Mimogrede: "*Zaščita pred sledenjem*" oziroma "*Firefox Tracking Protection*" je zaščitni mehanizem, ki uporabnika varuje pred sledenjem in mnogimi vsiljivimi oglasi. Vgrajen je v Firefox brskalnik in je privzeto omogočen le v načinu zasebnega brskanja. Za "klasično" brskanje pa ga je potrebno ročno vklopiti. Drugi brskalniki takšne vgrajene zaščite nimajo, zato je to edinstvena značilnost brskalnika Firefox. Prednost vgraditve takšnega mehanizma v brskalnik je v tem, da deluje zelo hitro (hitreje in bolje od naknadno nameščenih razširitev ali filtrov).

\* **Vse narejene spremembe v brskalniku je možno kadarkoli ponastaviti.** V nastavitvah brskalnika (*about:config*) se posamične nastavitve ponovno poiščejo, nato se desnim miškinim klikom na vsako nastavitev preko izbora "*Ponastavi*" (v priročnem meniju) zadeva povrne v prvotno stanje. **Kljub temu naj velja opozorilo, da se vse zgoraj opisane počenjajo na lastno odgovornost.** Samo brez panike, smrtno nevarno tudi ni. :)


###4. Datoteka hosts
Pomembna in uporabna stvar za izboljšanje varnosti in osnovno (a učinkovito) blokiranje oglasov je datoteka "*hosts*" (ki je brez datotečne pripone). Kot pojasnjuje [StevenBlack](https://github.com/StevenBlack/hosts/blob/master/readme.md): gre za besedilno datoteko, v katero se izbranim imenom gostiteljev (angl. [hostnames](https://en.wikipedia.org/wiki/Hostname)) določijo pripadajoči [IP naslovi](https://sl.wikipedia.org/wiki/IP-naslov), ki jih želimo prilagajati (v našem primeru blokirati) na sistemski ravni. To pomeni, da vnešena "pravila" učinkujejo na ravni celotnega [operacijskega sistema](https://sl.wikipedia.org/wiki/Operacijski_sistem), ne le na ravni brskalnikov oziroma posameznih programov.

Zaradi tovrstnega rigoroznega blokiranja se torej v datoteko <code>*hosts*</code> dodajo le povezave na tiste gostitelje, za katere je potrjeno, da so neželeni (npr. oglasni strežniki - angl. "ad servers") ali nevarni (npr. strežnike z zlonamerno programsko opremo - angl. "malware servers") in torej niso uporabni. To delo je že opravil StevenBlack, zato si je možno datoteko z več kot 25.000 blokiranimi neželenimi gostitelji [**prenesti tukaj**](https://github.com/StevenBlack/hosts/archive/master.zip) (datoteka <code>hosts</code> se nahaja v mapi "*hosts-master*"). 

Datoteko <code>hosts</code> odpakiramo, nato pa jo lahko kar zamenjamo z obstoječo (v kolikor že vanjo nismo predhodno vnašali svoja pravila). To lahko storimo na posebnem mestu v raziskovalcu datotek:

- v sistemih **Windows** jo kopiramo v: <code>C:\Windows\System32\Drivers\etc</code>
- v sistemih **Mac OS X**, **iOS**, **Linux** ali **Android** jo kopiramo v: <code>/etc/hosts</code>

Za tem lahko ponovno zaženemo računalnik in datoteka <hosts> bo samodejno osvežena. Lahko pa namesto ponovnega zagona vse skupaj usposobimo na hitrejši način:

- V **Windows** sistemih odpri Ukazni poziv (cmd.exe) kot administrator. Nato zaženi:<br><code>ipconfig /flushdns</code>
- V **Mac OS X** sistemih odpri Terminal in zaženi:<br><code>sudo dscacheutil -flushcache;sudo killall -HUP mDNSResponder</code>
- V **Linux Debian / Ubuntu** sistemih odpri Terminal in z administratorskimi pravicami zaženi:<br><code>sudo /etc/rc.d/init.d/nscd restart</code>
- V **Linux with systemd** sistemih odpri Terminal in z administratorskimi pravicami zaženi:<br><code>sudo systemctl restart network.service</code>
- V **Fedora Linux** ali **Arch Linux / Manjaro** sistemih odpri Terminal z administratorskimi pravicami zaženi:<br><code>sudo systemctl restart NetworkManager.service</code>

Zapri okno. Če imaš odprt brskalnik, ga zapri in ponovno zaženi. To je vse.<br>Veselo in varno brskanje :)

--------------
###5. License
This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <http://unlicense.org>

HAVE A NICE DAY. (*This wish is not part of a license anymore. You can however treat it as a special annex to the license.*)

# Slovenian List
[Slovenska lista](https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/filters.txt) (angl. Slovenian List) je **regionalen seznam, prvenstveno namenjen za uBlock Origin**. Sestavljajo ga statični kozmetični filtri in filtri sledenja. Lista med drugim krije **[100 najbolj obiskanih slovenskih spletnih strani](http://www.moss-soz.si/si/rezultati_moss/obdobje/)**. Lista je namenjena nezahtevnim uporabnikom, saj na osnovi ustrezne razširitve blokira najbolj moteče oglasne in pojavne elemente. Gre za komplementarno listo. To pomeni, da je **za boljši učinek zelo priporočljivo uporabljati tudi druge sezname filtrov skupaj z ostalimi metodami, ki so opisane spodaj**.

V kolikor katera izmed slovenskih spletnih strani ne deluje pravilno ali pa morda še ni zadovoljivo "očiščena", to prosim sporoči [na tej strani](https://github.com/betterwebleon/slovenian-list/issues) ali napiši [e-poštno sporočilo](mailto:betterweb.leon@outlook.com). Naj bo brskanje udobno tudi pri pohajkovanju po slovenskih straneh. :)

--------------
#### English
[Slovenian List](https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/filters.txt) is regional list primarily for uBlock Origin. The list consists mostly of static cosmetic filters and a few tracking filters. Among others, there are **[100 most popular Slovenian websites](http://www.moss-soz.si/si/rezultati_moss/obdobje/)** included in this list.

The list is **intended for simple users** with a set-and-forget approach. It is a complementary list, so it should be used together with other filter lists. In the case of uBlock Origin, Slovenian list can be found in settings within "*3rd-party filters*" tab (among regional lists), where it is titled "*SVN: Slovenian List*". If you have any suggestions or issues to report, please do it [here](https://github.com/betterwebleon/slovenian-list/issues) or write an [e-mail](mailto:betterweb.leon@outlook.com).

--------------
### 1. Priporočljiv brskalnik
**[Mozilla Firefox](https://www.mozilla.org/firefox/new/)**

***Zakaj?*** Ker ga je možno prilagoditi do te mere, da postane izredno hiter, varen, zaseben in uporabniku prijazen brskalnik.

\* ***Kako?*** V Firefox brskalniku odpri nov zavihek in v naslovno (URL) vrstico vpiši:<br><code>about:config</code>

Pritisni *enter* in potrdi Firefoxovo opozorilo o garanciji. Nato poišči spodnja imena nastavitev. Vsako posamezno ime nastavitve kopiraj in prilepi v iskalno vrstico brskalnika znotraj nastavitev. Ko se vnesena nastavitev (samodejno) prikaže na seznamu, jo z miško dvoklikni. Na ta način lahko spremenimo vrednosti v takšne, kakršne so navedene spodaj:

|   | IME NASTAVITVE                                                 |VREDNOST|
|---|:---------------------------------------------------------------|:------:|
|1. | beacon.enabled                                                 | false  |
|2. | browser.safebrowsing.downloads.enabled                         | false  |
|3. | browser.safebrowsing.malware.enabled                           | false  |
|4. | services.sync.prefs.sync.browser.safebrowsing.malware.enabled  | false  |
|5. | services.sync.prefs.sync.browser.safebrowsing.phishing.enabled | false  |
|6. | layout.css.visited_links_enabled                               | false  |
|7. | network.http.sendSecureXSiteReferrer                           | false  |
|8. | media.peerconnection.enabled                                   | false  |
|9. | media.peerconnection.turn.disable                              | true   |
|10.| privacy.trackingprotection.enabled                             | true   |

*Zgornje nastavitve* ***povečajo predvsem zasebnost***. *Za povečanje hitrosti delovanja brskalnika na enak način spremeni še spodnje nastavitve:*

|    | IME NASTAVITVE                            |   VREDNOST   |
|----|:------------------------------------------|:------------:|
| 11.| browser.fullscreen.animate                |    false     |
| 12.| browser.newtab.url                        | about:newtab |
| 13.| full-screen-api.transition-duration.enter |     0 0      |
| 14.| full-screen-api.transition-duration.leave |     0 0      |
| 15.| full-screen-api.warning.timeout           |      0       |
| 16.| memory.free_dirty_pages                   |     true     |
| 17.| network.http.keep-alive.timeout           |      60      |
| 18.| network.http.pipelining                   |     true     |
| 19.| network.http.pipelining.aggressive        |     true     |
| 20.| network.http.pipelining.maxrequests       |      8       |
| 21.| network.http.pipelining.ssl               |     true     |
| 22.| network.http.proxy.pipelining             |     true     |
| 23.| network.http.request.max-start-delay      |      4       |
| 24.| network.websocket.delay-failed-reconnects |    false     |
| 25.| security.dialog_enable_delay              |      0       |

*Vrednost pri nastavitvi št.* ***12*** *ročno vtipkaš.*<br>*Nastavitvi št.* ***13*** *in* ***14*** *naj zavzemata dve vrednosti (dve ničli, ločeni s presledkom).*

Za tem, ko vklopiš "Zaščito pred sledenjem" pri nastavitvi št. **10**, nekateri videi / slike / gradniki (widgets) / polja s komentarji, ki izvirajo neposredno iz socialnih omrežij (npr. s Facebooka ali Twitterja), **ne bodo delovali.** Neposredno na samem potralu (Facebook, Twitter) bodo sicer delovali, povezave nanje na drugih straneh pa ne.

**Če jih želiš vseeno videti, jih preprosto vklopiš.** To narediš tako, da levo zgoraj v naslovni (URL) vrstici brskalnika klikneš na sivo ikono ščita takrat, ko boš na tisti strani, kjer želiš videti blokiran video / slike / komentarje / gradnike. Ob kliku na omenjeno ikono se prikaže oblaček. V tem oblačku klikni na gumb <code>*Onemogoči zaščito za to stran*</code>. Stran se bo samodejno osvežila, ikona ščita pa bo prekrižana z rdečo črto. Brskalnik bo za to domensko ime (tj. za vse strani v okviru izbrane domene) tudi v prihodnje shranil nastavitve. Tako da teh problemov na spletnih straneh tiste domene ne bo več. Če želiš kljub temu to nastavitev spet ponastaviti (torej ponovno vklopiti zaščito na izbrani strani), samo ponovi postopek (greš na spletno stran želene domene, klikneš na ikono ščita in nato v oblačku klikneš na gumb <code>*Omogoči zaščito*</code>).

Za naslednje strani lahko že vnaprej izklopiš Zaščito pred sledenjem (kot je opisano v prejšnjem odstavku), ker lahko sicer včasih – preverjeno – naletiš na nepopoln prikaz spletnih vsebin:
- 24ur.com
- bibaleze.si
- dominvrt.si
- meteo.arso.gov.si
- moski.hudo.com
- moskisvet.com
- planet.si
- zadovoljna.si
- zenska.hudo.com

Mimogrede: "*Zaščita pred sledenjem*" (angl. Firefox Tracking Protection) je zaščitni mehanizem, ki uporabnika varuje pred sledenjem in mnogimi vsiljivimi oglasi. Vgrajen je v Firefox brskalnik in je privzeto omogočen le v načinu zasebnega brskanja. Za "klasično" brskanje pa ga je potrebno ročno vklopiti. Drugi brskalniki takšne vgrajene zaščite nimajo, zato je to edinstvena značilnost brskalnika Firefox. Prednost vgraditve takšnega mehanizma v brskalnik je v tem, da deluje zelo hitro (hitreje in bolje od naknadno nameščenih razširitev). Kljub temu pa za najboljši učinek velja v brskalnik namestiti še druge razširitve, ki so opisane v nadaljevanju. Vgrajena "Zaščita pred sledenjem" namreč ne blokira drugih neželenih vsebin (npr. številnih oglasov in drugih motečih elementov na spletnih straneh).

\* **Vse narejene spremembe v brskalniku je možno kadarkoli ponastaviti.** V nastavitvah brskalnika (*about:config*) se posamične nastavitve ponovno poiščejo, nato se desnim miškinim klikom na vsako nastavitev preko izbora "*Ponastavi*" (v priročnem meniju) zadeva povrne v prvotno stanje. Kljub temu naj velja opozorilo, da se vse zgoraj opisane nastavitve uveljavljajo *na lastno odgovornost.*

### 2. Priporočljiva razširitev za filtriranje (neželenih) vsebin na spletu
**uBlock Origin**

***Zakaj?*** Ker je učinkovita, nezahtevna, enostavna in brezplačna razširitev ("add-on"). V različnih pogledih je mnogo boljša od ostalih tovrstnih razširitev, med drugim tudi od znanega in požrešnega *AdBlock Plus*, kar je razvidno npr. iz [te primerjave](https://github.com/gorhill/uBlock/wiki/uBlock-vs.-ABP:-efficiency-compared) in iz<br>[tega obširnega testa](https://www.raymond.cc/blog/10-ad-blocking-extensions-tested-for-best-performance/view-all/). uBlock Origin za brskalnik Firefox se dobi [na tej strani](https://addons.mozilla.org/firefox/addon/ublock-origin/) s klikom na moder gumb <code>*Dodaj v Firefox*</code>.

#### 2.a) Priporočljivi dopolnilni seznami filtrov
Spodnje naročnine na filtre se lahko v okviru dodatnih možnosti razširitve uBlock Origin preprosto vklopijo tako, da se označijo s kljukico znotraj zavihka [*Filtri tretjih oseb*]:
- uBlock filters
- uBlock filters – Annoyances
- uBlock filters – Badware risks
- uBlock filters – Privacy
- uBlock filters – Resource abuse
- uBlock filters – Unbreak
- Adblock Warning Removal List
- EasyList
- EasyPrivacy
- Fanboy's Enhanced Tracking List
- Malware domains
- Spam404
- SVN: Slovenian List

Velik del zgornjih naročnin je najverjetneje že privzeto vklopljen. Preostale naročnine s seznama ročno vklopi (obkljukaj). Nato v desnem zgornjem kotu okna izberi oranžen gumb <code>*Uveljavi spremembe*</code>. Nato se pomakni na vrh strani in v levem zgornjem delu okna klikni še na gumb <code>*Posodobi zdaj*</code>. Po nekaj trenutkih se bo ta gumb obarval sivo.

#### 2.b) Priporočljivi dodatni dopolnilni seznami filtrov
Nadalje se lahko ročno vključijo številne dodatne naročnine za še učinkovitejše filtriranje raznovrstne spletne nesnage.

V uBlock Origin se preprosto dodajo tako, da najprej izberemo spodnje povezave naročnin (povezave seznamov s filtri). Da bo brskanje po spletu manj moteče in bolj hitro, je priporočljivo kopirati vseh devet spodnjih povezav *naenkrat*. Nato jih prilepimo v polje filtrov, ki se nahaja skrajno spodaj v okviru zavihka [*Filtri tretjih oseb*]. Vse dodane (prilepljene) povezave se morajo nahajati v svoji (posamezni) vrstici. Na koncu v desnem zgornjem delu okna kliknemo na oranžen gumb <code>*Uveljavi spremembe*</code>.

<code>https://<i></i>gist.githubusercontent.com/gorhill/ef1b62d606473c68d524/raw/90edb7864ee40d49c8f29ad4f2f1aded08e60c6c/gistfile1.txt</code><br>
<code>https://<i></i>easylist-downloads.adblockplus.org/adwarefilters.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/Yhonay/antipopads/master/popads.txt</code><br>
<code>https://<i></i>adguard.com/en/filter-rules.html?id=2</code><br>
<code>https://<i></i>raw.githubusercontent.com/betterwebleon/international-list/master/filters.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/hoshsadiq/adblock-nocoin-list/master/nocoin.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/metaphoricgiraffe/tracking-filters/master/trackingfilters.txt</code><br>
<code>https://<i></i>adguard.com/en/filter-rules.html?id=3</code><br>
<code>https://<i></i>raw.githubusercontent.com/IDKwhattoputhere/uBlock-Filters-Plus/master/uBlock-Filters-Plus.txt</code>

*Naročnine so seveda brezplačne, kakor tudi vse ostalo na tej strani.* ;)

### 3. Priporočene razširitve za brskalnik Mozilla Firefox
Spodnje razširitve se lahko namestijo po želji (pripadajoče povezave za namestitev so namenjene uporabnikom brskalnika Firefox). Za nezahtevne uporabnike se toplo priporoča namestitev razširitev št.: **1**, **6**, **8**, **9**, **11** in **13**. Gre za zelo koristne razširitve, ki ne zahtevajo veliko časa za njihovo namestitev in nastavitev. Hkrati pa občutno izboljšajo in pohitrijo brskanje po spletu.

1. [**au-revoir-utm**](https://addons.mozilla.org/firefox/addon/au-revoir-utm/)
2. [**Classic Theme Restorer**](https://addons.mozilla.org/firefox/addon/classicthemerestorer/)
3. [**Click&Clean**](https://addons.mozilla.org/firefox/addon/clickclean/)
4. [**Download Panel Tweaks**](https://addons.mozilla.org/firefox/addon/download-panel-tweaks/)
5. [**FindBar Tweak**](https://addons.mozilla.org/firefox/addon/findbar-tweak/)
6. [**I don't care about cookies**](https://addons.mozilla.org/firefox/addon/i-dont-care-about-cookies/)
7. [**Pocket**](https://mega.nz/#!T5RjHZyb!yXz5Wj-x7lWdRKbcCaMQ0_lZfpI828spmIm_sOEX5Ng)
8. [**uBlock Origin**](https://addons.mozilla.org/firefox/addon/ublock-origin/)
9. [**Undo Close Tab Replacement**](https://addons.mozilla.org/firefox/addon/undo-close-tab-replacement/)
10. [**UnMHT**](https://addons.mozilla.org/firefox/addon/unmht/)
11. [**Webmail Ad Blocker**](https://addons.mozilla.org/firefox/addon/webmail-ad-blocker/)
12. [**X-notifier**](https://addons.mozilla.org/firefox/addon/xnotifier/)
13. [**YouTube High Definition**](https://addons.mozilla.org/firefox/addon/youtube-high-definition/)
14. [**ZenMate Security, Privacy & Unblock VPN**](https://addons.mozilla.org/firefox/addon/zenmate-security-privacy-vpn/)

### 4. Datoteka hosts
Pomembna in uporabna stvar za izboljšanje varnosti in osnovno (a učinkovito) blokiranje oglasov je datoteka "***hosts***". Tudi ta datoteka (ki je brez datotečne pripone) je dopolnilo vsem ostalim prilagoditvam na tej strani. Uporablja se torej skupaj z razširitvijo uBlock Origin.

Kot pojasnjuje [StevenBlack](https://github.com/StevenBlack/hosts/blob/master/readme.md), gre pri *hosts* za besedilno datoteko, v katero se izbranim imenom gostiteljev (angl. [hostnames](https://en.wikipedia.org/wiki/Hostname)) določijo pripadajoči [IP naslovi](https://sl.wikipedia.org/wiki/IP-naslov), ki jih želimo prilagajati (v našem primeru blokirati) na sistemski ravni. To pomeni, da vnešena pravila za izbrane IP naslove učinkujejo na ravni celotnega [operacijskega sistema](https://sl.wikipedia.org/wiki/Operacijski_sistem), ne le na ravni brskalnikov oziroma posameznih programov.

Zaradi tovrstnega rigoroznega blokiranja se torej v datoteko *hosts* dodajo le povezave na tiste gostitelje, za katere je potrjeno, da so neželeni (npr. oglasni strežniki – angl. ad servers) ali nevarni (npr. strežniki z zlonamerno programsko opremo – angl. malware servers). Datoteko *hosts* z najbolj neželenimi gostitelji je že pripravil Steven Black. Omenjeno datoteko z več kot 50.000 blokiranimi neželenimi gostitelji je možno [**prenesti tukaj**](https://github.com/StevenBlack/hosts/archive/master.zip) (datoteka hosts se nahaja v mapi "hosts-master").

Datoteko *hosts* odpakiramo. Nato jo lahko kar zamenjamo z obstoječo verzijo (v kolikor vanjo nismo predhodno že vnašali svoja pravila). To storimo na posebnem mestu v raziskovalcu datotek:

- v sistemih **Windows** jo kopiramo v:<br><code>C:\Windows\System32\Drivers\etc</code>
- v sistemih **Mac OS X**, **iOS**, **Linux** ali **Android** jo kopiramo v:<br><code>/etc/hosts</code>

Za tem lahko ponovno zaženemo računalnik in datoteka *hosts* bo samodejno osvežena. Lahko pa namesto ponovnega zagona vse skupaj usposobimo na hitrejši način:

- V **Windows** sistemih odpri Ukazni poziv (cmd.exe) kot administrator. Nato zaženi sledeči ukaz:<br><code>ipconfig /flushdns</code>
- V **Mac OS X** sistemih odpri Terminal in zaženi:<br><code>sudo dscacheutil -flushcache;sudo killall -HUP mDNSResponder</code>
- V **Linux Debian / Ubuntu** sistemih odpri Terminal in z administratorskimi pravicami zaženi:<br><code>sudo /etc/rc.d/init.d/nscd restart</code>
- V **Linux with systemd** sistemih odpri Terminal in z administratorskimi pravicami zaženi:<br><code>sudo systemctl restart network.service</code>
- V **Fedora Linux** ali **Arch Linux / Manjaro** sistemih odpri Terminal in z administratorskimi pravicami zaženi:<br><code>sudo systemctl restart NetworkManager.service</code>

Zapremo okno. V kolikor imamo odprt brskalnik, ga zapremo in ponovno zaženemo. To je vse.

Veselo in varno brskanje :)

--------------
### License

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or distribute this software, either in source code form or as a compiled binary, for any purpose, commercial or non-commercial, and by any means.

In jurisdictions that recognize copyright laws, the author or authors of this software dedicate any and all copyright interest in the software to the public domain. We make this dedication for the benefit of the public at large and to the detriment of our heirs and successors. We intend this dedication to be an overt act of relinquishment in perpetuity of all present and future rights to this software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to http://unlicense.org

# slovenian-list
**[Slovenska lista](https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/filters.txt) je regionalen seznam za uBlock Origin** (ali za uBlock), ki ga sestavljajo statični kozmetični filtri in filtri sledenja. Lista med drugim krije **[100 najbolj obiskanih slovenskih spletnih strani](http://www.moss-soz.si/si/rezultati_moss/obdobje/)**. Lista je namenjena nezahtevnim uporabnikom, saj blokira najbolj moteče (oglasne) elemente. Gre za komplementarno listo. To pomeni, da je **za boljši učinek zelo priporočljivo uporabljati tudi druge sezname filtrov skupaj z vsemi ostalimi metodami, ki so opisane spodaj.**

V kolikor katera izmed slovenskih spletnih strani ne deluje pravilno ali pa morda še ni zadovoljivo "očiščena", to prosim poročaj [na tej strani](https://github.com/betterwebleon/slovenian-list/issues) ali pošlji [e-poštno sporočilo](mailto:betterweb.leon@outlook.com). Naj bo brskanje udobno tudi pri pohajkovanju po slovenskih straneh. :)

-------------
**English**

[SVN: Slovenian List](https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/filters.txt) is regional list primarily for uBlock Origin or uBlock, which consists mostly of static cosmetic filters and a few tracking filters. Among others, there are **[100 most popular Slovenian websites](http://www.moss-soz.si/si/rezultati_moss/obdobje/)** included in this list.

The list is **intended for simple users** with a set-and-forget approach. It is a complementary list, so it should be used together with other ad blocking filter lists. Within uBlock Origin, Slovenian list can be turned on in settings within "*3rd-party filters*" tab simply by ticking the "*SVN: Slovenian List*" among regional lists. If you have any suggestions or issues to report, please do it [here](https://github.com/betterwebleon/slovenian-list/issues) or write an [e-mail](mailto:betterweb.leon@outlook.com).

-------------
###1. Priporočljiva razširitev za filtriranje (neželenih) vsebin na spletu
**[uBlock Origin](https://addons.mozilla.org/sl/firefox/addon/ublock-origin/)**

***Zakaj?*** Ker je učinkovita, nezahtevna, enostavna in brezplačna razširitev (add-on). V različnih pogledih je mnogo boljša od ostalih tovrstnih razširitev, med drugim tudi od znanega in požrešnega *AdBlock Plus*, kar je razvidno npr. iz [te primerjave](https://github.com/gorhill/uBlock/wiki/uBlock-vs.-ABP:-efficiency-compared) in iz<br>[tega obširnega testa](https://www.raymond.cc/blog/10-ad-blocking-extensions-tested-for-best-performance/view-all/).

###2. Priporočljivi dopolnilni seznami filtrov
**A) Spodnje naročnine na filtre se lahko v razširitvi uBlock Origin preprosto vklopijo tako, da se označijo s kljukico v zavihku [Filtri tretjih oseb]:**
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

Večina izmed zgornjih naročnin je najverjetneje že vklopljenih. Preostale s seznama kar pogumno vklopi. Nato se znotraj istega okna pomakni na vrh in klikni na desni zgornji gumb "*Uveljavi spremembe*". Nato klikni še na levi zgornji gumb "*Posodobi zdaj*". Po nekaj trenutkih se gumb obarva sivo. Sedaj lahko zapreš celoten zavihek nastavitev te razširitve.

**B) Nadalje se lahko vključijo številne dodatne naročnine za še učinkovitejše filtriranje raznovrstne spletne nesnage. V uBlock Origin se preprosto dodajo s klikom na "*subscribe*" (priporočljivo je dodati vseh pet spodnjih naročnin, da bo brskanje po spletu manj moteče in bolj hitro):**

<code>https://<i></i>easylist-downloads.adblockplus.org/adwarefilters.txt</code>
<code>https://<i></i>raw.githubusercontent.com/metaphoricgiraffe/behind-the-scenes-filters/master/filters.txt</code>
<code>https://<i></i>raw.githubusercontent.com/betterwebleon/international-list/master/filters.txt</code>
<code>https://<i></i>raw.github.com/liamja/Prebake/master/obtrusive.txt</code>
<code>https://<i></i>raw.githubusercontent.com/metaphoricgiraffe/tracking-filters/master/trackingfilters.txt</code>

*Naročnine so seveda brezplačne, kakor tudi vse ostalo na tej strani.* ;)

###3. Priporočljiv brskalnik
**[Mozilla Firefox](https://www.mozilla.org/sl/firefox/new/)**

***Zakaj?*** Ker ga je možno prilagoditi do te mere, da postane izredno hiter, varen, zaseben in uporabniku prijazen brskalnik.

\****Kako?*** V Firefox brskalniku odpri nov zavihek in v naslovno (URL) vrstico vpiši:<br><code>about:config</code><br>Pritisni *enter* in potrdi Firefoxovo opozorilo o garanciji. Nato poišči vsa spodnja imena nastavitev. Vsako posamično ime nastavitve kopiraj in prilepi v iskalno vrstico brskalnika znotraj nastavitev. Ko se nastavitev (samodejno) prikaže na seznamu, jo dvoklikni z miško in nato v pojavnem oknu spremeni njeno vrednost v pripadajočo, kakor je navedeno spodaj:

|   | IME NASTAVITVE                       |VREDNOST|
|---|:-------------------------------------|:------:|
|1. | beacon.enabled                       | false  |
|2. | browser.safebrowsing.malware.enabled | false  |
|3. | geo.enabled                          | false  |
|4. | layout.css.visited_links_enabled     | false  |
|5. | network.http.sendSecureXSiteReferrer | false  |
|6. | media.peerconnection.enabled         | false  |
|7. | media.peerconnection.turn.disable    |  true  |
|8. | privacy.trackingprotection.enabled   |  true  |

*Zgornje nastavitve povečajo zgolj varnost in zasebnost. Za izboljšanje hitrosti in uporabniške izkušnje na enak način spremeni še spodnje nastavitve:*

|    | IME NASTAVITVE                            |VREDNOST|
|----|:------------------------------------------|:------:|
| 9. | browser.fullscreen.animate                | false  |
| 10.| browser.newtab.url                        | Reset  |
| 11.| full-screen-api.transition-duration.enter |        |
| 12.| full-screen-api.transition-duration.leave |        |
| 13.| full-screen-api.warning.timeout           |   0    |
| 14.| memory.free_dirty_pages                   |  true  |
| 15.| network.http.keep-alive.timeout           |   60   |
| 16.| network.http.pipelining                   |  true  |
| 17.| network.http.pipelining.aggressive        |  true  |
| 18.| network.http.pipelining.maxrequests       |   8    |
| 19.| network.http.pipelining.ssl               |  true  |
| 20.| network.http.proxy.pipelining             |  true  |
| 21.| network.http.request.max-start-delay      |   3    |
| 22.| network.websocket.delay-failed-reconnects | false  |
| 23.| security.dialog_enable_delay              |   0    |

**Vrednost nastavitve številka 10 vtipkaš.<br>Nastavitvi št. 11 in 12 naj ne zavzemata nobene vrednosti. Samo izbriši obstoječe vrednosti (številke) v pojavnem oknu in potrdi.**

Za tem, ko vklopiš "Zaščito pred sledenjem" oz. "Firefox Tracking Protection" (pri nastavitvi št. 8), nekateri videi / slike / gradniki (oz. "widgets") / polja s komentarji, ki izvirajo neposredno iz socialnih omrežij (npr. s Facebooka ali Twitterja) **ne bodo delovali.** Sicer bodo delovali na samem Facebooku oz. Twitterju, njihove povezave na drugih straneh pa ne. **Če jih želiš vseeno videti, jih preprosto vklopiš v brskalniku.** To narediš tako, da levo zgoraj v naslovni (URL) vrstici brskalnika klikneš na sivo ikono "ščita" takrat, ko boš na tisti strani, kjer želiš videti video / slike / komentarje / widget. Ob kliku na omenjeno ikono se prikaže oblaček. V tem oblačku klikni na gumb "*Onemogoči zaščito za to stran*". Stran se bo samodejno osvežila, ikona "ščita" bo prekrižana z rdečo črto. Brskalnik bo za to domensko ime (tj. za vse strani v okviru neke domene) tudi v prihodnje shranil nastavitve. Tako da teh problemov na tisti strani ne bo več. Če želiš kljub temu to nastavitev kdaj spet ponastaviti (vklopiti zaščito), samo ponovi postopek (greš na spletno stran, klikneš na ikono "ščita" in nato v oblačku klikneš na gumb "*Omogoči zaščito*").

Za naslednje strani lahko že vnaprej izklopiš Zaščito pred sledenjem (kot je opisano v prejšnjem odstavku), ker lahko sicer včasih - preverjeno - naletiš na nepopoln prikaz spletnih vsebin:
- 24ur.com
- bibaleze.si
- dominvrt.si
- gov.si
- moskisvet.com
- planet.si
- zadovoljna.si

Mimogrede: *Zaščita pred sledenjem* oziroma "Firefox Tracking Protection" je zaščitni mehanizem, ki uporabnika varuje pred sledenjem in mnogimi vsiljivimi oglasi. Vgrajen je v Firefox brskalnik in je privzeto omogočen le v načinu zasebnega brskanja. Za "klasično" brskanje pa ga je potrebno ročno vklopiti. Drugi brskalniki takšne vgrajene zaščite nimajo, zato je to edinstvena značilnost brskalnika Firefox. Prednost vgraditve takšnega mehanizma v brskalnik je v tem, da deluje zelo hitro (hitreje od kakršnihkoli naknadno nameščenih razširitev).

\* **Vse narejene spremembe v brskalniku je možno kadarkoli ponastaviti.** V nastavitvah brskalnika (*about:config*) se posamične nastavitve ponovno poiščejo, nato se desnim miškinim klikom na vsako nastavitev preko izbora "Ponastavi" (v priročnem meniju) zadeva povrne v prvotno stanje. **Kljub temu naj velja opozorilo, da se vse zgoraj opisane počenjajo na lastno odgovornost.** Samo brez panike, smrtno nevarno tudi ni. :)

###4. Hosts file
Another very important and useful tweak is the file named "hosts". It is highly recommended to set it up **together** with all aforementioned tweaks. According to [StevenBlack](https://github.com/StevenBlack/hosts/blob/master/readme.md), <code>hosts</code> is a plain-text file used by all operating systems to map hostnames to IP addresses. The <code>hosts</code> is not bound to any browser, so it should work all the time irrespective of the browser or program.

In other words, <code>hosts</code> works on a system level and takes care of all the junk before it even "reaches" a browser. It blocks the whole website and therefore protects user from getting into contact with dangerous websites, full of malware. Further, it greatly improves browsing speed and privacy by blocking access to various known ad servers and data collecting systems. StevenBlack's version of <code>hosts</code> file has been amalgamated with various sources. You can download the file from [here](https://github.com/StevenBlack/hosts/archive/master.zip) (you will find it within the downloaded zip file). Then:

- in Windows, you  place it to the folder <code>C:\Windows\System32\Drivers\etc</code>
- in Mac OS X, iOS, Linux or Android you place it to the folder <code>/etc/hosts</code>

After you are done, the easiest way is to restart the computer. Or you can also do it faster:

- in **Windows**, open the Command Prompt window (cmd.exe) as an Administrator: Then run <code>ipconfig /flushdns</code>
- in **Mac OS X**, open the Terminal and run: <code>sudo dscacheutil -flushcache;sudo killall -HUP mDNSResponder</code>
- in **Linux Debian/Ubuntu**, open the Terminal and run with root privileges: <code>sudo /etc/rc.d/init.d/nscd restart</code>
- in **Linux with systemd**, open the Terminal and run with root privileges: <code>sudo systemctl restart network.service</code>
- in **Fedora Linux** or **Arch Linux/Manjaro**, open the Terminal and run with root privileges:<br><code>sudo systemctl restart NetworkManager.service</code>

Close the window and restart your browser, if it has been opened. That's all. Enjoy browsing :)

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

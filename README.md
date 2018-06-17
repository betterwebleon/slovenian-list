[![license](https://img.shields.io/badge/License-Unlicense-blue.svg)](https://github.com/betterwebleon/slovenian-list/blob/master/LICENSE.txt)
[![last commit](https://img.shields.io/github/last-commit/betterwebleon/slovenian-list.svg)](https://github.com/betterwebleon/slovenian-list/commits/master)

<h1 align="center">Slovenian List</h1>

<h3>English</h3>

[Slovenian List](https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/filters.txt) is regional list primarily for uBlock Origin. The list consists mostly of static cosmetic filters and a few tracking filters. Among others, there are **[100 most popular Slovenian websites](http://www.moss-soz.si/si/rezultati_moss/obdobje/)** included in this list.

The list is **intended for simple users** with a set-and-forget approach. It is a complementary list, so it should be used together with other filter lists. In the case of uBlock Origin, Slovenian list can be found in settings within "*3rd-party filters*" tab (among regional lists), where it is titled "*SVN: Slovenian List*". If you have any suggestions or issues to report, please do it [here](https://github.com/betterwebleon/slovenian-list/issues) or write an [e-mail](mailto:betterweb.leon@outlook.com).
***
[Slovenska lista](https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/filters.txt) (angl. Slovenian List) je **regionalen seznam, prvenstveno namenjen za orodje [uBlock Origin](#2-priporo%C4%8Dljiva-raz%C5%A1iritev-za-filtriranje-ne%C5%BEelenih-vsebin-na-spletu)**. Sestavljajo ga statični kozmetični filtri in filtri sledenja. Lista med drugim krije **[100 najbolj obiskanih slovenskih spletnih strani](http://www.moss-soz.si/si/rezultati_moss/obdobje/)**. Lista je namenjena nezahtevnim uporabnikom, saj na osnovi ustrezne razširitve blokira najbolj moteče oglasne in pojavne elemente. Gre za komplementarno listo. To pomeni, da je **za boljši učinek zelo priporočljivo uporabljati tudi druge sezname filtrov skupaj z ostalimi metodami, ki so opisane spodaj**.

V kolikor katera izmed slovenskih spletnih strani ne deluje pravilno ali pa morda še ni zadovoljivo "očiščena", to prosim sporoči [na tej strani](https://github.com/betterwebleon/slovenian-list/issues) ali napiši [e-poštno sporočilo](mailto:betterweb.leon@outlook.com). Naj bo brskanje udobno tudi pri pohajkovanju po slovenskih straneh. :)
***
<h3>1. Priporočen brskalnik</h3>

**[Mozilla Firefox](https://www.mozilla.org/firefox/new/)**

***Zakaj?*** Ker ga je možno prilagoditi do te mere, da postane izredno hiter, varen, zaseben in uporabniku prijazen brskalnik.

***Kako?*** V Firefox brskalniku odpri nov zavihek in v naslovno (URL) vrstico vpiši:<br><code>about:config</code>

Pritisni *enter* in potrdi Firefoxovo opozorilo o garanciji. Nato poišči spodnja imena nastavitev. Vsako posamezno ime nastavitve kopiraj in prilepi v iskalno vrstico brskalnika znotraj nastavitev. Ko se vnesena nastavitev (samodejno) prikaže na seznamu, jo z miško dvoklikni. Na ta način lahko spremenimo vrednosti v takšne, kakršne so navedene v naslednjih dveh tabelah:

Spodnje nastavitve **povečajo zasebnost:**

|     | IME NASTAVITVE                                                 | VREDNOST |
| --- | :------------------------------------------------------------- | :------: |
| 1.  | beacon.enabled                                                 | false    |
| 2.  | browser.safebrowsing.downloads.enabled                         | false    |
| 3.  | browser.safebrowsing.malware.enabled                           | false    |
| 4.  | experiments.activeExperiment                                   | false    |
| 5.  | experiments.enabled                                            | false    |
| 6.  | experiments.manifest.uri                                       |          |
| 7.  | experiments.supported                                          | false    |
| 8.  | layout.css.visited_links_enabled                               | false    |
| 9.  | media.peerconnection.enabled                                   | false    |
| 10. | media.peerconnection.turn.disable                              | true     |
| 11. | network.allow-experiments                                      | false    |
| 12. | network.http.sendSecureXSiteReferrer                           | false    |
| 13. | privacy.trackingprotection.enabled                             | true     |
| 14. | services.sync.prefs.sync.browser.safebrowsing.malware.enabled  | false    |
| 15. | services.sync.prefs.sync.browser.safebrowsing.phishing.enabled | false    |

*Vrednost (v obliki spletnega naslova) pri nastavitvi št.* ***6*** *preprosto izbriši.*

Za **zvišanje hitrosti** delovanja brskalnika spremeni še spodnje nastavitve:

|     | IME NASTAVITVE                            |   VREDNOST   |
| --- | :---------------------------------------- | :----------: |
| 16. | browser.fullscreen.animate                | false        |
| 17. | browser.newtab.url                        | about:newtab |
| 18. | full-screen-api.transition-duration.enter | 0 0          |
| 19. | full-screen-api.transition-duration.leave | 0 0          |
| 20. | full-screen-api.warning.timeout           | 0            |
| 21. | memory.free_dirty_pages                   | true         |
| 22. | network.http.keep-alive.timeout           | 60           |
| 23. | network.http.pipelining                   | true         |
| 24. | network.http.pipelining.aggressive        | true         |
| 25. | network.http.pipelining.maxrequests       | 8            |
| 26. | network.http.pipelining.ssl               | true         |
| 27. | network.http.proxy.pipelining             | true         |
| 28. | network.http.request.max-start-delay      | 4            |
| 29. | network.websocket.delay-failed-reconnects | false        |
| 30. | security.dialog_enable_delay              | 0            |

*Vrednosti pri nastavitvi št.* ***17*** *in pri vseh nastavitvah s številčnimi vrednostmi prepiši iz zgornje tabele.*<br>*Nastavitvi št.* ***18*** *in* ***19*** *naj zavzemata dve vrednosti (dve ničli, ločeni s presledkom).*

Za tem, ko vklopiš "Zaščito pred sledenjem" pri nastavitvi št. **13**, nekateri videi / slike / gradniki (widgets) / polja s komentarji, ki izvirajo neposredno iz socialnih omrežij (npr. s Facebooka ali Twitterja), **ne bodo delovali**. Neposredno na samem portalu (npr. facebook.com, twitter.com) bodo sicer delovali, povezave nanje na drugih spletnih straneh pa ne.

**Če jih želiš vseeno videti, jih preprosto vklopiš.** To narediš tako, da levo zgoraj v naslovni (URL) vrstici brskalnika klikneš na sivo ikono ščita takrat, ko boš na tisti strani, kjer želiš videti blokiran video / slike / komentarje / gradnike. Ob kliku na omenjeno ikono se prikaže oblaček. V tem oblačku klikni na gumb <code>*Onemogoči zaščito za to stran*</code>. Stran se bo samodejno osvežila, ikona ščita pa bo prekrižana z rdečo črto. Brskalnik bo za to domensko ime (tj. za vse strani v okviru izbrane domene) tudi v prihodnje shranil nastavitve. Tako da teh problemov na spletnih straneh tiste domene ne bo več. Če želiš kljub temu to nastavitev spet ponastaviti (torej ponovno vklopiti zaščito na izbrani strani), samo ponovi postopek (greš na spletno stran želene domene, klikneš na ikono ščita in nato v oblačku klikneš na gumb <code>*Omogoči zaščito*</code>).

Primeri spletnih portalov, na katerih je priporočljivo izklopiti Zaščito pred sledenjem (na zgoraj opisan način), so:
- 24ur.com
- bibaleze.si
- dominvrt.si
- meteo.arso.gov.si
- moski.hudo.com
- moskisvet.com
- planet.si
- zadovoljna.si
- zenska.hudo.com

To je le nekaj primerov slovenskih spletišč, na katerih lahko – preverjeno – v okviru nekaterih člankov naletiš na nepopoln prikaz spletnih vsebin. Zaščito pred sledenjem lahko po potrebi izklopiš na katerikoli strani, kjer omenjena zaščita blokira razne spletne sledilnike.

Mimogrede: "*Zaščita pred sledenjem*" (angl. Firefox Tracking Protection) je zaščitni mehanizem, ki uporabnika varuje pred sledenjem in mnogimi vsiljivimi oglasi. Vgrajen je v Firefox brskalnik in je privzeto omogočen le v načinu zasebnega brskanja. Za "klasično" brskanje pa ga je potrebno ročno vklopiti. Drugi brskalniki takšne vgrajene zaščite nimajo, zato je to edinstvena značilnost brskalnika Firefox. Prednost vgraditve takšnega mehanizma v brskalnik je v tem, da deluje zelo hitro (hitreje in bolje od naknadno nameščenih razširitev). Kljub temu pa za najboljši učinek velja v brskalnik namestiti še druge razširitve, ki so opisane v nadaljevanju. Vgrajena "Zaščita pred sledenjem" namreč ne blokira drugih neželenih vsebin (npr. številnih oglasov in drugih motečih elementov na spletnih straneh).

**Vse narejene spremembe v brskalniku je možno kadarkoli ponastaviti.** V nastavitvah brskalnika (*about:config*) posamezno nastavitev ponovno poiščemo, nanjo kliknemo z desnim miškinim gumbom in v priročnem meniju izberemo "*Ponastavi*". Nastavitev se nato povrne v prvotno (privzeto) stanje. Vseeno naj velja opozorilo, da se vse zgoraj opisane nastavitve uveljavljajo na lastno odgovornost.

<h3>2. Priporočena razširitev za filtriranje (neželenih) vsebin na spletu</h3>

**uBlock Origin**

***Zakaj?*** Ker je učinkovita, nezahtevna, enostavna in brezplačna razširitev ("add-on"). V različnih pogledih je mnogo boljša od ostalih tovrstnih razširitev, med drugim tudi od znanega in požrešnega *AdBlock Plus*, kar je razvidno npr. iz [te primerjave](https://github.com/gorhill/uBlock/wiki/uBlock-vs.-ABP:-efficiency-compared) in iz<br>[tega obširnega testa](https://www.raymond.cc/blog/10-ad-blocking-extensions-tested-for-best-performance/view-all/). uBlock Origin za brskalnik Firefox se dobi **[na tej strani](https://addons.mozilla.org/firefox/addon/ublock-origin/)** s klikom na moder gumb <code>*Dodaj v Firefox*</code>.

<h4>2.a) Priporočeni seznami filtrov</h4>

Spodnje naročnine na filtre se lahko v okviru dodatnih možnosti razširitve uBlock Origin preprosto vklopijo tako, da se označijo s kljukico na zavihku <kbd>Filtri tretjih oseb</kbd>. Seznam vklopljenih naročnin je razviden na sledeči sliki:

<kbd><img src="https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/img/3rd-party-filters-slo.png" /></kbd>

Velik del zgornjih naročnin je najverjetneje že privzeto vklopljen. Preostale naročnine s seznama ročno vklopi (obkljukaj). Nato v desnem zgornjem kotu okna izberi oranžen gumb <code>*Uveljavi spremembe*</code>. Nato se pomakni na vrh strani in v levem zgornjem delu okna klikni še na gumb <code>*Posodobi zdaj*</code>. Po nekaj trenutkih se bo ta gumb obarval sivo.

<h4>2.b) Priporočeni dodatni seznami filtrov</h4>

Nadalje se lahko ročno vključijo številne dodatne naročnine za še učinkovitejše filtriranje raznovrstne spletne nesnage.

V uBlock Origin se preprosto dodajo tako, da najprej izberemo spodnje povezave naročnin (povezave seznamov s filtri). Da bo brskanje po spletu manj moteče in bolj hitro, je priporočljivo v uBlock Origin vključiti še spodnje povezave. Povezave kopiramo in nato prilepimo v polje filtrov, ki se nahaja skrajno spodaj v okviru zavihka <kbd>Filtri tretjih oseb</kbd>. Polje filtrov za vnos povezav se odpre za tem, ko v razdelku "*Po meri*" obkljukamo možnost *Uvozi ...*. Vse dodane (prilepljene) povezave se morajo nahajati v svoji (posamezni) vrstici. Najlažje je, če kopiramo in v polje prilepimo vseh devet spodnjih povezav *naenkrat*. Za tem pa v desnem zgornjem delu okna kliknemo na oranžen gumb <code>*Uveljavi spremembe*</code>.

<code>https://<i></i>adguard.com/en/filter-rules.html?id=2</code><br>
<code>https://<i></i>adguard.com/en/filter-rules.html?id=3</code><br>
<code>https://<i></i>easylist-downloads.adblockplus.org/adwarefilters.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/Yhonay/antipopads/master/popads.txt</code><br>
<code>https://<i></i>gist.githubusercontent.com/gorhill/ef1b62d606473c68d524/raw/f8181faac18cb5172c7c9bca8e5a3b22f0c925d0/gistfile1.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/betterwebleon/international-list/master/filters.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/hoshsadiq/adblock-nocoin-list/master/nocoin.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/metaphoricgiraffe/tracking-filters/master/trackingfilters.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/IDKwhattoputhere/uBlock-Filters-Plus/master/uBlock-Filters-Plus.txt</code>

Po nekaj trenutkih se v razdelku "*Po meri*" pojavi takšen seznam:

<kbd><img src="https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/img/3rd-party-filters-custom-slo.png" /></kbd>

Nastavitve razširitve uBlock Origin lahko na tem mestu zapremo.

*Naročnine so seveda brezplačne, kakor tudi vse ostalo na tej strani.* :)

<h3>3. Priporočene razširitve za brskalnik Mozilla Firefox</h3>

V nadaljevanju so naštete in opisane priporočene razširitve, ki so vsebinsko razdeljene na tri podpoglavja:
- za povečanje zasebnosti brskanja
- za povečanje uporabnosti brskalnika
- za prilagajanje videza (teme) brskalnika

Razširitve se namestijo po želji. Pripadajoče povezave za namestitev so namenjene zgolj uporabnikom brskalnika Firefox. Toplo se priporoča namestitev razširitev vsaj iz prvih dveh tabel – zaradi večje zasebnosti in uporabnosti.

<h4>3.1 Zasebnost</h4>

|     | IME RAZŠIRITVE | FUNKCIJA |
| :-- | :------------: | -------- |
| 1.  | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/521/521554-64.png" width="50" />](https://addons.mozilla.org/firefox/addon/decentraleyes/)<br><b>[Decentraleyes](https://addons.mozilla.org/firefox/addon/decentraleyes/)</b> | Posnema omrežja za dostavo vsebin (angl. content delivery network – CDN). Namen je preprečiti številne zahteve omenjenih omrežij. Razširitev se skuša izogniti velikim omrežjem, ki na spletu ponujajo brezplačne storitve (npr. Google Hosted Libraries, Microsoft Ajax CDN, CDNJS ...). Razširitev deluje tako, da prestreza spletni promet, na osnovi česar najde vire, ki so podprti na lokalni ravni. Če so potrebni viri na voljo na lokalni ravni, jih vrine v okolje. V kolikor nek zahtevan vir ni na voljo na lokalni ravni, pa Decentraleyes pomaga odstraniti občutljive podatke iz odhodne spletne zahteve.<br><b>OPOMBA:</b> uporabniki starejših različic Firefoxa (do različice 56) lahko namestijo <b>[starejšo različico](https://addons.mozilla.org/firefox/addon/decentraleyes/versions/)</b> razširitve. |
| 2.  | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/351/351740-64.png" width="45" />](https://addons.mozilla.org/firefox/addon/google-search-link-fix/)<br><b>[Google search link fix](https://addons.mozilla.org/firefox/addon/google-search-link-fix/)</b> | Preprečuje spreminjanje povezav z rezultati iskanja na spletnih mestih Google in Yandex. Razširitev spletnemu iskalniku preprečuje, da bi pri uporabnikovem kliku na rezultat iskanja spremenil pripadajočo povezavo. Na ta način se lahko povezava brez težav kopira neposredno na straneh spletnega iskalnika. Poleg tega pa spletni iskalnik ne more več učinkovito spremljati nadaljnjih klikov uporabnika. |
| 3.  | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/843/843685-64.png" width="45" />](https://addons.mozilla.org/firefox/addon/neat-url/)<br><b>[Neat URL](https://addons.mozilla.org/firefox/addon/neat-url/)</b> | Iz URL naslovov odstranjuje parametre (npr. UTM parametre za storitev Google Analytics). Različna analitična orodja uporabljajo URL parametre za namene spletne analitike, s čimer sledijo obiskovalcem spletnih strani (npr. za analize časa zadrževanja na posamezni strani, načine navigiranja po straneh ...). |
| 4.  | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/422/422756-64.png" />](https://addons.mozilla.org/firefox/addon/private-tab/)<br><b>[Private Tab](https://addons.mozilla.org/firefox/addon/private-tab/)</b> | Omogoči dodajanje novega zasebnega zavihka tudi v običajnem oknu (ki sicer ni zasebno). Nov zasebni zavihek se odpre s tipkami Ctrl+Alt+P ali z izborom gumba "<i>New Private Tab</i>".<br><b>OPOMBA:</b> ta razširitev zaenkrat ni združljiva z brskalnikom Firefox 57 in novejšimi. |
| 5.  | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/642/642100-64.png" width="43" />](https://addons.mozilla.org/firefox/addon/skip-redirect/)<br><b>[Skip Redirect](https://addons.mozilla.org/firefox/addon/skip-redirect/)</b> | Preskoči posredne strani, ki jih uporabljajo nekatera spletna mesta, preden uporabnika preusmerijo na končno (zahtevano) stran. Posredne strani sicer služijo sledenju uporabnikom (npr. za spremljanje števila uporabnikov, ki so izbrali določeno povezavo). |
| 6.  | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/327/327417-64.png" width="45" />](https://addons.mozilla.org/firefox/addon/smart-referer/)<br><b>[Smart Referer](https://addons.mozilla.org/firefox/addon/smart-referer/)</b> | Vključi t. i. pametne napotitelje. Razširitev samodejno spremeni informacijo o napotitelju (angl. HTTP referer) vsakič, ko uporabnik obišče spletno mesto z drugo domeno. Pri tem je napotitelj spletni naslov, ki ga je uporabnik predhodno obiskal in iz katerega je prišel na trenutno spletno mesto. Smart referer pa informacijo o dejanskem (predhodnem) spletnem naslovu zamenja kar s ciljnim (aktualnim) spletnim naslovom. Na ta način se ustvarja vtis, da je uporabnik na trenutno spletno mesto prišel direktno (recimo z neposrednim vnosom spletnega naslova v brskalnik ali z odprtjem zaznamka) – ne pa iz nekega predhodnega spletnega mesta. S takšnim spreminjanjem informacije o napotitelju uporabnik pridobi več zasebnosti, saj denimo ni mogoče razpoznati, na podlagi katerega iskalnega niza v spletnem iskalniku (oz. iz katerega predhodnega spletnega naslova) je uporabnik v resnici prišel na trenutno spletno mesto. |
| 7.  | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/607/607454-64.png" width="43" />](https://addons.mozilla.org/firefox/addon/ublock-origin/)<br><b>[uBlock Origin](https://addons.mozilla.org/firefox/addon/ublock-origin/)</b> | Filtrira (blokira) poljubne vsebine na spletu. Večinoma se uporablja za zavračanje neželenih vsebin, kot so spletni oglasi in sledilci za sledenje uporabnikov. uBlock Origin se zato mnogokrat označuje kot preprečevalnik oglasov (angl. ad blocker). uBlock Origin je eno najbolj učinkovitih tovrstnih orodij z vidika hitrosti delovanja in porabe sistemskih sredstev. Z uporabo te razširitve se občutno zviša hitrost nalaganja spletnih strani, poveča se njihova preglednost, hkrati pa se lahko (z nekaj dodatnimi nastavitvami) precej omeji tudi sledenje, ki se ga poslužujejo številna spletna mesta. |
| 8.  | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/7/7560-64.png" width="45" />](https://addons.mozilla.org/firefox/addon/webmail-ad-blocker/)<br><b>[Webmail Ad Blocker](https://addons.mozilla.org/firefox/addon/webmail-ad-blocker/)</b> | Blokira oglase in oglasne pasice za znane storitve spletne pošte: Google Mail, Outlook.com (prej Hotmail) in Yahoo Mail. Razširitev je priporočljivo uporabljati hkrati s preprečevalnikom oglasov (npr. uBlock Origin), saj je slednji v tem primeru zmožen blokirati samo spletne oglase, ne pa tudi oglasnih pasic. Webmail Ad Blocker pa je zmožen odpraviti tudi oglasne pasice in s tem povečati preglednost spletišč, ki ponujajo e-poštne storitve. |

<h4>3.2 Uporabnost</h4>

|     | IME RAZŠIRITVE | FUNKCIJA |
| :-- | :------------: | -------- |
| 9.  | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/660/660064-64.png" width ="45" />](https://addons.mozilla.org/firefox/addon/autoplay-no-more/)<br><b>[Autoplay No More](https://addons.mozilla.org/firefox/addon/autoplay-no-more/)</b> | Izklopi funkcijo samodejnega predvajanja (tj. samodejnega skoka na naslednji videoposnetek) na spletnih mestih YouTube, TED in Vimeo. |
| 10. | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/743/743689-64.png" width ="43" />](https://addons.mozilla.org/firefox/addon/bookmarks-manager-and-viewer/)<br><b>[Bookmarks Manager and Viewer](https://addons.mozilla.org/firefox/addon/bookmarks-manager-and-viewer/)</b> | Upravitelj in pregledovalnik zaznamkov. Izbor pripadajočega gumba prikaže ploščo, v kateri je možno iskanje med vsemi shranjenimi zaznamki. Razširitev omogoča urejanje in premikanje zaznamkov, ustvarjanje novih zaznamkov in map ipd. |
| 11. | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/481/481438-64.png" width ="45" />](https://addons.mozilla.org/firefox/addon/i-dont-care-about-cookies/)<br><b>[I don't care about cookies](https://addons.mozilla.org/firefox/addon/i-dont-care-about-cookies/)</b> | Odpravi nadležna obvestila o piškotkih na številnih "okuženih" spletnih mestih. Razširitev odpravi moteče pasice z obvestili, s čimer poveča preglednost in nekoliko skrajša čas nalaganja spletne strani. Zakonodaja EU za spletna mesta, ki so v lasti družb s sedežem v EU, med drugim zahteva, da obiskovalcem ponudijo možnost sprejetja ali zavrnitve oz. preklica soglasja za uporabo piškotkov. Obvestila so zelo nadležna, ker se vse uporabnikove odločitve izničijo ("pozabijo") vsakič, ko piškotke izbrišemo iz naprave. Enako velja za uporabo zasebnega brskanja, v okviru katerega se zgodovina spletnega brskanja ne shranjuje. To pomeni, da se uporabnik z obvestili o piškotkih navadno srečuje vedno znova. Razširitev tovrstna obvestila skrije, kar naredi tako, da samodejno privoli v uporabo piškotkov. Samodejno strinjanje z uporabo piškotkov (ki je sicer včasih pogoj za popolno delovanje pripadajočega spletnega mesta) krni zasebnost, vendar pa se to lahko vseeno kompenzira s hkratno uporabo drugih razširitev (npr. uBlock Origin) in zaščitnih mehanizmov (npr. Zaščita pred sledenjem v brskalniku Firefox). |
| 12. | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/739/739386-64.png" width ="42" />](https://addons.mozilla.org/firefox/addon/in-my-pocket/)<br><b>[In My Pocket](https://addons.mozilla.org/firefox/addon/in-my-pocket/)</b> | In My Pocket je odličen za uporabnike storitve <i>[Pocket](https://getpocket.com/)</i>. Razširitev v naslovno (URL) vrstico brskalnika doda ikono, ki omogoča shranjevanje ali odstranjevanje spletnih mest s storitve <i>Pocket</i>. Poleg tega razširitev omogoča uporabo priročnega seznama z vsemi shranjenimi povezavami do spletnih mest v okviru storitve Pocket. Povezave s seznama je možno odpreti ali odstraniti (sinhronizirano s storitvijo Pocket). Omenjen seznam prikličemo z izborom pripadajočega gumba. Razširitev torej deluje po vzoru uradne (a ukinjene različice) razširitve Pocket, na podlagi katere za uporabo storitve Pocket ni potrebe po neposrednem obiskovanju spletnega mesta getpocket.com. |
| 13. | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/718/718289-64.png" width ="45" />](https://addons.mozilla.org/firefox/addon/mouse-gestures/)<br><b>[Mouse Gesture Events](https://addons.mozilla.org/firefox/addon/mouse-gestures/)</b> | Omogoča brskanje z uporabo priročnih miškinih potez. V nastavitvah razširitve se lahko prilagodijo različne možnosti za navigiranje po spletu z uporabo desnega miškinega gumba v povezavi z gibanjem miške in/ali z uporabo desnega miškinega gumba v povezavi z vrtenjem miškinega koleščka. |
| 14. | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/724/724283-64.png" width ="42" />](https://addons.mozilla.org/firefox/addon/save-page-we/)<br><b>[Save Page WE](https://addons.mozilla.org/firefox/addon/save-page-we/)</b> | Omogoča (lokalno) shranjevanje spletnih strani v eni sami datoteki HTML. Shraniti (arhivirati) je možno celotno spletno stran ali pa samo njene izbrane elemente. Shranjevanje strani s pomočjo Save Page WE je precej bolj praktično od "običajnega" shranjevanja, saj Save page WE celotno razpoložljivo vsebino spletne strani združi v le eno datoteko HTML. Nadalje je uporaba Save Page WE primernejša od shranjevanja spletnih strani v drugih oblikah (npr. v obliki MHT). Shranjevanje spletnih strani v obliki HTML je primernejše od MHT, ker podporo za datoteke HTML brez težav nudijo vsi brskalniki (v nasprotju z datotekami MHT, za katere v splošnem obstaja precej slabša podpora). |
| 15. | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/937/937151-64.png" width ="45" />](https://addons.mozilla.org/firefox/addon/view-image/)<br><b>[View Image](https://addons.mozilla.org/firefox/addon/view-image/)</b> | Ponovno prikaže gumba "Ogled slike" in "Iskanje s sliko" v spletnem iskalniku slik <i>[Google Slike](https://www.google.si/imghp?hl=sl)</i>. Google je namreč leta 2018 ta dva gumba umaknil s svoje storitve zaradi obtožb, da z "bližnjičnimi" gumbi ponuja neposreden dostop do vsebin, ki so avtorsko zaščitene, s tem pa olajšuje tudi možnost njihove kraje. |
| 16. | [<img src="https://addons.cdn.mozilla.net/static/img/addon-icons/posts-64.png" width ="42" />](https://addons.mozilla.org/firefox/addon/youtubes-annotations-no-more/)<br><b>[Youtube's Annotations No More](https://addons.mozilla.org/firefox/addon/youtubes-annotations-no-more/)</b> | Izklopi pripise (angl. annotations) na spletnem mestu YouTube. S tem se poveča preglednost pri ogledovanju videoposnetkov.<br><b>OPOMBA:</b> če bi kljub temu želeli v videoposnetkih videti (oz. klikniti na) pripise, je potrebno to razširitev v seznamu razširitev (začasno) onemogočiti ali pa odstraniti. |

<h4>3.3 Prilagajanje videza</h4>

*Razširitve v spodnji tabeli so združljive samo z brskalnikom Firefox 57 in novejšimi.*

|     | IME RAZŠIRITVE | FUNKCIJA |
| :-- | :------------: | -------- |
| 17. | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/961/961626-64.png" width ="45" />](https://addons.mozilla.org/firefox/addon/envify/)<br><b>[Envify](https://addons.mozilla.org/firefox/addon/envify/)</b> | Spremeni barvo teme brskalnika glede na želen spletni naslov. V možnostih razširitve določimo poljubno barvo teme, ki jo želimo imeti prikazano takrat, ko v brskalniku obiščemo poljubno domeno ali poddomeno. Razširitev nato samodejno obarva temo brskalnika v skladu z vsakim dodeljenim spletnim naslovom. |
| 18. | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/938/938596-64.png" width ="45" />](https://addons.mozilla.org/firefox/addon/native-dark/)<br><b>[[Dark Theme] - Native Dark](https://addons.mozilla.org/firefox/addon/native-dark/)</b> | Privzeto barvo teme brskalnika spremeni v takšno, da se ujema z izbrano barvo poudarkov v samem sistemu. |

<h3>4. Datoteka hosts</h3>

Pomembna in uporabna stvar za izboljšanje varnosti in osnovno (a učinkovito) blokiranje oglasov je datoteka "***hosts***". Tudi ta datoteka (ki je brez datotečne pripone) je dopolnilo vsem ostalim prilagoditvam na tej strani. Uporablja se torej skupaj z razširitvijo uBlock Origin.

Kot pojasnjuje [Steven Black](https://github.com/StevenBlack/hosts/blob/master/readme.md), gre pri *hosts* za besedilno datoteko, v katero se izbranim imenom gostiteljev (angl. hostnames) določijo pripadajoči IP naslovi, ki jih želimo prilagajati (v našem primeru blokirati) na sistemski ravni. To pomeni, da vnešena pravila za izbrane IP naslove učinkujejo na ravni celotnega operacijskega sistema, ne le na ravni brskalnikov oz. posameznih programov.

Zaradi tovrstnega rigoroznega blokiranja se torej v datoteko *hosts* dodajo le povezave na tiste gostitelje, za katere je potrjeno, da so neželeni (npr. oglasni strežniki – angl. ad servers) ali nevarni (npr. strežniki z zlonamerno programsko opremo – angl. malware servers). Datoteko *hosts* z najbolj neželenimi gostitelji je že pripravil Steven Black. Omenjeno datoteko z več kot 50.000 blokiranimi neželenimi gostitelji je možno **[prenesti tukaj](https://github.com/StevenBlack/hosts/archive/master.zip)** (datoteka *hosts* se nahaja v mapi "*hosts-master*").

Datoteko *hosts* odpakiramo. Nato jo lahko kar zamenjamo z obstoječo verzijo (v kolikor vanjo nismo predhodno že vnašali svoja pravila). To storimo na posebnem mestu v raziskovalcu datotek:

- v sistemih **Windows** jo kopiramo v:<br><code>C:\Windows\System32\Drivers\etc</code>
- v sistemih **Mac OS X**, **iOS**, **Linux** ali **Android** jo kopiramo v:<br><code>/etc/hosts</code>

Za tem lahko ponovno zaženemo računalnik in datoteka *hosts* bo samodejno osvežena. Lahko pa namesto ponovnega zagona vse skupaj usposobimo na hitrejši način:
- v sistemih **Windows** odpri Ukazni poziv (cmd.exe) kot administrator. Nato zaženi sledeči ukaz:<br><code>ipconfig /flushdns</code>
- v sistemih **Mac OS X** odpri Terminal in zaženi:<br><code>sudo dscacheutil -flushcache;sudo killall -HUP mDNSResponder</code>
- v sistemih **Linux Debian / Ubuntu** odpri Terminal in z administratorskimi pravicami zaženi:<br><code>sudo /etc/rc.d/init.d/nscd restart</code>
- v sistemih **Linux with systemd** odpri Terminal in z administratorskimi pravicami zaženi:<br><code>sudo systemctl restart network.service</code>
- v sistemih **Fedora Linux** ali **Arch Linux / Manjaro** odpri Terminal in z administratorskimi pravicami zaženi:<br><code>sudo systemctl restart NetworkManager.service</code>

Zapremo okno. V kolikor imamo odprt brskalnik, ga nato zapremo in ponovno zaženemo. To je vse.

Prijetno in varno brskanje!
***
<h3>Licenca</h3>

[Unlicense](https://github.com/betterwebleon/slovenian-list/blob/master/LICENSE.txt).

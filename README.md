[![license](https://img.shields.io/badge/License-Unlicense-blue.svg)](https://github.com/betterwebleon/slovenian-list/blob/master/LICENSE.txt)
[![last commit](https://img.shields.io/github/last-commit/betterwebleon/slovenian-list.svg)](https://github.com/betterwebleon/slovenian-list/commits/master)

<h1 align="center">Slovenian List</h1>

<h3>English</h3>

[Slovenian List](https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/filters.txt) is regional list primarily intended for uBlock Origin. The list consists mostly of static cosmetic filters and a few tracking filters. Among others, there are **[100 most popular Slovenian websites](http://www.moss-soz.si/si/rezultati_moss/obdobje/)** included in this list.

The list is **intended for simple users** with a set-and-forget approach. It is a complementary list, so it should be used together with other filter lists. In the case of uBlock Origin, Slovenian list can be found in settings within "*3rd-party filters*" tab (among regional lists), where it is titled "*SVN: Slovenian List*". If you have any suggestions or issues to report, please do it [here](https://github.com/betterwebleon/slovenian-list/issues) or write an [e-mail](mailto:betterweb.leon@outlook.com).
***
[Slovenska lista](https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/filters.txt) (angl. Slovenian List) je **regionalen seznam, prvenstveno namenjen za razširitev uBlock Origin**. Sestavljajo jo statični kozmetični filtri in filtri sledenja. Lista med drugim krije **[100 najbolj obiskanih slovenskih spletnih strani](http://www.moss-soz.si/si/rezultati_moss/obdobje/)**. Lista je namenjena nezahtevnim uporabnikom, saj na osnovi ustrezne razširitve blokira najbolj moteče oglasne in pojavne elemente. Gre za komplementarno listo: to pomeni, da je **za boljši učinek zelo priporočljivo uporabljati tudi druge sezname filtrov skupaj z ostalimi metodami, ki so opisane spodaj**.

V kolikor katera izmed slovenskih spletnih strani ne deluje pravilno ali pa morda še ni zadovoljivo "očiščena", to prosim sporoči [na tej strani](https://github.com/betterwebleon/slovenian-list/issues) ali napiši [e-poštno sporočilo](mailto:betterweb.leon@outlook.com). Naj bo brskanje udobno tudi pri pohajkovanju po slovenskih straneh. :)
***

**KAZALO**

* [Priporočeni brskalnik](#1-priporočeni-brskalnik)
  * [Navodila za nastavljanje brskalnika](#1a-navodila-za-nastavljanje-brskalnika)
  * [Ponastavljanje spremenjenih nastavitev](#1b-ponastavljanje-spremenjenih-nastavitev)
* [Seznam priporočenih razširitev za brskalnik Firefox](#2-seznam-priporočenih-razširitev-za-brskalnik-firefox)
  * [Zasebnost](#2a-zasebnost)
  * [Uporabnost](#2b-uporabnost)
* [Priporočena razširitev za blokiranje oglasov](#3-priporočena-razširitev-za-filtriranje-neželenih-vsebin-na-spletu)
  * [Priporočeni seznami filtrov](#3a-priporočeni-seznami-filtrov)
  * [Priporočeni dodatni seznami filtrov](#3b-priporočeni-dodatni-seznami-filtrov)
* [Datoteka hosts](#4-datoteka-hosts)
* [Licenca](#licenca)

<h3>1. Priporočeni brskalnik</h3>

**[Mozilla Firefox](https://www.mozilla.org/firefox/new/)**

***Zakaj?*** Ker ga je možno prilagoditi na način, da postane izredno hiter, varen in uporabniku prijazen brskalnik.

***Kako ga optimalno prilagoditi?*** Beri naprej. :)

<h4>1.a) Navodila za nastavljanje brskalnika</h4>

**Nastavitve v sledečih tabelah veljajo za brskalnik Firefox 57 in novejše (torej za serijo Firefox Quantum).**

V brskalniku odpri nov zavihek in v naslovno (URL) vrstico vpiši:<br><code>about:config</code>

Pritisni *enter* in izberi gumb <code>Sprejmem tveganje!</code> Nato poišči spodnje vnose. Vsako posamezno ime vnosa kopiraj in prilepi v iskalno polje znotraj okna z nastavitvami. Vnos se (samodejno) prikaže na seznamu, nato ga z miško dvoklikni. Na ta način lahko spremeniš vrednosti v takšne, kakršne so navedene v naslednjih dveh tabelah:

Spodnje nastavitve **povečajo zasebnost:**

|     | IME VNOSA                                                      | VREDNOST | OPOMBE |
| --- | :------------------------------------------------------------- | :------: | :----- |
| 1.  | beacon.enabled                                                 | false    |        |
| 2.  | browser.safebrowsing.downloads.enabled                         | false    |        |
| 3.  | browser.safebrowsing.malware.enabled                           | false    |        |
| 4.  | browser.safebrowsing.phishing.enabled                          | false    |        |
| 5.  | experiments.activeExperiment                                   | false    | Ustvari nov vnos: glej dodatna pojasnila spodaj. |
| 6.  | experiments.enabled                                            | false    |        |
| 7.  | experiments.manifest.uri                                       |          | Glej dodatna pojasnila spodaj. |
| 8.  | experiments.supported                                          | false    |        |
| 9.  | layout.css.visited_links_enabled                               | false    |        |
| 10. | media.peerconnection.enabled                                   | false    |        |
| 11. | media.peerconnection.turn.disable                              | true     |        |
| 12. | network.allow-experiments                                      | false    |        |
| 13. | privacy.trackingprotection.enabled                             | true     | Glej dodatna pojasnila spodaj. |
| 14. | services.sync.prefs.sync.browser.safebrowsing.malware.enabled  | false    |        |
| 15. | services.sync.prefs.sync.browser.safebrowsing.phishing.enabled | false    |        |

<br>Za **povečanje hitrosti** delovanja brskalnika spremeni še spodnje nastavitve:<br>

|     | IME VNOSA                                  |   VREDNOST   | OPOMBE |
| --- | :----------------------------------------- | :----------: | :----- |
| 16. | browser.download.animateNotifications      | false        |        |
| 17. | dom.animations-api.element-animate.enabled | false        |        |
| 18. | dom.ipc.processCount                       | 1            | ***Pogojno:*** glej dodatna pojasnila spodaj. |
| 19. | full-screen-api.transition-duration.enter  | 0 0          | Glej dodatna pojasnila spodaj. |
| 20. | full-screen-api.transition-duration.leave  | 0 0          | Glej dodatna pojasnila spodaj. |
| 21. | full-screen-api.warning.timeout            | 0            |        |
| 22. | image.mem.animated.discardable             | false        |        |
| 23. | memory.free_dirty_pages                    | true         | Ustvari nov vnos: glej dodatna pojasnila spodaj. |
| 24. | network.http.keep-alive.timeout            | 60           |        |
| 25. | network.http.request.max-start-delay       | 5            |        |
| 26. | network.websocket.delay-failed-reconnects  | false        |        |
| 27. | security.dialog_enable_delay               | 0            |        |

***DODATNA POJASNILA:***
- Vnosa št. **5** in **23**: ta dva vnosa je potrebno najprej ustvariti. Z desnim miškinim gumbom kliknemo kamorkoli v polju s seznamom nastavitev in v priročnem meniju izberemo: *Novo* --> *Logična vrednost*.
- Vnos št. **7**: v seznamu nastavitev dvokliknemo na ta vnos, iz pojavnega okenca izbrišemo povezavo in spremembo potrdimo z izborom gumba "*V redu*".
- Vnos št. **18** je namenjen intenzivnejšemu varčevanju brskalnika z delovnim pomnilnikom (RAM). Vendar pa bo brskalnik v primeru spremembe pripadajoče vrednosti (na 1) morda postal nekoliko manj odziven v scenariju z večjim številom odprtih zavihkov. Spreminjanje te vrednosti je zato koristno predvsem za tiste računalnike, ki imajo vgrajenega manj kot 4 GB RAM-a.
- Vnosa št. **19** in **20**: pri obeh vnosih naj ima pripadajoča vrednost dve številki (dve ničli, ločeni s presledkom).
- Vnos št. **13**: za tem, ko spremenimo pripadajočo vrednost (torej ko vklopimo t. i. Zaščito pred sledenjem), nekateri videi / slike / gradniki (widgets) / polja s komentarji, ki izvirajo neposredno iz socialnih omrežij (npr. s Facebooka ali Twitterja), **ne bodo delovali**. Neposredno na samem portalu (npr. facebook.com, twitter.com) bodo sicer delovali, povezave nanje na drugih spletnih straneh pa ne. **Če jih želimo vseeno videti, na izbranih spletnih mestih preprosto vklopimo zaščito pred sledenjem.** To naredimo tako, da levo zgoraj v naslovni (URL) vrstici brskalnika kliknemo na sivo ikono ščita takrat, ko bomo na tistem spletnem mestu, na katerem želimo videti blokirane videe / slike / komentarje / gradnike. Ob kliku na omenjeno ikono se prikaže oblaček. V tem oblačku kliknemo na gumb <code>Onemogoči zaščito za to stran</code>. Stran se bo samodejno osvežila, ikona ščita pa bo prekrižana z rdečo črto. Brskalnik bo za to domensko ime (tj. za vse strani v okviru izbrane domene) shranil nastavitve. Tako da teh problemov na vseh straneh v okviru izbrane spletne domene v prihodnosti ne bo več. Če želimo kljub temu to nastavitev spet ponastaviti (torej ponovno vklopiti zaščito na izbrani domeni), samo ponovimo postopek (odpremo spletno stran želene domene, kliknemo na ikono prekrižanega ščita in nato v oblačku kliknemo na gumb <code>Omogoči zaščito</code>).

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

To je le nekaj primerov slovenskih spletišč, na katerih lahko – preverjeno – v okviru nekaterih člankov naletimo na nepopoln prikaz spletnih vsebin. Zaščito pred sledenjem lahko po potrebi izklopimo na katerikoli spletni strani, kjer omenjen zaščitni mehanizem blokira elemente, ki so del (koristne) vsebine.

Mimogrede: *Zaščita pred sledenjem* (angl. Firefox Tracking Protection) je zaščitni mehanizem, ki uporabnika varuje pred sledenjem in mnogimi vsiljivimi oglasi. Vgrajen je v brskalnik Firefox in je privzeto omogočen le v načinu zasebnega brskanja. Za delovanje v načinu "klasičnega" brskanja pa ga je potrebno ročno vklopiti. Drugi brskalniki takšne vgrajene zaščite nimajo, zato je to edinstvena značilnost brskalnika Firefox. Prednost takšnega mehanizma, ki je vgrajen v brskalnik, je v tem, da deluje zelo hitro (tj. hitreje od naknadno nameščenih razširitev). Vseeno pa za najboljši učinek velja v brskalnik namestiti še druge razširitve (naštete v [2. poglavju](#2-seznam-priporočenih-razširitev-za-brskalnik-firefox)) in v sistem namestiti datoteko hosts (več o njej v [4. poglavju](#4-datoteka-hosts)). Vgrajena *Zaščita pred sledenjem* namreč ne blokira drugih neželenih vsebin (npr. številnih oglasov in drugih motečih elementov na spletnih straneh).

<h4>1.b) Ponastavljanje spremenjenih nastavitev</h4>

**Narejene spremembe v podrobnih nastavitvah brskalnika Firefox je možno kadarkoli ponastaviti** (vrniti v prvotno stanje): v podrobnih nastavitvah (*about:config*) posamezen vnos ponovno poiščemo, nanj kliknemo z desnim miškinim gumbom in v priročnem meniju izberemo "*Ponastavi*". Vrednost vnosa se bo nato povrnila v prvotno (privzeto) stanje. Kljub temu naj velja opozorilo, da se vse spremembe nastavitev, opisane na tej strani, uveljavljajo na lastno odgovornost.

**Obvestilo v zvezi z ukazi "pipelining":** brskalniki Firefox Quantum (od različice 57 naprej) ne podpirajo več ukazov za cevljenje (angl. pipelining). Če smo v predhodnih različicah brskalnika Firefox te nastavitve spreminjali, lahko morebitne obstoječe vnose ponastavimo (poiščemo jih z iskalnim nizom "pipelining" v naprednih nastavitvah about:config). Ti vnosi bodo nato po ponovnem zagonu brskalnika izbrisani.

<h3>2. Seznam priporočenih razširitev za brskalnik Firefox</h3>

V nadaljevanju so naštete in opisane priporočene razširitve, ki so vsebinsko razdeljene na dve podpoglavji:
- za povečanje zasebnosti brskanja
- za povečanje uporabnosti brskalnika

Posamezne razširitve se namestijo po želji. Pripadajoče povezave za namestitev so namenjene uporabnikom brskalnika **Firefox od različice 60 naprej**.

<h4>2.a) Zasebnost</h4>

|     | IME RAZŠIRITVE | FUNKCIJA |
| :-- | :------------: | -------- |
| 1.  | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/521/521554-64.png" width="50" />](https://addons.mozilla.org/firefox/addon/decentraleyes/)<br><b>[Decentraleyes](https://addons.mozilla.org/firefox/addon/decentraleyes/)</b> | Posnema omrežja za dostavo vsebin (angl. content delivery network – CDN). Namen je preprečiti številne zahteve omenjenih omrežij. Razširitev se skuša izogniti velikim omrežjem, ki na spletu ponujajo brezplačne storitve (npr. Google Hosted Libraries, Microsoft Ajax CDN, CDNJS ...). Razširitev deluje tako, da prestreza spletni promet, na osnovi česar najde vire, ki so podprti na lokalni ravni. Če so potrebni viri na voljo na lokalni ravni, jih vrine v okolje. V kolikor nek zahtevan vir ni na voljo na lokalni ravni, pa Decentraleyes pomaga odstraniti občutljive podatke iz odhodne spletne zahteve.<br><b>OPOMBA:</b> uporabniki starejših različic Firefoxa (do različice 56) lahko namestijo <b>[starejšo različico](https://addons.mozilla.org/firefox/addon/decentraleyes/versions/)</b> razširitve. |
| 2.  | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/351/351740-64.png" width="45" />](https://addons.mozilla.org/firefox/addon/google-search-link-fix/)<br><b>[Google search link fix](https://addons.mozilla.org/firefox/addon/google-search-link-fix/)</b> | Preprečuje spreminjanje povezav z rezultati iskanja na spletnih mestih Google in Yandex. Razširitev spletnemu iskalniku preprečuje, da bi pri uporabnikovem kliku na rezultat iskanja spremenil pripadajočo povezavo. Na ta način se lahko povezava brez težav kopira neposredno na straneh spletnega iskalnika. Poleg tega pa spletni iskalnik ne more več učinkovito spremljati nadaljnjih klikov uporabnika. |
| 3.  | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/843/843685-64.png" width="45" />](https://addons.mozilla.org/firefox/addon/neat-url/)<br><b>[Neat URL](https://addons.mozilla.org/firefox/addon/neat-url/)</b> | Iz URL naslovov odstranjuje parametre (npr. UTM parametre za storitev Google Analytics). Različna analitična orodja uporabljajo URL parametre za namene spletne analitike, s čimer sledijo obiskovalcem spletnih strani (npr. za analize časa zadrževanja na posamezni strani, načine navigiranja po straneh ...). |
| 4.  | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/327/327417-64.png" width="45" />](https://addons.mozilla.org/firefox/addon/smart-referer/)<br><b>[Smart Referer](https://addons.mozilla.org/firefox/addon/smart-referer/)</b> | Vključi t. i. pametne napotitelje. Razširitev samodejno spremeni informacijo o napotitelju (angl. HTTP referer) vsakič, ko uporabnik obišče spletno mesto z drugo domeno. Pri tem je napotitelj spletni naslov, ki ga je uporabnik predhodno obiskal in iz katerega je prišel na trenutno spletno mesto. Smart referer pa informacijo o dejanskem (predhodnem) spletnem naslovu zamenja kar s ciljnim (aktualnim) spletnim naslovom. Na ta način se ustvarja vtis, da je uporabnik na trenutno spletno mesto prišel direktno (recimo z neposrednim vnosom spletnega naslova v brskalnik ali z odprtjem zaznamka) – ne pa iz nekega predhodnega spletnega mesta. S takšnim spreminjanjem informacije o napotitelju uporabnik pridobi več zasebnosti, saj denimo ni mogoče razpoznati, na podlagi katerega iskalnega niza v spletnem iskalniku (oz. iz katerega predhodnega spletnega naslova) je uporabnik v resnici prišel na trenutno spletno mesto. |
| 5.  | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/607/607454-64.png" width="43" />](https://addons.mozilla.org/firefox/addon/ublock-origin/)<br><b>[uBlock Origin](https://addons.mozilla.org/firefox/addon/ublock-origin/)</b> | **Več o tej razširitvi v [3. poglavju](#3-priporočena-razširitev-za-filtriranje-neželenih-vsebin-na-spletu).** Filtrira (blokira) poljubne vsebine na spletu. Večinoma se uporablja za zavračanje neželenih vsebin, kot so spletni oglasi in sledilci za sledenje uporabnikov. uBlock Origin se zato mnogokrat označuje kot preprečevalnik oglasov (angl. ad blocker). uBlock Origin je eno najbolj učinkovitih tovrstnih orodij z vidika hitrosti delovanja in porabe sistemskih sredstev. Z uporabo te razširitve se občutno zviša hitrost nalaganja spletnih strani, poveča se njihova preglednost, hkrati pa se lahko (z nekaj dodatnimi nastavitvami) precej omeji tudi sledenje, ki se ga poslužujejo številna spletna mesta. |
| 6.  | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/7/7560-64.png" width="45" />](https://addons.mozilla.org/firefox/addon/webmail-ad-blocker/)<br><b>[Webmail Ad Blocker](https://addons.mozilla.org/firefox/addon/webmail-ad-blocker/)</b> | Blokira oglase in oglasne pasice za znane storitve spletne pošte: Google Mail, Outlook.com (prej Hotmail) in Yahoo Mail. Razširitev je priporočljivo uporabljati hkrati s preprečevalnikom oglasov (npr. uBlock Origin), saj je slednji v tem primeru zmožen blokirati samo spletne oglase, ne pa tudi oglasnih pasic. Webmail Ad Blocker pa je zmožen odpraviti tudi oglasne pasice in s tem povečati preglednost spletišč, ki ponujajo e-poštne storitve. |

<h4>2.b) Uporabnost</h4>

|     | IME RAZŠIRITVE | FUNKCIJA |
| :-- | :------------: | -------- |
| 7.  | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/909/909373-64.png" width ="45" />](https://addons.mozilla.org/firefox/addon/auto-tab-discard/)<br><b>[Auto Tab Discard](https://addons.mozilla.org/firefox/addon/auto-tab-discard/)</b> | Razširitev je namenjena varčevanju z delovnim pomnilnikom: neaktivni zavihki (torej tisti v ozadju) se po določenem času – privzeto po 10 minutah – samodejno izbrišejo iz pomnilnika (ne pa tudi iz brskalnika), na podlagi česar brskalnik tudi po daljšem času neprenehne uporabe in pri večjem številu odprtih zavihkov ostaja varčen z delovnim pomnilnikom. Namestitev razširitve je zelo priporočljiva za računalnike, ki imajo vgrajenega manj kot 4 GB RAM-a. |
| 8.  | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/660/660064-64.png" width ="45" />](https://addons.mozilla.org/firefox/addon/autoplay-no-more/)<br><b>[Autoplay No More](https://addons.mozilla.org/firefox/addon/autoplay-no-more/)</b> | Izklopi funkcijo samodejnega predvajanja (tj. samodejnega skoka na naslednji videoposnetek) na spletnih mestih YouTube, TED in Vimeo. |
| 9.  | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/743/743689-64.png" width ="43" />](https://addons.mozilla.org/firefox/addon/bookmarks-manager-and-viewer/)<br><b>[Bookmarks Manager and Viewer](https://addons.mozilla.org/firefox/addon/bookmarks-manager-and-viewer/)</b> | Upravitelj in pregledovalnik zaznamkov. Izbor pripadajočega gumba prikaže ploščo, v kateri je možno iskanje med vsemi shranjenimi zaznamki. Razširitev omogoča urejanje in premikanje zaznamkov, ustvarjanje novih zaznamkov in map ipd. |
| 10. | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/481/481438-64.png" width ="45" />](https://addons.mozilla.org/firefox/addon/i-dont-care-about-cookies/)<br><b>[I don't care about cookies](https://addons.mozilla.org/firefox/addon/i-dont-care-about-cookies/)</b> | Odpravi nadležna obvestila o piškotkih na številnih "okuženih" spletnih mestih. Razširitev odpravi moteče pasice z obvestili, s čimer poveča preglednost in nekoliko skrajša čas nalaganja spletne strani. Zakonodaja EU za spletna mesta, ki so v lasti družb s sedežem v EU, med drugim zahteva, da obiskovalcem ponudijo možnost sprejetja ali zavrnitve oz. preklica soglasja za uporabo piškotkov. Obvestila so zelo nadležna, ker se vse uporabnikove odločitve izničijo ("pozabijo") vsakič, ko piškotke izbrišemo iz naprave. Enako velja za uporabo zasebnega brskanja, v okviru katerega se zgodovina spletnega brskanja ne shranjuje. To pomeni, da se uporabnik z obvestili o piškotkih navadno srečuje vedno znova. Razširitev tovrstna obvestila skrije, kar naredi tako, da samodejno privoli v uporabo piškotkov. Samodejno strinjanje z uporabo piškotkov (ki je sicer včasih pogoj za popolno delovanje pripadajočega spletnega mesta) krni zasebnost, vendar pa se to lahko vseeno kompenzira s hkratno uporabo drugih razširitev (npr. uBlock Origin) in zaščitnih mehanizmov (npr. Zaščita pred sledenjem v brskalniku Firefox). |
| 11. | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/739/739386-64.png" width ="42" />](https://addons.mozilla.org/firefox/addon/in-my-pocket/)<br><b>[In My Pocket](https://addons.mozilla.org/firefox/addon/in-my-pocket/)</b> | In My Pocket je odličen za uporabnike storitve *[Pocket](https://getpocket.com/)*. Razširitev v naslovno (URL) vrstico brskalnika doda ikono, ki omogoča shranjevanje ali odstranjevanje spletnih mest s storitve *Pocket*. Poleg tega razširitev omogoča uporabo priročnega seznama z vsemi shranjenimi povezavami do spletnih mest v okviru storitve Pocket. Povezave s seznama je možno odpreti ali odstraniti (sinhronizirano s storitvijo Pocket). Omenjen seznam prikličemo z izborom pripadajočega gumba. Razširitev torej deluje po vzoru uradne (a ukinjene različice) razširitve Pocket, na podlagi katere za uporabo storitve Pocket ni potrebe po neposrednem obiskovanju spletnega mesta getpocket.com. |
| 12. | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/718/718289-64.png" width ="45" />](https://addons.mozilla.org/firefox/addon/mouse-gestures/)<br><b>[Mouse Gesture Events](https://addons.mozilla.org/firefox/addon/mouse-gestures/)</b> | Omogoča brskanje z uporabo priročnih miškinih potez. V nastavitvah razširitve se lahko prilagodijo različne možnosti za navigiranje po spletu z uporabo desnega miškinega gumba v povezavi z gibanjem miške in/ali z uporabo desnega miškinega gumba v povezavi z vrtenjem miškinega koleščka. |
| 13. | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/724/724283-64.png" width ="42" />](https://addons.mozilla.org/firefox/addon/save-page-we/)<br><b>[Save Page WE](https://addons.mozilla.org/firefox/addon/save-page-we/)</b> | Omogoča (lokalno) shranjevanje spletnih strani v eni sami datoteki HTML. Shraniti (arhivirati) je možno celotno spletno stran ali pa samo njene izbrane elemente. Shranjevanje strani s pomočjo Save Page WE je precej bolj praktično od "običajnega" shranjevanja, saj Save page WE celotno razpoložljivo vsebino spletne strani združi v le eno datoteko HTML. Nadalje je uporaba Save Page WE primernejša od shranjevanja spletnih strani v drugih oblikah (npr. v obliki MHT). Shranjevanje spletnih strani v obliki HTML je primernejše od MHT, ker podporo za datoteke HTML brez težav nudijo vsi brskalniki (v nasprotju z datotekami MHT, za katere v splošnem obstaja precej slabša podpora). |
| 14. | [<img src="https://addons.cdn.mozilla.net/user-media/addon_icons/937/937151-64.png" width ="45" />](https://addons.mozilla.org/firefox/addon/view-image/)<br><b>[View Image](https://addons.mozilla.org/firefox/addon/view-image/)</b> | Ponovno prikaže gumba <code>Ogled slike</code> in <code>Iskanje s sliko</code> v spletnem iskalniku slik *[Google Slike](https://www.google.si/imghp?hl=sl)*. Google je namreč leta 2018 ta dva gumba umaknil s svoje storitve zaradi obtožb, da z "bližnjičnimi" gumbi ponuja neposreden dostop do vsebin, ki so avtorsko zaščitene, s tem pa olajšuje tudi možnost njihove kraje. |
| 15. | [<img src="https://addons.cdn.mozilla.net/static/img/addon-icons/posts-64.png" width ="42" />](https://addons.mozilla.org/firefox/addon/youtubes-annotations-no-more/)<br><b>[Youtube's Annotations No More](https://addons.mozilla.org/firefox/addon/youtubes-annotations-no-more/)</b> | Izklopi pripise (angl. annotations) na spletnem mestu YouTube. S tem se poveča preglednost pri ogledovanju videoposnetkov.<br><b>OPOMBA:</b> če bi kljub temu želeli v videoposnetkih videti (oz. klikniti na) pripise, je potrebno to razširitev v seznamu razširitev (začasno) onemogočiti ali pa odstraniti. |

<h3>3. Priporočena razširitev za filtriranje (neželenih) vsebin na spletu</h3>

**uBlock Origin**

***Zakaj?*** Ker je učinkovita, nezahtevna, enostavna in brezplačna razširitev ("add-on"). V različnih pogledih je mnogo boljša od ostalih tovrstnih razširitev, med drugim tudi od znanega in požrešnega *AdBlock Plus*, kar je razvidno npr. iz [te primerjave](https://github.com/gorhill/uBlock/wiki/uBlock-vs.-ABP:-efficiency-compared) in iz [tega obširnega testa](https://www.raymond.cc/blog/10-ad-blocking-extensions-tested-for-best-performance/view-all/).
<br><br>Povezave za namestitev razširitve uBlock Origin:

- <b>[Dodatki za Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)</b> za brskalnik Mozilla Firefox
- <b>[Spletna trgovina Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)</b> za brskalnike Google Chrome, Vivaldi in ostale, ki temeljijo na Chromiumu
- <b>[Opera add-ons](https://addons.opera.com/extensions/details/ublock/)</b> za brskalnik Opera

<h4>3.a) Priporočeni seznami filtrov</h4>

Spodnje naročnine na filtre se lahko v okviru dodatnih možnosti razširitve uBlock Origin preprosto vklopijo tako, da se označijo s kljukico na zavihku <kbd>Filtri tretjih oseb</kbd>. Seznam vklopljenih naročnin je razviden na sledeči sliki:

<kbd><img src="https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/img/3rd-party-filters-slo.png" /></kbd>

Velik del zgornjih naročnin je najverjetneje že privzeto vklopljen. Preostale naročnine s seznama ročno vklopi (obkljukaj). Nato v desnem zgornjem kotu okna izberi oranžen gumb <code>Uveljavi spremembe</code>. Nato se pomakni na vrh strani in v levem zgornjem delu okna klikni še na gumb <code>Posodobi zdaj</code>. Po nekaj trenutkih se bo ta gumb obarval sivo.

<h4>3.b) Priporočeni dodatni seznami filtrov</h4>

Nadalje se lahko ročno vključijo številne dodatne naročnine za še učinkovitejše filtriranje raznovrstne spletne nesnage.

V uBlock Origin se preprosto dodajo tako, da najprej izberemo spodnje povezave naročnin (povezave seznamov s filtri). Da bo brskanje po spletu manj moteče in bolj hitro, je priporočljivo v uBlock Origin vključiti še spodnje povezave. Povezave kopiramo in nato prilepimo v polje filtrov, ki se nahaja skrajno spodaj v okviru zavihka <kbd>Filtri tretjih oseb</kbd>. Polje filtrov za vnos povezav se odpre za tem, ko v razdelku *Po meri* obkljukamo možnost "*Uvozi ...*". Vse dodane (prilepljene) povezave se morajo nahajati v svoji (posamezni) vrstici. Najlažje je, če kopiramo in v polje prilepimo vseh devet spodnjih povezav *naenkrat*. Za tem pa v desnem zgornjem delu okna kliknemo na oranžen gumb <code>Uveljavi spremembe</code>.

<code>https://<i></i>adguard.com/en/filter-rules.html?id=2</code><br>
<code>https://<i></i>adguard.com/en/filter-rules.html?id=3</code><br>
<code>https://<i></i>easylist-downloads.adblockplus.org/adwarefilters.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/Yhonay/antipopads/master/popads.txt</code><br>
<code>https://<i></i>gist.githubusercontent.com/gorhill/ef1b62d606473c68d524/raw/f8181faac18cb5172c7c9bca8e5a3b22f0c925d0/gistfile1.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/betterwebleon/international-list/master/filters.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/hoshsadiq/adblock-nocoin-list/master/nocoin.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/metaphoricgiraffe/tracking-filters/master/trackingfilters.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/IDKwhattoputhere/uBlock-Filters-Plus/master/uBlock-Filters-Plus.txt</code>

Po nekaj trenutkih se v razdelku *Po meri* pojavi takšen seznam:

<kbd><img src="https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/img/3rd-party-filters-custom-slo.png" /></kbd>

Nastavitve razširitve uBlock Origin lahko na tem mestu zapremo.

*Naročnine so seveda brezplačne, kakor tudi vse ostalo na tej strani.* :)

<h3>4. Datoteka hosts</h3>

Pomembna in uporabna stvar za izboljšanje varnosti in osnovno (a učinkovito) blokiranje oglasov je datoteka "***hosts***". Tudi ta datoteka (ki je brez datotečne pripone) je dopolnilo vsem ostalim prilagoditvam na tej strani. Uporablja se torej skupaj z razširitvijo uBlock Origin.

Kot pojasnjuje [Steven Black](https://github.com/StevenBlack/hosts/blob/master/readme.md), gre pri *hosts* za besedilno datoteko, v katero se izbranim imenom gostiteljev (angl. hostnames) določijo pripadajoči IP naslovi, ki jih želimo prilagajati (v našem primeru blokirati) na sistemski ravni. To pomeni, da vnešena pravila za izbrane IP naslove učinkujejo na ravni celotnega operacijskega sistema, ne le na ravni brskalnikov in drugih programov.

Zaradi tovrstnega rigoroznega blokiranja se torej v datoteko *hosts* dodajo le povezave na tiste gostitelje, za katere je potrjeno, da so neželeni (npr. oglasni strežniki – angl. ad servers) ali nevarni (npr. strežniki z zlonamerno programsko opremo – angl. malware servers). Datoteko *hosts* z najbolj neželenimi gostitelji je že pripravil Steven Black. Omenjeno datoteko z več kot 50.000 blokiranimi neželenimi gostitelji je možno **[prenesti tukaj](https://github.com/StevenBlack/hosts/archive/master.zip)** (datoteka *hosts* se nahaja v preneseni mapi "*hosts-master*").

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

[![license](https://img.shields.io/badge/License-Unlicense-blue.svg)](https://github.com/betterwebleon/slovenian-list/blob/master/LICENSE.txt)
[![last commit](https://img.shields.io/github/last-commit/betterwebleon/slovenian-list.svg)](https://github.com/betterwebleon/slovenian-list/commits/master)

<h1 align="center">Slovenian List</h1>

<h3>English</h3>

[Slovenian List](https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/filters.txt) is regional list primarily intended for uBlock Origin. The list consists mostly of static cosmetic filters and a few tracking filters. Among others, it includes **[the most popular Slovenian websites](https://www.moss-soz.si/rezultati/)**.

The list is **intended for simple users** with a set-and-forget approach. It is a complementary list, so it should be used together with other filter lists. In the case of uBlock Origin, Slovenian list can be found in settings within "*3rd-party filters*" tab (among regional lists), where it is titled "*SVN: Slovenian List*". If you have any suggestions or issues to report, please do it [here](https://github.com/betterwebleon/slovenian-list/issues) or write an [e-mail](mailto:betterweb.leon@outlook.com).
***
[Slovenska lista](https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/filters.txt) (angl. Slovenian List) je **regionalen seznam, prvenstveno namenjen za dodatek uBlock Origin**. Sestavljajo jo statični kozmetični filtri in filtri sledenja. Lista med drugim krije **[najbolj obiskane slovenske spletne strani](https://www.moss-soz.si/rezultati/)**. Lista je namenjena nezahtevnim uporabnikom, saj na osnovi ustreznega dodatka blokira najbolj moteče oglasne in pojavne elemente. Gre za komplementarno listo: to pomeni, da je **za boljši učinek zelo priporočljivo uporabljati tudi druge sezname filtrov skupaj z ostalimi metodami, ki so opisane spodaj**.

V kolikor katera izmed slovenskih spletnih strani ne deluje pravilno ali pa morda še ni zadovoljivo "očiščena", to prosim sporoči [na tej strani](https://github.com/betterwebleon/slovenian-list/issues) ali napiši [e-poštno sporočilo](mailto:betterweb.leon@outlook.com). Naj bo brskanje udobno tudi pri pohajkovanju po slovenskih straneh. :)
***

<br>

**KAZALO**

* [Priporočeni brskalnik za namizni računalnik: Mozilla Firefox](#1-priporočeni-brskalnik-za-namizni-računalnik-mozilla-firefox)
  * [Optimizacija nastavitev brskalnika](#1a-optimizacija-nastavitev-brskalnika)
  * [Izboljšana zaščita pred sledenjem](#1b-izboljšana-zaščita-pred-sledenjem)
* [Seznam priporočenih dodatkov](#2-seznam-priporočenih-dodatkov)
  * [Dodatki za zasebnost](#2a-dodatki-za-zasebnost)
  * [Dodatki za produktivnost](#2b-dodatki-za-produktivnost)
  * [Slovarji](#2c-slovarji)
* [Priporočeni dodatek za filtriranje vsebin: uBlock Origin](#3-priporočeni-dodatek-za-filtriranje-vsebin-ublock-origin)
  * [Priporočeni seznami filtrov](#3a-priporočeni-seznami-filtrov)
  * [Priporočeni dodatni seznami filtrov](#3b-priporočeni-dodatni-seznami-filtrov)
* [Datoteka hosts](#4-datoteka-hosts)
* [Ostali zaščitni ukrepi](#5-ostali-zaščitni-ukrepi)
  * [Za čim bolj anonimno spletno iskanje](#5a-za-čim-bolj-anonimno-spletno-iskanje)
  * [Za izogib geografskim omejitvam in digitalnim preprekam](#5b-za-izogib-geografskim-omejitvam-in-digitalnim-preprekam)
  * [Čiščenje zgodovine in sledi brskanja](#5c-čiščenje-zgodovine-in-sledi-brskanja)
* [Licenca](#licenca)

<br>

<h3>1. Priporočeni brskalnik za namizni računalnik: Mozilla Firefox</h3>

[Tu je povezava za prenos brskalnika Firefox.](https://www.mozilla.org/sl/firefox/new/)

***Zakaj ta brskalnik?*** Ker ga je možno prilagoditi na način, da postane hiter, varen in uporabniku prijazen.<br>
***Kako si ga čim bolje prilagoditi?*** Beri naprej. :)

<h4>1.a) OPTIMIZACIJA NASTAVITEV BRSKALNIKA</h4>

**I. DEL: Napredne nastavitve**

V brskalniku odpri nov zavihek in v naslovno (URL) vrstico vpiši:<br><code>about:config</code>

Pritisni *enter* in izberi gumb <code>Sprejmem tveganje!</code> Nato poišči spodnje vnose: vsako posamezno ime nastavitve kopiraj in prilepi v iskalno polje znotraj okna z nastavitvami. Nastavitev se samodejno prikaže na seznamu, nato jo z miško dvoklikni. Na ta način lahko spremeniš vrednosti v takšne, kakršne so navedene v naslednjih dveh tabelah:

Za **povečanje zasebnosti** brskalnika spremeni sledeče nastavitve:<br>

|     | IME NASTAVITVE                                                 | VREDNOST |
| --- | :------------------------------------------------------------- | :------: |
| 1.  | beacon.enabled                                                 | false    |
| 2.  | browser.safebrowsing.downloads.enabled                         | false    |
| 3.  | browser.safebrowsing.malware.enabled                           | false    |
| 4.  | browser.safebrowsing.phishing.enabled                          | false    |
| 5.  | browser.urlbar.groupLabels.enabled                             | false    |
| 6.  | extensions.experiments.enabled                                 | false    |
| 7.  | extensions.pocket.enabled                                      | false    |
| 8.  | network.trr.mode                                               | 5        |
| 9.  | privacy.resistFingerprinting                                   | true     |
| 10. | services.sync.prefs.sync.browser.safebrowsing.malware.enabled  | false    |
| 11. | services.sync.prefs.sync.browser.safebrowsing.phishing.enabled | false    |

<br>Za **izboljšanje odzivnosti in uporabnosti** brskalnika spremeni sledeče nastavitve:<br>

|     | IME NASTAVITVE                                     | VREDNOST | OPOMBE |
| --- | :------------------------------------------------- | :------: | :----- |
| 12. | browser.compactmode.show                           | true     |        |
| 13. | browser.download.animateNotifications              | false    |        |
| 14. | browser.uidensity                                  | 1        |        |
| 15.\* | dom.ipc.processCount                             | 4        | **Pogojno:** glej dodatna pojasnila spodaj. |
| 16. | extensions.htmlaboutaddons.recommendations.enabled | false    |        |
| 17.\* | full-screen-api.transition-duration.enter        | 0 0      | Glej dodatna pojasnila spodaj. |
| 18.\* | full-screen-api.transition-duration.leave        | 0 0      | Glej dodatna pojasnila spodaj. |
| 19. | full-screen-api.warning.timeout                    | 0        |        |
| 20. | security.dialog_enable_delay                       | 0        |        |

***\* Dodatna pojasnila:***
- Nastavitev št. **15** je namenjena intenzivnejšemu varčevanju brskalnika z delovnim pomnilnikom (RAM). Vendar pa bo brskalnik v primeru spremembe privzete vrednosti (iz 8 na 4) morda postal nekoliko manj odziven v scenariju z večjim številom odprtih zavihkov. Spreminjanje te vrednosti je zato koristno predvsem pri tistih računalnikih, ki uporabljajo manj kot 3 GB RAM-a.
- Nastavitvi št. **17** in **18**: pri obeh naj ima pripadajoča vrednost dve številki (dve ničli, ločeni s presledkom).

**Narejene spremembe v brskalniku Firefox je možno kadarkoli ponastaviti** (vrniti v prvotno stanje): v naprednih nastavitvah *about:config* posamezen vnos ponovno poiščemo, nanj kliknemo z desnim miškinim gumbom in v priročnem meniju izberemo "*Ponastavi*". Vrednost vnosa se bo nato povrnila v prvotno (privzeto) stanje. Kljub temu naj velja opozorilo, da se vse spremembe nastavitev, opisane na tej strani, uveljavljajo na lastno odgovornost.

<br>

**II. DEL: Dovoljenja in zbiranje podatkov Firefoxa**

Za izklop pošiljanja podatkov o uporabi Firefoxa v URL-vrstico brskalnika vpišemo sledeči vnos in ga odpremo:<br>
<code>about:preferences#privacy</code>

Premaknemo se v razdelek "***Dovoljenja***". V razdelku vklopimo (obkljukamo) naslednji dve možnosti, kot kaže sledeča slika:

<kbd><img src="https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/img/firefox-permissions-slo.png" width ="700" /></kbd><br><br>

Nato se na strani pomaknemo še v razdelek "***Zbiranje in uporaba podatkov Firefoxa***". V tem razdelku izklopimo naslednje možnosti, kot kaže ta slika:

<kbd><img src="https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/img/firefox-data-collection-slo.png" width ="700" /></kbd><br><br>

<h4>1.b) IZBOLJŠANA ZAŠČITA PRED SLEDENJEM</h4>

V URL vrstico brskalnika Firefox vpišemo sledeči vnos in ga odpremo:<br>
<code>about:preferences#privacy</code>

V razdelku "***Izboljšana zaščita pred sledenjem***" izberemo polje <code>Običajno</code> (kar je priporočeno) ali <code>Strogo</code>, kot kaže sledeča slika:

<kbd><img src="https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/img/firefox-enhanced-tracking-protection-slo.png" width ="700" /></kbd><br><br>

Ko je v Firefoxu vključena "Izboljšana zaščita pred sledenjem", nekateri videi / slike / gradniki (widgets) / polja s komentarji, ki izvirajo neposredno iz socialnih omrežij (npr. s Facebooka ali Twitterja), **ne bodo delovali**. Neposredno na samih portalih (npr. facebook.com, twitter.com) bodo sicer delovali, povezave nanje na drugih spletnih straneh pa ne. **Če jih želimo vseeno videti, na izbranih spletnih mestih preprosto izklopimo izboljšano zaščito pred sledenjem.** To naredimo tako, da levo zgoraj v naslovni (URL) vrstici brskalnika kliknemo na ikono ščita takrat, ko bomo na tistem spletnem mestu, na katerem želimo videti blokirane videe / slike / komentarje / gradnike. Ob kliku na omenjeno ikono se prikaže pojavni oblaček, v katerem kliknemo na vklopljeno stikalo. Stran se bo samodejno osvežila, ikona ščita pa bo odslej prečrtana. Brskalnik bo za to domensko ime izbiro shranil med izjeme v nastavitvah, da teh omejitev na vseh straneh v okviru izbrane spletne domene v prihodnje ne bo več. Če želimo kljub temu to nastavitev spet ponastaviti (torej ponovno vklopiti zaščito na izbrani domeni), samo ponovimo postopek: odpremo spletno stran želene domene, kliknemo na ikono prekrižanega ščita in nato v oblačku kliknemo izklopljeno stikalo.

Primeri spletnih portalov, na katerih je priporočljivo izklopiti Izboljšano zaščito pred sledenjem (na zgoraj opisani način), so:
- 24ur.com
- avtomanija.com
- avto.finance.si
- avto.info
- bibaleze.si
- ceneje.si
- dominvrt.si
- finance.si
- lisa.si
- live.finance.si
- lokalno.si
- meteo.arso.gov.si
- moskisvet.com
- moski.hudo.com
- rtvslo.si
- siol.net
- zadovoljna.si
- zenska.hudo.com

To je le nekaj slovenskih spletišč, na katerih lahko v okviru nekaterih člankov naletimo na nepopoln prikaz spletnih vsebin. Izboljšano zaščito pred sledenjem lahko po potrebi izklopimo na katerikoli spletni strani, kjer omenjen zaščitni mehanizem blokira elemente, ki so del (koristne oz. zaželene) vsebine.

Mimogrede: *Izboljšana zaščita pred sledenjem* (angl. Enhanced Tracking Protection) je zaščitni mehanizem, ki uporabnika delno varuje pred sledenjem in nekaterimi vsiljivimi oglasi. Vgrajen je v brskalnik Firefox. Prednost takšnega mehanizma, ki je vgrajen v brskalnik, je v tem, da deluje zelo hitro (tj. hitreje od naknadno nameščenih dodatkov). Vseeno pa za najboljši učinek velja v brskalnik namestiti še druge dodatke (naštete v [2. poglavju](#2-seznam-priporočenih-dodatkov)) in v sistem dodati datoteko hosts (več o njej v [4. poglavju](#4-datoteka-hosts)). Vgrajena zaščita v brskalniku namreč ne blokira vseh neželenih vsebin (npr. številnih oglasov in drugih motečih elementov na spletnih straneh).

<h3>2. Seznam priporočenih dodatkov</h3>

V nadaljevanju so našteti in opisani priporočeni dodatki, ki jih namestimo po potrebi. Vsebinsko so razdeljeni na dve podpoglavji:
- za povečanje zasebnosti brskanja
- za povečanje uporabnosti brskalnika

<h4>2.a) DODATKI ZA ZASEBNOST</h4>

|     | IME DODATKA | OPIS |
| :-- | :---------: | ---- |
| 1.  | [<img src="https://addons.mozilla.org/user-media/addon_icons/839/839767-64.png" width="45" />](https://addons.mozilla.org/firefox/addon/clearurls/)<br><b>[ClearURLs](https://addons.mozilla.org/firefox/addon/clearurls/)</b> | Dodatek ima dve funkciji. 1.) Iz URL naslovov odstranjuje parametre (npr. UTM parametre od Google Analytics). Različna analitična orodja uporabljajo URL parametre za namene spletne analitike, s čimer sledijo obiskovalcem spletnih strani (npr. za analize časa zadrževanja na posamezni strani, načine navigiranja po straneh ...). 2.) Dodatek preprečuje tudi spreminjanje povezav z rezultati iskanja na spletnih mestih (npr. Google in Yandex, lahko tudi na straneh za napotitveno trženje). Spletnemu iskalniku preprečuje, da bi se pri uporabnikovem kliku na rezultat iskanja spremenila originalna povezava na rezultat. Na ta način se lahko povezava brez težav kopira kar na strani spletnega iskalnika. Poleg tega pa spletni iskalnik ne more več učinkovito slediti nadaljnje klike uporabnika. |
| 2.  | [<img src="https://addons.mozilla.org/user-media/addon_icons/784/784287-64.png" width="45" />](https://addons.mozilla.org/firefox/addon/cookie-autodelete/)<br><b>[Cookie AutoDelete](https://addons.mozilla.org/firefox/addon/cookie-autodelete/)</b> | Omogoča samodejno brisanje vseh neuporabljenih piškotkov za tem, ko se zavihek brskalnika zapre oziroma zavrže. Obenem je možno dodajati izjeme (domene), za katere ta dodatek ne briše piškotkov. Omogočeno je tudi ročno brisanje piškotkov. |
| 3.  | [<img src="https://addons.mozilla.org/user-media/addon_icons/521/521554-64.png" width="50" />](https://addons.mozilla.org/firefox/addon/decentraleyes/)<br><b>[Decentraleyes](https://addons.mozilla.org/firefox/addon/decentraleyes/)</b> | Posnema omrežja za dostavo vsebin (angl. content delivery networks – CDN) z namenom, da prepreči čim več zahtev s strani teh omrežij. Decentraleyes se skuša izogniti sledenju različnih uveljavljenih CDN-jev (npr. Google Hosted Libraries, CDNJS, jQuery CDN, Microsoft Ajax CDN), ki kot nekakšni posredniki ponujajo "brezplačne" storitve za pohitritev nalaganja spletnih strani. Namesto, da bi se datoteke, ki so potrebne za delovanje neke spletne strani, vsakič znova prenesle neposredno iz CDN-jev (s spleta), Decentraleyes enake datoteke nadomesti iz lastnega predpomnilnika (torej iz lokalne zbirke, ki vsebuje številne pogosto zahtevane knjižnice) in jih vrine v okolje. Na ta način se je možno elegantno izogniti številnim zahtevam CDN-jev, kar prinaša različne koristi: pomaga ščititi zasebnost, poveča prihranke pri prenosu podatkov in pripomore k hitrejšem nalaganju spletnih strani. Decentraleyes naj se uporablja hkrati z drugimi dodatki, ki so opisani v nadaljevanju te tabele. V kolikor nek zahtevan vir ni na voljo na lokalni ravni, pa Decentraleyes pomaga odstraniti občutljive podatke iz odhodne spletne zahteve. |
| 4.  | [<img src="https://addons.mozilla.org/user-media/addon_icons/327/327417-64.png" width="45" />](https://addons.mozilla.org/firefox/addon/smart-referer/)<br><b>[Smart Referer](https://addons.mozilla.org/firefox/addon/smart-referer/)</b> | Vključi t. i. pametne napotitelje. Dodatek samodejno spremeni informacijo o napotitelju (angl. HTTP referer) vsakič, ko uporabnik obišče spletno mesto z drugo domeno. Pri tem je napotitelj spletni naslov, ki ga je uporabnik predhodno obiskal in iz katerega je prišel na trenutno spletno mesto. Smart referer pa informacijo o dejanskem (predhodnem) spletnem naslovu zamenja kar s ciljnim (aktualnim) spletnim naslovom. Na ta način se ustvarja vtis, da je uporabnik na trenutno spletno mesto prišel direktno (recimo z neposrednim vnosom spletnega naslova v brskalnik ali z odprtjem zaznamka) – ne pa iz nekega predhodnega spletnega mesta. S takšnim spreminjanjem informacije o napotitelju uporabnik pridobi malenkost več zasebnosti, saj denimo ni mogoče razpoznati, na podlagi katerega iskalnega niza v spletnem iskalniku (oz. iz katerega predhodnega spletnega naslova) je uporabnik v resnici prišel na trenutno spletno mesto. |
| 5.  | [<img src="https://addons.mozilla.org/user-media/addon_icons/607/607454-64.png" width="43" />](https://addons.mozilla.org/firefox/addon/ublock-origin/)<br><b>[uBlock Origin](https://addons.mozilla.org/firefox/addon/ublock-origin/)</b> | **Več o tem dodatku v [3. poglavju](#3-priporočeni-dodatek-za-filtriranje-neželenih-vsebin-na-spletu).** Dodatek blokira poljubne vsebine pri spletnem brskanju. Večinoma se uporablja za zavračanje neželenih vsebin, kot so spletni oglasi, sledilci za sledenje uporabnikov in povezav na (potencialno) nevarna spletna mesta. uBlock Origin se zato mnogokrat označuje kot zaviralec oglasov (angl. ad blocker). uBlock Origin je eno najbolj učinkovitih tovrstnih orodij z vidika hitrosti delovanja in porabe sistemskih sredstev. Z uporabo tega dodatka se občutno zviša hitrost nalaganja spletnih strani, poveča se njihova preglednost in varnost, hkrati pa se lahko (z nekaj dodatnimi nastavitvami) precej omeji tudi sledenje, ki se ga poslužujejo številna spletna mesta. |

<h4>2.b) DODATKI ZA PRODUKTIVNOST</h4>

|     | IME DODATKA | OPIS |
| :-- | :---------: | ---- |
| 6.  | [<img src="https://addons.mozilla.org/user-media/addon_icons/660/660064-64.png" width ="45" />](https://addons.mozilla.org/firefox/addon/autoplay-no-more/)<br><b>[Autoplay No More](https://addons.mozilla.org/firefox/addon/autoplay-no-more/)</b> | Izklopi funkcijo samodejnega predvajanja (tj. samodejnega skoka na naslednji videoposnetek) na spletnih mestih *[YouTube](https://www.youtube.com/)*, *[Vimeo](https://vimeo.com/)* in *[TED](https://www.ted.com/)*. |
| 7.  | [<img src="https://addons.mozilla.org/user-media/addon_icons/743/743689-64.png" width ="43" />](https://addons.mozilla.org/firefox/addon/bookmarks-manager-and-viewer/)<br><b>[Bookmarks Manager and Viewer](https://addons.mozilla.org/firefox/addon/bookmarks-manager-and-viewer/)</b> | Upravitelj in pregledovalnik zaznamkov. Izbor pripadajočega gumba prikaže ploščo, v kateri je možno iskanje med vsemi shranjenimi zaznamki. Dodatek omogoča urejanje in premikanje zaznamkov, ustvarjanje novih zaznamkov in map ipd. |
| 8.  | [<img src="https://addons.mozilla.org/user-media/addon_icons/807/807213-64.png" width ="43" />](https://addons.mozilla.org/firefox/addon/bookmarks-organizer/)<br><b>[Bookmarks Organizer](https://addons.mozilla.org/firefox/addon/bookmarks-organizer/)</b> | Upravitelj zaznamkov, ki omogoča iskanje in urejanje duplikatov med zaznamki, zaznamkov brez imen in takšnih z neveljavnimi ali preusmerjenimi povezavami ipd. |
| 9. | [<img src="https://addons.mozilla.org/user-media/addon_icons/481/481438-64.png" width ="45" />](https://addons.mozilla.org/firefox/addon/i-dont-care-about-cookies/)<br><b>[I don't care about cookies](https://addons.mozilla.org/firefox/addon/i-dont-care-about-cookies/)</b> | Samodejno odpravi obvestila o piškotkih na način, da jih potrdi (tj. se strinja z uporabo piškotkov) na posamezni strani. S tem se poveča preglednost in nekoliko skrajša čas nalaganja strani. Zakonodaja EU za spletna mesta, ki so v lasti družb s sedežem v EU, med drugim zahteva, da obiskovalcem ponudijo možnost sprejetja ali zavrnitve oz. preklica soglasja za uporabo piškotkov v obliki vidnega obvestila. Samodejno strinjanje z uporabo piškotkov (ki je sicer včasih pogoj za popolno delovanje pripadajočega spletnega mesta) krni zasebnost, vendar pa se to lahko vseeno kompenzira s hkratno uporabo drugih dodatkov (npr. uBlock Origin) in zaščitnih mehanizmov (npr. Izboljšana zaščita pred sledenjem v brskalniku Firefox). |
| 10. | [<img src="https://addons.mozilla.org/user-media/addon_icons/739/739386-64.png" width ="42" />](https://addons.mozilla.org/firefox/addon/in-my-pocket/)<br><b>[In My Pocket](https://addons.mozilla.org/firefox/addon/in-my-pocket/)</b> | In My Pocket je odličen za uporabnike storitve *[Pocket](https://getpocket.com/)*. Dodatek v naslovno (URL) vrstico brskalnika doda ikono, ki omogoča shranjevanje ali odstranjevanje spletnih mest s storitve *Pocket*. Poleg tega dodatek omogoča uporabo priročnega seznama z vsemi shranjenimi povezavami do spletnih mest v okviru storitve Pocket. Povezave s seznama je možno odpreti ali odstraniti (sinhronizirano s storitvijo Pocket). Omenjen seznam prikličemo z izborom pripadajočega gumba. Dodatek torej deluje po vzoru prvotnega uradnega (a ukinjenega) dodatka Pocket, na podlagi katerega za uporabo storitve Pocket ni potrebe po neposrednem obiskovanju spletnega mesta getpocket.com. |
| 11. | [<img src="https://addons.mozilla.org/user-media/addon_icons/718/718289-64.png" width ="45" />](https://addons.mozilla.org/firefox/addon/mouse-gestures/)<br><b>[Mouse Gesture Events](https://addons.mozilla.org/firefox/addon/mouse-gestures/)</b> | Omogoča brskanje z uporabo priročnih miškinih potez. V nastavitvah dodatka se lahko prilagodijo različne možnosti za navigiranje po spletu z uporabo desnega miškinega gumba v povezavi z gibanjem miške in/ali z uporabo desnega miškinega gumba v povezavi z vrtenjem miškinega koleščka. |
| 12. | [<img src="https://addons.mozilla.org/user-media/addon_icons/937/937151-64.png" width ="45" />](https://addons.mozilla.org/firefox/addon/view-image/)<br><b>[Ogled slike](https://addons.mozilla.org/firefox/addon/view-image/)</b> | Ponovno prikaže gumba <code>Ogled slike</code> in <code>Iskanje s sliko</code> v spletnem iskalniku slik *[Google Slike](https://www.google.si/imghp?hl=sl)*. Google je namreč leta 2018 ta dva gumba umaknil s svoje storitve zaradi obtožb, da z "bližnjičnimi" gumbi ponuja neposreden dostop do vsebin, ki so avtorsko zaščitene, s tem pa olajšuje tudi možnost njihove kraje. |
| 13. | [<img src="https://addons.mozilla.org/user-media/addon_icons/2729/2729178-64.png" width ="45" />](https://addons.mozilla.org/firefox/addon/return-youtube-dislikes/)<br><b>[Return Youtube Dislike](https://addons.mozilla.org/firefox/addon/return-youtube-dislikes/)</b> | Ponovno prikaže število nevšečkov ("Ni mi všeč") pri videih na spletnem mestu *[YouTube](https://www.youtube.com/)*. Ta platforma je namreč leta 2021 ukinila javno prikazovanje števila neveščkov z izgovorom, da naj bi prikazovanje nevščkov škodovalo nekaterim ustvarjalcem vsebin. |
| 14. | [<img src="https://addons.mozilla.org/user-media/addon_icons/724/724283-64.png" width ="40" />](https://addons.mozilla.org/firefox/addon/save-page-we/)<br><b>[Save Page WE](https://addons.mozilla.org/firefox/addon/save-page-we/)</b> | Omogoča (lokalno) shranjevanje spletnih strani v eni sami datoteki HTML. Shraniti (arhivirati) je možno celotno spletno stran ali pa samo njene izbrane elemente. Shranjevanje strani s pomočjo Save Page WE je precej bolj praktično od "običajnega" shranjevanja, saj Save page WE celotno razpoložljivo vsebino spletne strani združi v le eno datoteko HTML. Nadalje je uporaba Save Page WE primernejša od shranjevanja spletnih strani v drugih oblikah (npr. v obliki MHT). Shranjevanje spletnih strani v obliki HTML je primernejše od MHT, ker podporo za datoteke HTML brez težav nudijo vsi brskalniki (v nasprotju z datotekami MHT, za katere v splošnem obstaja precej slabša podpora). |
| 15. | [<img src="https://addons.mozilla.org/user-media/addon_icons/2590/2590937-64.png" width ="40" />](https://addons.mozilla.org/firefox/addon/sponsorblock/)<br><b>[SponsorBlock for YouTube - Skip Sponsorships](https://addons.mozilla.org/firefox/addon/sponsorblock/)</b> | Samodejno preskoči izseke v *[YouTube](https://www.youtube.com/)* videih, ki so bili zaznani kot (irelevantna) sponzorirana vsebina. Dodatek omogoča tudi, da sami označimo in sporočimo zaznane odseke s sponzorirano vsebino, ki še v nekem YouTube videu niso bili preskočeni. Na ta način se hkrati dopolnjuje spletna baza podatkov, na osnovi katere lahko vsi uporabniki dodatka SponsorBlock spremljajo videe s čim manj sponzoriranimi/oglasnimi izseki. |
| 16. | [<img src="https://addons.mozilla.org/user-media/addon_icons/1002/1002139-64.png" width ="45" />](https://addons.mozilla.org/sl/firefox/addon/youtube-nonstop/)<br><b>[YouTube NonStop](https://addons.mozilla.org/sl/firefox/addon/youtube-nonstop/)</b> | Samodejno potrdi obvestila, ki se med predvajanjem *[YouTube](https://www.youtube.com/)* videov včasih samodejno pojavijo ("Predvajanje videoposnetka je začasno zaustavljeno"). Z dodatkom se tako izognemo samodejnemu pavziranju videov med njihovim predvajanjem. |
| 17. | [<img src="https://addons.mozilla.org/user-media/addon_icons/673/673711-64.png" width ="40" />](https://addons.mozilla.org/firefox/addon/youtubes-annotations-no-more/)<br><b>[Youtube's Annotations No More](https://addons.mozilla.org/firefox/addon/youtubes-annotations-no-more/)</b> | Izklopi pripise (angl. annotations) na spletnem mestu *[YouTube](https://www.youtube.com/)*. S tem se poveča preglednost pri ogledovanju videoposnetkov.<br><b>OPOMBA:</b> če bi kljub temu želeli v videoposnetkih videti (oz. klikniti na) pripise, je potrebno ta dodatek v seznamu dodatkov in tem (začasno) onemogočiti ali odstraniti. |

<h4>2.c) SLOVARJI</h4>

|     | IME SLOVARJA | OPIS |
| :-- | :----------: | ---- |
| 1.  | [<img src="https://addons.mozilla.org/user-media/addon_icons/677/677644-64.png" width ="45" />](https://addons.mozilla.org/firefox/addon/us-english-dictionary/)<br><b>[English United States Dictionary](https://addons.mozilla.org/firefox/addon/us-english-dictionary/)</b> | Slovar angleškega jezika (ZDA). |
| 2.  | [<img src="https://addons.mozilla.org/static-server/img/addon-icons/default-64.d144b50f2bb8.png" width ="45" />](https://addons.mozilla.org/firefox/addon/dictionary-german/)<br><b>[German Dictionary](https://addons.mozilla.org/firefox/addon/dictionary-german/)</b> | Slovar nemškega jezika. |
| 3.  | [<img src="https://addons.mozilla.org/user-media/addon_icons/3/3046-64.png" width ="45" />](https://addons.mozilla.org/firefox/addon/slovar-za-slovenski-jezik/)<br><b>[Slovar za slovenski jezik](https://addons.mozilla.org/firefox/addon/slovar-za-slovenski-jezik/)</b> | Slovar slovenskega jezika. |

Seznam vseh razpoložljvih slovarjev in jezikovnih paketov [se nahaja tukaj](https://addons.mozilla.org/firefox/language-tools/).

<h3>3. Priporočeni dodatek za filtriranje vsebin: uBlock Origin</h3>

***Zakaj ta dodatek?*** Ker je učinkovit, nezahteven, enostaven in brezplačen. V različnih pogledih je mnogo boljši od ostalih tovrstnih alternativ, med drugim tudi od znanega in požrešnega *AdBlock Plus*, kar je razvidno npr. iz [te primerjave](https://github.com/gorhill/uBlock/wiki/uBlock-vs.-ABP:-efficiency-compared) in iz [tega testa](https://www.raymond.cc/blog/10-ad-blocking-extensions-tested-for-best-performance/view-all/).
<br><br>Povezave za namestitev dodatka uBlock Origin:

- <b>[Dodatki za Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)</b> za brskalnik Mozilla Firefox
- <b>[Spletna trgovina Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)</b> za brskalnike Google Chrome, Vivaldi in ostale, ki temeljijo na Chromiumu
- <b>[Opera add-ons](https://addons.opera.com/extensions/details/ublock/)</b> za brskalnik Opera

<h4>3.a) PRIPOROČENI SEZNAMI FILTROV</h4>

Želene naročnine na filtre vklopimo tako, da se v okviru dodatnih možnosti dodatka uBlock Origin pomaknemo na zavihek <kbd>Filtri tretjih oseb</kbd> in nato na pripadajočem seznamu posamezne naročnine označimo s kljukico. Priporočene naročnine so vklopljene na sledečih slikah:

<kbd><img src="https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/img/3rd-party-filters-slo-1.png" width ="600" /></kbd>

<kbd><img src="https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/img/3rd-party-filters-slo-2.png" width ="600" /></kbd>

<kbd><img src="https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/img/3rd-party-filters-slo-3.png" width ="600" /></kbd>

Velik del zgornjih naročnin je najverjetneje privzeto že vklopljen. Preostale naročnine s seznama ročno vklopi oziroma izklopi. Nato v desnem zgornjem kotu okna izberi oranžen gumb <code>Uveljavi spremembe</code>. Nato se pomakni na vrh strani in v levem zgornjem delu okna klikni še na gumb <code>Posodobi zdaj</code>. Po nekaj trenutkih se bo ta gumb obarval sivo.

<h4>3.b) PRIPOROČENI DODATNI SEZNAMI FILTROV</h4>

Nadalje se lahko v uBlock Origin ročno dodajo številne dodatne naročnine za še učinkovitejše filtriranje raznovrstne spletne nesnage in hitrejše brskanje.

Spodnje povezave najprej kopiramo. Najbolj preprosto je, če kopiramo vse spodnje povezave *naenkrat*, saj se bodo morale vse dodane povezave nahajati v svoji (posamezni) vrstici. Nato odpremo polje filtrov, ki se nahaja skrajno spodaj v okviru zavihka <kbd>Filtri tretjih oseb</kbd>. Polje filtrov za vnos kopiranih povezav odpremo tako, da v razdelku *Po meri* obkljukamo možnost "*Uvozi ...*". Ko povezave dodamo (prilepimo) v polje filtrov, v zgornjem levem delu okna kliknemo na oranžen gumb <code>Uveljavi spremembe</code>.

<code>https://<i></i>raw.githubusercontent.com/AdguardTeam/AdguardFilters/908c5ee818d05803cff6243d127b5efc89b89c67/AnnoyancesFilter/sections/popups.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener-AffiliateTagAllowlist.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt</code><br>
<code>https://<i></i>filters.adtidy.org/windows/filters/2.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/Yhonay/antipopads/master/popads.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/DandelionSprout/adfilt/master/ClearURLs%20for%20uBo/clear_urls_uboified.txt</code><br>
<code>https://<i></i>www.fanboy.co.nz/enhancedstats.txt</code><br>
<code>https://<i></i>fanboy.co.nz/fanboy-problematic-sites.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/betterwebleon/international-list/master/filters.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/hoshsadiq/adblock-nocoin-list/master/nocoin.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/metaphoricgiraffe/tracking-filters/master/trackingfilters.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/Spam404/lists/master/adblock-list.txt</code><br>
<code>https://<i></i>raw.githubusercontent.com/IDKwhattoputhere/uBlock-Filters-Plus/master/uBlock-Filters-Plus.txt</code><br>

Po nekaj trenutkih se v razdelku *Po meri* pojavi takšen seznam:

<kbd><img src="https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/img/3rd-party-filters-slo-4.png" /></kbd>

Nastavitve dodatka uBlock Origin lahko na tem mestu zapremo.

*Naročnine so seveda brezplačne, kakor tudi ostalo na tej strani.* :)

<h3>4. Datoteka hosts</h3>

Pomembna in uporabna stvar za izboljšanje varnosti in osnovno (a učinkovito) blokiranje oglasov je datoteka "***hosts***". Tudi ta datoteka (ki je brez datotečne pripone) je dopolnilo vsem ostalim prilagoditvam na tej strani. Uporablja se torej skupaj z dodatkom uBlock Origin.

Kot pojasnjuje [Steven Black](https://github.com/StevenBlack/hosts/blob/master/readme.md), gre pri *hosts* za besedilno datoteko, v katero se izbranim imenom gostiteljev (angl. hostnames) določijo pripadajoči IP naslovi, ki jih želimo prilagajati (v našem primeru blokirati) na sistemski ravni. To pomeni, da vnešena pravila za izbrane IP naslove učinkujejo na ravni celotnega operacijskega sistema, ne le na ravni posameznega brskalnika.

Zaradi tovrstnega rigoroznega blokiranja se torej v datoteko *hosts* dodajo le povezave na tiste gostitelje, za katere je potrjeno, da so neželeni (npr. oglasni strežniki – angl. ad servers) ali nevarni (npr. strežniki z zlonamerno programsko opremo – angl. malware servers). Datoteko *hosts* z najbolj neželenimi gostitelji je že pripravil Steven Black. Omenjeno datoteko s približno 200.000 blokiranimi neželenimi gostitelji je možno **[prenesti tukaj](https://github.com/StevenBlack/hosts/archive/master.zip)** (datoteka *hosts* se nahaja v preneseni mapi "*hosts-master*").

Datoteko *hosts* odpakiramo. Nato jo lahko kar zamenjamo z obstoječo verzijo (v kolikor vanjo nismo predhodno že vnašali svoja pravila). To storimo na posebnem mestu v raziskovalcu datotek:

- v sistemih **Windows** jo kopiramo v:<br><code>C:\Windows\System32\Drivers\etc</code>
- v sistemih **Mac OS X**, **iOS**, **Linux** ali **Android** jo kopiramo v:<br><code>/etc/hosts</code>

Za tem lahko ponovno zaženemo računalnik in datoteka *hosts* bo samodejno osvežena. Lahko pa namesto ponovnega zagona vse skupaj usposobimo na hitrejši način:
- v sistemih **Windows** odpri Ukazni poziv (cmd.exe) kot administrator. Nato zaženi sledeči ukaz:<br><code>ipconfig /flushdns</code>
- v sistemih **Mac OS X** odpri Terminal in zaženi:<br><code>sudo dscacheutil -flushcache;sudo killall -HUP mDNSResponder</code>
- v sistemih **Linux Debian / Ubuntu** odpri Terminal in z administratorskimi pravicami zaženi:<br><code>sudo /etc/rc.d/init.d/nscd restart</code>
- v sistemih **Linux with systemd** odpri Terminal in z administratorskimi pravicami zaženi:<br><code>sudo systemctl restart network.service</code>
- v sistemih **Fedora Linux** ali **Arch Linux / Manjaro** odpri Terminal in z administratorskimi pravicami zaženi:<br><code>sudo systemctl restart NetworkManager.service</code>

Zapremo okno. V kolikor imamo odprt brskalnik, ga nato zapremo in ponovno zaženemo.

<h3>5. Ostali zaščitni ukrepi</h3>

<h4>5.a) ZA ČIM BOLJ ANONIMNO SPLETNO ISKANJE</h4>

Uporabimo lahko spletne iskalnike, ki naše iskanje anonimizirajo. Od takšnih so najbolj znani:

- [Brave Search](https://search.brave.com/): omogočal naj bi anonimno iskanje
- [DuckDuckGo](https://duckduckgo.com/): omogočal naj bi anonimno iskanje
- [StartPage](https://www.startpage.com/): bazira na iskalniku Google, pri čemer naj bi se iskalni zadetki anonimizirali

<h4>5.b) ZA IZOGIB GEOGRAFSKIM OMEJITVAM IN DIGITALNIM PREPREKAM</h4>

Za bolj intenzivno prikrivanje svoje lokacije in (pogojno) identitete se lahko precej učinkovito uporabi kakovostno VPN omrežje. VPN lahko usposobimo z namestitvijo programa (deluje na ravni celotnega sistema) ali z namestitvijo dodatka v brskalnik (deluje samo znotraj brskalnika z vklopljenim VPN dodatkom). Eden od seznamov z uveljavljenimi VPN ponudniki se nahaja recimo [na tej strani](https://www.techradar.com/vpn/best-vpn).

<h4>5.c) ČIŠČENJE ZGODOVINE IN SLEDI BRSKANJA</h4>

Vsaj občasno je priporočljivo odstraniti zgodovino in sledi brskanja iz naprav, na katerih dostopamo do spleta. S tem optimiramo delovanje spletnega brskalnika in mnogokrat izboljšamo odzivnost sistema. Zgodovina brskanja se odstrani neposredno iz brskalnika. Primer: na namizni različici brskalnika Mozille Firefox do te funkcije dostopamo s kombinacijo tipk: <code>Ctrl</code>, <code>Shift</code> in <code>Delete</code>. Nato pri možnosti "*Časovni obseg brisanja*" izberemo "***Vse***". V razdelku "*Zgodovina*" obkljukamo vse opcije. Na koncu z izborom gumba <code>V redu</code> potrdimo izbris izbranih podatkov iz brskalnika. Pripadajoče okno je razvidno s spodnje slike:

<kbd><img src="https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/img/firefox-clean-history-slo.png" width ="400" /></kbd>

Če želimo, da brskalnik sploh shranjuje zgodovine brskanja, prijav in izpolnjenih obrazcev, pa lahko vklopimo anonimni način brskanja. Primer: na namizni različici brskalnika Mozille Firefox do te funkcionalnosti dostopamo s kombinacijo tipk: <code>Ctrl</code>, <code>Shift</code> in <code>P</code>.

**OPOMBA:** kljub uporabi vseh dodatkov, datoteke hosts, anonimnih spletnih iskalnikov, VPN omrežij in ostalih zaščitnih mehanizmov je potrebno poudariti, da **popolne anonimnosti na spletu žal ni**. Še vedno namreč komunikacija neizogibno poteka preko telekomunikacijskih ponudnikov, različnih posredniških strežnikov in naprav. Poleg tega uporabniki navadno uporabljamo različne spletne storitve: e-pošta (v obliki klienta ali spletne storitve), socialna omrežja, forumi in drugi portali... V primeru uporabe teh storitev nas vsi omenjeni ukrepi ščitijo v zelo omejenem obsegu. Vsekakor nam sicer občutno olajšajo hitrost, preglednost in varnost spletnega brskanja, ne zagotavljajo pa popolne anonimnosti – vsaj ne vedno in v vsakem scenariju.

Prijetno in varno brskanje!
***
<h3>Licenca</h3>

[Unlicense](https://github.com/betterwebleon/slovenian-list/blob/master/LICENSE.txt).

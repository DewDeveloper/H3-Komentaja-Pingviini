<h1>H3 Komentaja Pingviini</h1>

<h3>Command Line Basic Revisited -sivua koskevat muistiinpanot</h3>

<h5>Komennoista</h5>

<p>-"pwd" tulostaa nykyisen kansion polun<br>
-"ls" tulostaa kansion sisällön<br>
-"cd kohdekansio" siirtää hakemistorakenteessa yhden pykälän alaspäin<br>
-"cd .." siirtää hakemistorakenteessa yhden pykälän ylöspäin<br>
-"less tekstitiedosto.txt" avaa tekstitiedoston katseltavaksi<br>
-"mkdir kansionnimi" luo halutunnimisen uuden kansion<br>
-"mv nykyinennimi uusinimi" uudelleennimeää kohdetiedoston tai -kansion<br>
-"rm nimi" poistaa tiedoston<br>
-"rmdir nimi" poistaa tyhjän kansion<br>
-"rm -r nimi" poistaa kansion sisältöineen<br>
-"history" listaa komennot, joita on annettu<br>
-"sudo apt-get update" listaa saatavilla olevat paketit (käytettävä ennen muita apt-komentoja)<br>
-"apt-cache search hakusana" etsii hakumääreen mukaisia ohjelmistoja<br>
-"sudo apt-get -y install asennettava" asentaa ohjelmiston<br>
-"dpkg --listfiles kohdeohjelmisto" listaa ohjelman tiedostot<br>
-Tabulaattori täydentää komennon, jos ei ole erehtymisen mahdollisuutta (ts. vain yksi vaihtoehto)<br>
-Tabulaattori kahdesti painettuna listaa vaihtoehdot</p>

<h5>Kansioista</h5>

-"/"-kansio eli Root, tiedostojärjestelmän juuri<br>
-"/home/"-kansio, sisältää käyttäjien kotihakemistot<br>
-"/home/username"-kansio, käyttäjä voi varastoida tietojaan pysyvästi vain sinne<br>
-"/etc/"-kansio, sisältää järjestelmänlaajuiset asetukset<br>
-"/media/"-kansio, sisältää irroitettavat tallennusmediat<br>
-"/var/log/"-kansio, sisältää lokitiedostot

<h5>Muuta</h5>


-SSH mahdollistaa toisen tietokoneen etäkäytön<br>
-Pico ja Nano ovat tekstieditoreja<br>
-"Minimum privilege"-periaate eli Linuxia tulisi käyttää heikoimmalla riittävän voimakkaalla käyttöoikeudella (järjestelmää vahingoittavien erehdyksessä annettujen komentojen välttämiseksi?)<br>
-"sudo" antaa pääkäyttäjäoikeudet

Viimeisenä, muttei vähäisimpänä, älä pelaa Nethackia (minua on varoitettu)

<h3>Micro-editorin asentaminen</h3>

[08:04] Käynnistettyäni Debianin ja kirjauduttuani sisään avasin terminaalin.<br>
[08:05] Hain saatavilla olevat paketit komennolla<br>
      <code> sudo apt-get update </code><br>
Hain "Micro"-tekstieditoria komennolla <br>
<code>apt-cache search micro</code><br>
Löysin listalta selaamisen jälkeen micro-nimisen ohjelman, joka on kuvauksen mukaan moderni tekstieditori.<br>
Asensin micron komennolla <br>
<code>sudo apt-get -y install micro</code><br>

![1](https://user-images.githubusercontent.com/105177604/213964208-8785ee43-0b0d-4c5d-b3c7-7f2f11765a43.JPG)

[08:17] Avasin Micro-sovelluksen kirjoittamalla terminaaliin <br>
<code>micro</code><br>
Kirjoitin tiedostoon ja tallensin sen.<br>

![2](https://user-images.githubusercontent.com/105177604/213964533-60ca6154-1e2f-44d9-bf31-3db0a0a93253.JPG)

Tämän jälkeen suljin Micro-sovelluksen näppäinyhdistelmällä <br>
<code>Ctrl-q</code><br>
[08:24] En tiennyt, mihin tiedosto tallentui. Listasin nykyisen kansion sisällön ja tiedosto näkyi polussa <br>
<code>/home/matiask</code><br>

![3](https://user-images.githubusercontent.com/105177604/213964626-afa60a53-7d37-4026-b2db-0ea65b9349d1.JPG)

[08:25] Tarkistin tiedoston sisältävän mitä pitikin avaamalla sen Micro-ohjelmassa terminaalissa antamallani komennolla <br>
<code>micro testi</code><br>

![4](https://user-images.githubusercontent.com/105177604/213964724-b3e30fe8-5b1d-445a-802d-a4ac5c85b26e.JPG)

[08:26] Suljin Micro-ohjelman näppäinyhdistelmällä<br> 
<code>Ctrl-q</code>

<h3>Raudan listaaminen</h3>

[09:00] Avasin terminaalin ja annoin komennon <br>
<code>sudo lshw -short -sanitize</code><br>
[09:00] Sain ilmoituksen <br>
<code>sudo: lshw: command not found</code> <br>
[09:01] Annoin komennon <br>
<code>sudo apt-get update</code> <br>
[09:02] Annoin komennon <br>
<code>sudo apt-get -y install lshw</code> <br>
[09:03] Lshw-ohjelman asennus valmistui.<br>

![5](https://user-images.githubusercontent.com/105177604/213964836-78623417-788a-4928-b2ee-f9678a7cd20e.JPG)

[09:11] Annoin uudelleen komennon<br> 
<code>sudo lshw -short -sanitize</code> <br>
[09:11] Sain alapuolisen raportin.<br>

![6](https://user-images.githubusercontent.com/105177604/213963807-f32386f2-0b15-435e-91e4-97fb4c67b182.JPG)

Apuna raportin tulkinnassa käytin internetistä löytämääni sivustoa[3].
Lisäksi luin hitusen eteläsillasta[4] ja pohjoissillasta[5] Wikipediasta.

"H/W Path" -sarakkeessa näkyy komponenttien liittyminen toisiinsa ylhäältä alaspäin.<br>
"/0" kuvaa emolevyä, jona tämän virtuaalikoneen tapauksessa näkyy VirtualBox.<br>
Emolevylle taas liittyy muita komponentteja, kuten välimuisti ("/0/1").
"/0/100" puolestaan kuvaa pohjoissiltaa, yhtä emolevyn piirisarjan kahdesta päämikropiiristä, jonka kautta suurta
tiedonsiirtonopeutta vaativat komponentit keskustelevat keskenään. <br>
"/0/100/1" kuvaa toista piirisarjan kahdesta päämikropiiristä, pohjoissiltaan yhteydessä olevaa eteläsiltaa, johon liittyy vähäisemmällä tiedonsiirtonopeudella toimivat komponentit.<br>
"/0/100/d" kuvaa tallennusjärjestelmiä.

<h3>Kolmen komentoriviohjelman asentaminen</h3>

Pikaisen googlaamisen jälkeen päädyin sivulle[6], joka listasi parhaita komentorivityökaluja ohjelmistokehittäjille. Koska suuntaan opintojani siihen suuntaan, valitsin ohjelmat tältä listalta. Valitsemani ohjelmat olivat tldr, howdoi ja rebound.

Karvisen tehtävänannossa[2] haastettiin asentamaan kaikki kolme ohjelmaa yhdellä komennolla. Kurssilla aiemmin opetetun perusteella muistelin, että useita tiedostoja voi luoda yksinkertaisesti listaamalla tiedostonimet perätysten välilyönnein erotettuna. Päädyin kokeilemaan jo opitun soveltamista.

[14:36] Avasin terminaalin ja latasin tiedot paketeista komennolla <br>
<code>sudo apt-get update</code><br>
[14:37] Annoin komennon <br>
<code>sudo apt-get -y install tldr howdoi rebound</code><br>
[14:40] Komento näytti toimivan, asentaminen alkoi.<br>

![8](https://user-images.githubusercontent.com/105177604/213965193-14a32780-7fb0-42e7-8249-b93366ff14d5.JPG)

[14:42] Asennus oli yhä kesken.<br>
[14:47] Asennus oli valmis.<br>

Ohjelmien kokeilu ei sen sijaan sujunut mutkattomasti. Howdoi, jolta siis voi kysyä ohjelmointiin liittyvistä asioista ja se etsii vastauksia Stackexchange-sivustolta, ei löytänyt mitään vastauksia mihinkään.
Reddit[7] osasi kertoa, ettei ohjelma pidä apt-asennuksesta, vaan pitäisi käyttää pip-asennusta.

![9 howdoi](https://user-images.githubusercontent.com/105177604/213965325-79f94c79-3b8e-4fc8-b399-a5ba65c3f32d.JPG)

TLDR:n käyttö sujui hieman paremmin, tosin se ei ymmärtänyt esimerkiksi komentoa <br>
<code>tldr history</code><br>
Sen sijaan se osasi kertoa hakemistorakenteessa liikkumisesta annettuani komennon <br> 
<code>tldr cd</code>

![10 tldr](https://user-images.githubusercontent.com/105177604/213965344-3868b5fa-a28e-46cf-9f94-efa0e1994e04.JPG)


Rebound taas on ohjelma, joka auttaa diagnostiikassa, kun virheellisen python-ohjelman suoritus keskeytyy.
Kirjoitinkin Microlla seuraavan, virheellisen ohjelman.

![11](https://user-images.githubusercontent.com/105177604/213965418-8d31c26b-5231-4521-ad4c-4f7e10b2f500.JPG)

Sen suoritus Reboundilla näytti seuraavalta.

![12](https://user-images.githubusercontent.com/105177604/213965459-1193ddde-72fe-4892-a24d-6e059fea3079.JPG)

<h3>Command Line Basics Revisited -verkkosivulla[1] listattujen tärkeiden hakemistojen esittely</h3>

<h5>'/'</h5>
Root eli juuri. Juuressa on mm. boot-kansio, joka mitä ilmeisimmin on tärkeä järjestelmän käynnistyksen kannalta.

![14 root](https://user-images.githubusercontent.com/105177604/213965792-eca1d865-0ccc-4874-adc5-e97809066ac2.JPG)

<h5>/home/</h5>
Home eli käyttäjien tiedostot sisältävä hakemisto. Alikansiot on nimetty käyttäjänimen mukaan, tässä tapauksessa "matiask", kun se on ainoa käyttäjä.

![15  home kayttaja](https://user-images.githubusercontent.com/105177604/213965809-99b32d70-32ae-43b0-be14-03038d94ce8e.JPG)

<h5>/etc/</h5>
Etc eli järjestelmänlaajuiset asetukset, jotka ovat tekstitiedostojen muodossa.

![16 etc](https://user-images.githubusercontent.com/105177604/213965881-9b774674-7be4-4860-b9a4-eb6926d56370.JPG)

<h5>/media/</h5>
Media eli irroitettavissa olevat tallennusmediat, kuten muistitikut ja dvd-levyt.

![17 media](https://user-images.githubusercontent.com/105177604/213966011-162ded78-b224-433e-9ae6-697c3109493d.JPG)

<h5>/var/log/</h5>
Järjestelmän lokitiedostot. Voi olla hyödyllinen mm. vianselvityksessä.

![18 var log](https://user-images.githubusercontent.com/105177604/213966068-946500e9-1e63-4d04-b1f3-177cd1eb27b7.JPG)

<h3>Grep-komennon käyttö</h3>

Tutustuin aiheeseen internetissä[8] ja opin, että Grep mahdollistaa hakujen tekemisen tiedostojen ja kansioiden sisältöön.

[08:23] Latasin Wikipediasta sivun kissaroduista ja tallensin sen. <br>
[08:58] Hain termiä "American" (esim. American Bobtail, American Shorthair) kaikista kansion .html-päätteisistä tiedostoista komennolla: <br>
<code>grep "American" *.html</code> <br>
Toimin näin sen takia, että en onnistunut kohdistamaan hakua suoraan tiedostoon. Ehkä lainaushipsujen kanssa pitäisi käyttää jotakin erikoismerkkiä, en tiedä. <br>
Sain seuraavan listan.

![19 grep](https://user-images.githubusercontent.com/105177604/213982528-c2d45297-1bb7-46bf-9bc4-1ac3e3f911b9.JPG)

<h3>Kohdatut ongelmat</h3>

Jos Debian jäi liian pitkäksi aikaa epäaktiiviseksi, virtuaalikone hyytyi alapuolisen kuvan mukaisesti. Ongelman sai korjattua VirtualBoxin Machine-ylävalikon Pause-vaihtoehdosta, mutta se uusiutui taas, jos Debianin jätti epäaktiiviseksi.

![virhe](https://user-images.githubusercontent.com/105177604/213983113-14d52a29-d370-4ed3-971e-3ae8be5d204e.JPG)

Myös Debianin selain, Firefox, toimi hyvin hitaasti. Painallukset eivät aina rekisteröityneet ja esimerkiksi pelkkä scrollaaminen saattoi hyydyttää näkymän. Tätä koskien ei tullut virheilmoituksia, mutta häiritsevää se oli.


<h3>Lähdemateriaalit</h3>
 
[1] Karvinen, Tero. 2020. Command Line Basics Revisited. https://terokarvinen.com/2020/command-line-basics-revisited/. Luettu 22.1.2023. <br>
[2] Karvinen, Tero. 2023. Linux Palvelimet 2023 alkukevät. https://terokarvinen.com/2023/linux-palvelimet-2023-alkukevat/#h2-komentaja-pingviini. Luettu 22.1.2023. <br>
[3] Ezix. Hardware Lister (lshw). https://ezix.org/project/wiki/HardwareLiSter. Luettu 22.1.2023. <br>
[4] Wikipedia. 2023. Southbridge (computing). https://en.wikipedia.org/wiki/Southbridge_(computing). Luettu 22.1.2023. <br>
[5] Wikipedia. 2023. Northbridge (computing). https://en.wikipedia.org/wiki/Northbridge_(computing). Luettu 22.1.2023. <br>
[6] Steins, Bas. 2022. 14 Awesome CLI Tools for Modern Software Developers. https://bas.codes/posts/best-cli-tools-software-developer. Luettu 22.1.2023. <br>
[7] Reddit. Package 'howdoi' not working? https://www.reddit.com/r/linuxquestions/comments/lx55br/package_howdoi_not_working/. Luettu 23.1.2023. <br>
[8] Computer Hope. Linux grep command. https://www.computerhope.com/unix/ugrep.htm Luettu 23.1.2023. <br>


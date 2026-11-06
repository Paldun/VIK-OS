# ⚡ VIK-OS — BME Hallgatói Munkakörnyezet & Tanulmányi Rendszer

A **VIK-OS** egy modern, PyQt6-alapú, kifejezetten a Budapesti Műszaki és Gazdaságtudományi Egyetem Villamosmérnöki és Informatikai Karának (BME VIK) hallgatói számára tervezett asztali munkakörnyezet. Egyesíti a kari tanulmányi portálok elérését, a grafikus kari ZH-beosztás feldolgozását, a kredit- és kollégiumi pontszámítást, valamint a Google/Apple naptárszinkronizációt egyetlen testreszabható munkafelületen.

---

## 🌟 Főbb funkciók

### 🖥️ Szabadon rendezhető asztal & Mapparendszer
* **Valódi asztali élmény:** Szabadon elhelyezhető és mozgatható tantárgykártyák láthatatlan 16 px-es mágneses illesztéssel.
* **Méretezhető asztali elemek:** Minden kártya, mappa és a naptár a jobb alsó sarkában lévő fogantyúval (`◢`) tetszőleges méretűre húzható.
* **Asztali mappák (Drag & Drop):** Hozz létre színes mappákat, és húzd rájuk a tárgyakat a csoportosításhoz. A mappákra duplán kattintva külön szerkesztőablak nyílik meg.

### 📅 Intelligens ZH-Naptár & Szinkronizáció
* **Kari ZH-táblázat automatikus importálása:** A hivatalos `zh_26-27_ösz_grafikus.xlsx` fájl betöltésekor a program a beállított szakod (Mérnökinformatikus, Villamosmérnök, BProf, GaIn, MSc) és féléved alapján automatikusan kiválogatja az összes ZH, PZH és PPZH időpontot.
* **Google Naptár & Apple Naptár (`.ics`) kétirányú szinkron:**
  * **Import:** Olvasd be a telefonodon vagy Google Naptáradban lévő eseményeket.
  * **Export:** Egyetlen kattintással mentsd ki az összes számonkérést szabványos `.ics` formátumba, amely azonnal importálható mobilra.
* **Automatikus PótZH prioritás:** Ha egy tantárgy pontszáma nem éri el az aláírási minimumot, a rendszer automatikusan kiemelt, sürgős státuszba helyezi a hozzá tartozó pótZH-kat.

### 📊 BMEVIK-Calc Kredit- & Koli-pont Kalkulátor
* **Kari számolólap integráció:** A hivatalos `BMEVIK-Calc.xlsx` mintatanterveinek közvetlen beolvasása (BSc Info, BSc Villany, BProf, MSc).
* **Élő mutatók:** Súlyozott tanulmányi átlag, Ösztöndíjindex ($\frac{\sum \text{kredit} \times \text{jegy}}{30}$), gördített ösztöndíjindex és kollégiumi tanulmányi pontszám azonnali újraszámolása.

### 🌐 Beágyazott böngésző & Auto-Login
* **Integrált böngészőfülek:** Nem kell elhagyni az alkalmazást; a Neptun, Moodle, InfoC és VIK Wiki közvetlenül belső füleken nyílik meg.
* **Intelligens Auto-Login:** Automatikusan felismeri a BME EduID (Shibboleth) és Neptun bejelentkező mezőket, kitölti az azonosítót, jelszót, és igény szerint azonnal be is léptet.
* **Perzisztens munkamenet:** Megőrzi a bejelentkezési munkameneteket és sütiket egy elkülönített profilmappában.

### 🛠️ További beépített eszközök
* **🍅 Pomodoro Fókusz Időzítő:** 25 perces fókusz és 5/15 perces szünet blokkok vizsgafelkészüléshez és programozási feladatokhoz.
* **📁 Fájlkezelő & Google Drive:** Saját tantárgyi könyvtárak tallózása közvetlenül az oldalsávból, valamint gyorselérés a Google Drive felhőtárhelyhez.
* **📜 Rendszer Log:** Valós idejű eseménynapló a háttérfolyamatok, hálózati műveletek és Auto-Login ellenőrzéséhez.
* **🔄 Automatikus OTA Frissítéskereső:** Induláskor ellenőrzi a legújabb kiadásokat a megadott távoli szerveren vagy GitHub Releases-en.

---

## 🔒 Biztonság & Adatvédelem

* **Helyi kulcsgenerálás:** A program az első indításakor egy egyedi, kriptográfiailag biztonságos 256 bites titkosítási kulcsot hoz létre (`vik_os_secret.key`).
* **Helyi tárolás:** A mentett jelszavak és azonosítók kizárólag a saját gépeden, titkosítva tárolódnak, semmilyen külső szerverre nem kerülnek feltöltésre.
* **Telepítés előtti tisztaság:** A git tároló nem tartalmaz személyes adatokat, profilokat vagy bejelentkezési sütiket.

---


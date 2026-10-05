# cv02: CSS a formulár

Teória a ukážky: <https://beata.stehlikova.website.tuke.sk/ti/03.html>

**Odovzdávaš:** `index.html`, `form.html`, `css/style.css`, `img/obrazok.jpg` v tomto repozitári (commit a push do konca cvičenia, ideálne commit po každej úlohe) a rovnaké súbory na sigma v `public_html/ti/cv02`.

**Úloha 3.1: Zadanie a klon.** Prijmi zadanie *cv02* v Classroom 50 a repozitár naklonuj do `~/web/ti/cv02` podľa návodu [04 Odovzdávanie](https://beata.stehlikova.website.tuke.sk/navody/04-odovzdavanie.html). Ak sa po reštarte Kubeflow stratilo rozšírenie SFTP, vráti ho tento príkaz v termináli:

```bash
code-server --install-extension Natizyskunk.sftp --install-extension yandeu.five-server --install-extension bmewburn.vscode-intelephense-client --install-extension mblode.twig-language-2
```

Potom `F1`, **Developer: Reload Window**. Nastavenie pripojenia na sigma zostáva.

**Úloha 3.2: Vygeneruj web.** Prompt nižšie vlož do AI a na koniec doplň tému svojho semestrálneho projektu. Výsledok ulož do `~/web/ti/cv02` presne v tejto štruktúre: `index.html`, `form.html`, priečinok `css` so `style.css`, priečinok `img`. Do `img` pretiahni vlastný obrázok a premenuj ho na `obrazok.jpg`. Stránky si pozri cez Five Server. **Prečítaj komentáre v kóde — sú tvoja učebnica; každý riadok musíš vedieť vysvetliť.**

```text
Vytvor mi jednoduchý web v HTML5 v slovenčine (lang="sk", kódovanie UTF-8),
dve stránky a jeden samostatný súbor so štýlmi. Bez JavaScriptu a bez
frameworkov (žiadny Bootstrap).

Štruktúra súborov, presne takto:
- index.html
- form.html
- css/style.css (jediné miesto so štýlmi, žiadne inline štýly ani <style>)
- img/obrazok.jpg (obrázok dodám sám)

index.html obsahuje:
- hlavičku s nadpisom h1 a vodorovné menu s odkazmi na index.html a form.html
  (menu je rovnaké na oboch stránkach),
- aspoň dve sekcie s nadpismi h2 a odsekmi textu, jedna sekcia má id,
- obrázok img/obrazok.jpg s atribútom alt,
- pätičku s menom a rokom.

form.html obsahuje to isté menu a formulár s method="get" (zatiaľ bez
spracovania — neskôr ho napojíme na PHP, preto KAŽDÉ pole musí mať atribút
name a vlastný label):
- textové pole (meno), e-mail (type="email"), číslo (type="number"),
  dátum (type="date"),
- select s aspoň tromi možnosťami,
- skupinu troch radio tlačidiel s rovnakým name,
- dva checkboxy,
- textarea na správu,
- odosielacie tlačidlo.

CSS v css/style.css: čitateľné písmo, obsah s obmedzenou šírkou centrovaný cez
max-width a margin auto, farebne odlíšené nadpisy, menu položky vedľa seba,
vzhľad formulára (polia pod sebou, label nad poľom, odsadenia), obrázok nesmie
pretiecť mimo stránku. Použi selektory na elementy, aspoň jednu triedu a aspoň
jeden id selektor.

Do HTML aj CSS napíš krátke slovenské komentáre ku každému bloku, ktoré
vysvetlia, čo robí a prečo — učím sa z nich.

Téma webu: [DOPLŇ tému svojho projektu]
```

**Úloha 3.3: Selektory.** Jedným pravidlom v `style.css` zmeň farbu všetkých nadpisov `h2` na oboch stránkach. Vytvor triedu `.zvyraznene` (napr. farba pozadia alebo rámik) a použi ju aspoň na dvoch rôznych prvkoch na dvoch rôznych stránkach. Prvku, ktorý má `id`, zmeň štýl cez `#id` selektor.

**Úloha 3.4: Box model.** Sekciám nastav vnútorný odstup (padding) a obrázku rámik (border) s vonkajším odstupom (margin). V prehliadači cez F12 si na obrázku pozri diagram box modelu a over, že hodnoty sedia.

**Úloha 3.5: Pozicovanie.** Pripni menu na vrch okna (`position: fixed`) a zariaď, aby neprekrývalo obsah (odsadenie obsahu zhora). V jednej sekcii nastav rodiča ako `position: relative` a umiestni do jej rohu malý prvok (štítok alebo obrázok) cez `position: absolute`.

**Úloha 3.6: Formulár.** Pridaj do formulára jedno nové pole typu, ktorý tam ešte nie je — aj s `label` a `name`.

**Úloha 3.7: Oživenie.** Položkám menu pridaj `:hover` a poliam formulára `:focus` s viditeľnou zmenou (farba, rámik).

**Úloha 3.8: Odovzdanie.** Commit a push podľa návodu [04 Odovzdávanie](https://beata.stehlikova.website.tuke.sk/navody/04-odovzdavanie.html). Klikni pravým na priečinok `cv02` a v menu úplne dole zvoľ **Upload Folder** — na sigma tým doplníš aj pretiahnutý obrázok (pri ukladaní v editore sa nahráva samo, obrázok nie). Over v prehliadači `https://sigma.tuke.sk/student/meno.priezvisko/ti/cv02/` — obe stránky aj obrázok.

---

# cv02: CSS and a form (English)

Theory and examples: <https://beata.stehlikova.website.tuke.sk/ti/03.html> (switch to EN at the top)

**You submit:** `index.html`, `form.html`, `css/style.css`, `img/obrazok.jpg` in this repository (commit and push by the end of the lab, ideally one commit per task) and the same files on sigma in `public_html/ti/cv02`.

**Task 3.1: Assignment and clone.** Accept the assignment *cv02* in Classroom 50 and clone the repository into `~/web/ti/cv02` following guide [04 Submitting](https://beata.stehlikova.website.tuke.sk/navody/04-odovzdavanie.html). If the SFTP extension disappeared from Kubeflow after a restart, this terminal command brings it back:

```bash
code-server --install-extension Natizyskunk.sftp --install-extension yandeu.five-server --install-extension bmewburn.vscode-intelephense-client --install-extension mblode.twig-language-2
```

Then `F1`, **Developer: Reload Window**. The sigma connection settings stay.

**Task 3.2: Generate the web.** Paste the prompt below into an AI and add the topic of your semester project at the end. Save the result into `~/web/ti/cv02` exactly in this structure: `index.html`, `form.html`, a `css` folder with `style.css`, an `img` folder. Drag your own image into `img` and rename it to `obrazok.jpg`. View the pages with Five Server. **Read the comments in the code — they are your textbook; you must be able to explain every line.**

```text
Create a simple two-page website in HTML5 (set lang to the page language,
UTF-8 encoding) with one separate stylesheet. No JavaScript and no frameworks
(no Bootstrap).

File structure, exactly like this:
- index.html
- form.html
- css/style.css (the only place with styles, no inline styles and no <style>)
- img/obrazok.jpg (I will supply the image)

index.html contains:
- a header with an h1 heading and a horizontal menu linking to index.html and
  form.html (the same menu on both pages),
- at least two sections with h2 headings and paragraphs, one section has an id,
- the image img/obrazok.jpg with an alt attribute,
- a footer with my name and the year.

form.html contains the same menu and a form with method="get" (no processing
yet — we will connect it to PHP later, so EVERY field must have a name
attribute and its own label):
- a text field (name), an e-mail (type="email"), a number (type="number"),
  a date (type="date"),
- a select with at least three options,
- a group of three radio buttons sharing one name,
- two checkboxes,
- a textarea for a message,
- a submit button.

CSS in css/style.css: readable font, content width limited and centred with
max-width and margin auto, coloured headings, menu items side by side, form
styling (fields below each other, label above the field, spacing), the image
must not overflow the page. Use element selectors, at least one class and at
least one id selector.

Add short comments to both the HTML and the CSS for every block, explaining
what it does and why — I learn from them.

Website topic: [FILL IN your project topic]
```

**Task 3.3: Selectors.** With one rule in `style.css` change the colour of all `h2` headings on both pages. Create a class `.zvyraznene` (e.g. background colour or a border) and use it on at least two different elements on two different pages. Change the style of the element that has an `id` via a `#id` selector.

**Task 3.4: Box model.** Give the sections inner spacing (padding) and the image a border with outer spacing (margin). In the browser, open F12, look at the box model diagram on the image and check that the values match.

**Task 3.5: Positioning.** Pin the menu to the top of the window (`position: fixed`) and make sure it does not cover the content (offset the content from the top). In one section set the parent to `position: relative` and place a small element (a label or an image) in its corner with `position: absolute`.

**Task 3.6: The form.** Add one new field of a type that is not in the form yet — with a `label` and a `name`.

**Task 3.7: Bring it to life.** Add `:hover` to the menu items and `:focus` to the form fields with a visible change (colour, border).

**Task 3.8: Submitting.** Commit and push following guide [04 Submitting](https://beata.stehlikova.website.tuke.sk/navody/04-odovzdavanie.html). Right-click the `cv02` folder and at the very bottom of the menu choose **Upload Folder** — this also gets the dragged image to sigma (saves in the editor upload themselves, the image does not). Check in the browser `https://sigma.tuke.sk/student/name.surname/ti/cv02/` — both pages and the image.

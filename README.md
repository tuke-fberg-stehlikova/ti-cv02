# cv02: Formuláre a CSS

Stránka týždňa s teóriou a ukážkami: https://beata.stehlikova.website.tuke.sk/ti/03.html

## Odovzdávaš

V repository *cv02* na GitHub a vo svojom webovom priestore na sigma (`ti/cv02`):

- `index.html`, `form.html`, `css/style.css`, `img/photo.jpg`,
- všetky štýly v `css/style.css`, v HTML nie sú inline štýly ani `<style>`.

## Hodnotenie

1 bod. Web je na sigma: obe stránky aj obrázok (image); form sa dá odoslať a údaje sú v adresnom riadku. Commit a push najneskôr do nasledujúceho cvičenia. Po každom push sa spustia automatické testy; výsledok nájdeš podľa návodu [04 Odovzdávanie](https://beata.stehlikova.website.tuke.sk/navody/04-odovzdavanie.html), časť 6.

## Prompty pre AI

Na miestach `// DOPLŇ` a `[DOPLŇ …]` dopĺňaš sám.

### Ukážka 4: prompt pre AI na dvojstránkový web

```text
Vytvor mi jednoduchý web v HTML5 v slovenčine (lang="sk", kódovanie UTF-8),
dve stránky a jeden samostatný súbor so štýlmi. Bez JavaScriptu a bez
frameworkov (žiadny Bootstrap).

Štruktúra súborov, presne takto:
- index.html
- form.html
- css/style.css (jediné miesto so štýlmi, žiadne inline štýly ani <style>)
- img/photo.jpg (image dodám sám)

index.html obsahuje:
- header s heading h1 a vodorovné menu s links na index.html a form.html
  (menu je rovnaké na oboch stránkach),
- aspoň dve section s headings h2 a paragraphs textu, jedna section má id,
- image img/photo.jpg s attribute alt,
- footer s menom a rokom.

form.html obsahuje to isté menu a form <form method="get" action="">
(zatiaľ bez spracovania, neskôr ho napojíme na PHP). Fields:
- textové field (meno), e-mail (type="email"), číslo (type="number" s min
  a max), dátum (type="date"),
- select s aspoň tromi možnosťami; prvá možnosť je
  <option value="">-- vyber --</option>,
- skupinu troch radio tlačidiel vo <fieldset> s <legend>, jedno má checked,
- skupinu dvoch checkboxov vo <fieldset> s <legend>, z ktorých sa dá vybrať
  viac,
- jeden samostatný checkbox na súhlas s value="yes",
- textarea na správu,
- odosielacie button <button type="submit">.

Pravidlá pre KAŽDÉ field form (kvôli PHP):
- attribute name: malé písmená, bez diakritiky a bez medzier, slová spojené
  podčiarkovníkom (napr. since); každé name je iné,
- attribute id a vlastný <label for="..."> s tým istým id,
- každá možnosť (option, radio, checkbox) má attribute value s krátkou
  hodnotou bez diakritiky a bez medzier,
- radio v skupine majú rovnaké name,
- skupina checkboxov má name s hranatými zátvorkami (napr. interest[]).

CSS v css/style.css: čitateľné písmo, obsah s obmedzenou šírkou centrovaný cez
max-width a margin auto, farebne odlíšené headings, menu položky vedľa seba,
vzhľad form (fields pod sebou, label nad field, odsadenia), image nesmie
pretiecť mimo stránku. Použi selectors na elementy, aspoň jednu class a aspoň
jeden id selector.

Do HTML aj CSS napíš krátke slovenské komentáre ku každému bloku, ktoré
vysvetlia, čo robí a prečo — učím sa z nich.

Téma webu: [DOPLŇ tému svojho projektu]
```

## Úlohy

**Úloha 3.1: Príprava Kubeflow a zadanie.** Priprav si Kubeflow podľa návodu [04 Odovzdávanie](https://beata.stehlikova.website.tuke.sk/navody/04-odovzdavanie.html), časť 1: v Explorer je hore WEB, dole na stavovej lište je **Go Live**. Ak tam nie je, rozšírenia vráti tento príkaz v termináli:

```bash
code-server --install-extension Natizyskunk.sftp --install-extension yandeu.five-server --install-extension bmewburn.vscode-intelephense-client --install-extension mblode.twig-language-2
```

Potom `F1`, **Developer: Reload Window**. Nastavenie pripojenia na sigma zostáva. Prijmi zadanie *cv02* v Classroom 50 (link je vyššie) a repository naklonuj do `~/web/ti/cv02` podľa návodu 04, časti 2 a 3.

**Úloha 3.2: Vygeneruj web.** Prompt z Ukážky 4 vlož do AI a na koniec doplň tému svojho projektu. Výsledok ulož do `~/web/ti/cv02` presne v štruktúre z promptu. Do `img` pretiahni vlastný obrázok (image) a premenuj ho na `photo.jpg`. Stránky si pozri cez Five Server. **Prečítaj komentáre v kóde — každý riadok musíš vedieť vysvetliť.**

**Úloha 3.3: Selectors.** Jedným pravidlom v `style.css` zmeň farbu všetkých nadpisov (headings) `h2` na oboch stránkach. Vytvor class `.highlight` (napr. farba pozadia alebo rámik) a použi ju aspoň na dvoch rôznych elements na dvoch rôznych stránkach. Element, ktorý má `id`, zmeň štýl cez `#id` selector.

**Úloha 3.4: Box model.** Sekciám (Sections) nastav vnútorný odstup (padding) a image rámik (border) s vonkajším odstupom (margin). V prehliadači cez F12 si na image pozri diagram box modelu a over, že hodnoty sedia.

**Úloha 3.5: Pozicovanie.** Pripni menu na vrch okna (`position: fixed`) a zariaď, aby neprekrývalo obsah (odsadenie obsahu zhora). V jednej section nastav rodiča ako `position: relative` a umiestni do jej rohu malý element (štítok alebo image) cez `position: absolute`.

**Úloha 3.6: Form.** Pridaj do form jedno nové field typu, ktorý tam ešte nie je — aj s `label` a `name`. Odošli form a v adresnom riadku nájdi svoje údaje.

**Úloha 3.7: Oživenie.** Položkám menu pridaj `:hover` a fields form `:focus` s viditeľnou zmenou (farba, rámik).

**Úloha 3.8: Odovzdanie.** Commit a push podľa návodu [04 Odovzdávanie](https://beata.stehlikova.website.tuke.sk/navody/04-odovzdavanie.html), časť 5. Potom podľa časti 7 klikni pravým na priečinok `cv02` a v menu úplne dole zvoľ **Upload Folder**. Na sigma tým doplníš aj pretiahnutý image: pri ukladaní v editore sa súbor nahráva sám, pretiahnutý image nie. Over v prehliadači `https://sigma.tuke.sk/student/meno.priezvisko/ti/cv02/`: obe stránky aj image.

**Hodnotenie:** 1 bod. V repository *cv02* na GitHub aj na sigma je funkčný web: `index.html`, `form.html`, `css/style.css`, `img/photo.jpg`, a úlohy sú splnené. Commit a push najneskôr do nasledujúceho cvičenia.

---

# cv02: Forms and CSS

The week page with theory and examples: https://beata.stehlikova.website.tuke.sk/ti/03.html

## What you submit

In the repository *cv02* on GitHub and in your web space on sigma (`ti/cv02`):

- `index.html`, `form.html`, `css/style.css`, `img/photo.jpg`,
- all styles in `css/style.css`, no inline styles or `<style>` in the HTML.

## Grading

1 point. The website is on sigma: both pages and the image; the form can be submitted and the data is in the address bar. Commit and push by the next lab at the latest. Automatic tests run after every push; find the result following guide [04 Submitting](https://beata.stehlikova.website.tuke.sk/navody/04-odovzdavanie.html), part 6.

## AI prompts

You fill in the `// DOPLŇ` and `[FILL IN …]` places yourself.

### Example 4: an AI prompt for a two-page website

```text
Create a simple two-page website in HTML5 (set lang to the page language,
UTF-8 encoding) with one separate stylesheet. No JavaScript and no frameworks
(no Bootstrap).

File structure, exactly like this:
- index.html
- form.html
- css/style.css (the only place with styles, no inline styles and no <style>)
- img/photo.jpg (I will supply the image)

index.html contains:
- a header with an h1 heading and a horizontal menu linking to index.html and
  form.html (the same menu on both pages),
- at least two sections with h2 headings and paragraphs, one section has an id,
- the image img/photo.jpg with an alt attribute,
- a footer with my name and the year.

form.html contains the same menu and a form <form method="get" action="">
(no processing yet, we will connect it to PHP later). Fields:
- a text field (name), an e-mail (type="email"), a number (type="number"
  with min and max), a date (type="date"),
- a select with at least three options; the first option is
  <option value="">-- select --</option>,
- a group of three radio buttons in a <fieldset> with a <legend>, one has
  checked,
- a group of two checkboxes in a <fieldset> with a <legend>, where several
  can be ticked,
- one single checkbox for agreement with value="yes",
- a textarea for a message,
- a submit button <button type="submit">.

Rules for EVERY form field (because of PHP):
- a name attribute: lowercase, no accents, no spaces, words joined by an
  underscore (e.g. since); every name is different,
- an id attribute and its own <label for="..."> with the same id,
- every option (option, radio, checkbox) has a value attribute with a short
  value without accents and spaces,
- radios in a group share one name,
- a checkbox group has a name with square brackets (e.g. interest[]).

CSS in css/style.css: readable font, content width limited and centred with
max-width and margin auto, coloured headings, menu items side by side, form
styling (fields below each other, label above the field, spacing), the image
must not overflow the page. Use element selectors, at least one class and at
least one id selector.

Add short comments to both the HTML and the CSS for every block, explaining
what it does and why — I learn from them.

Website topic: [FILL IN your project topic]
```

## Tasks

**Task 3.1: Getting Kubeflow ready and the assignment.** Get Kubeflow ready following guide [04 Submitting](https://beata.stehlikova.website.tuke.sk/navody/04-odovzdavanie.html), part 1: Explorer shows WEB at the top, the status bar at the bottom shows **Go Live**. If it does not, this terminal command brings the extensions back:

```bash
code-server --install-extension Natizyskunk.sftp --install-extension yandeu.five-server --install-extension bmewburn.vscode-intelephense-client --install-extension mblode.twig-language-2
```

Then `F1`, **Developer: Reload Window**. The sigma connection settings stay. Accept the assignment *cv02* in Classroom 50 (the link is above) and clone the repository into `~/web/ti/cv02` following guide 04, parts 2 and 3.

**Task 3.2: Generate the web.** Paste the prompt from Example 4 into an AI and add the topic of your project at the end. Save the result into `~/web/ti/cv02` exactly in the structure from the prompt. Drag your own image into `img` and rename it to `photo.jpg`. View the pages with Five Server. **Read the comments in the code — you must be able to explain every line.**

**Task 3.3: Selectors.** With one rule in `style.css` change the colour of all `h2` headings on both pages. Create a class `.highlight` (e.g. background colour or a border) and use it on at least two different elements on two different pages. Change the style of the element that has an `id` via a `#id` selector.

**Task 3.4: Box model.** Give the sections inner spacing (padding) and the image a border with outer spacing (margin). In the browser, open F12, look at the box model diagram on the image and check that the values match.

**Task 3.5: Positioning.** Pin the menu to the top of the window (`position: fixed`) and make sure it does not cover the content (offset the content from the top). In one section set the parent to `position: relative` and place a small element (a label or an image) in its corner with `position: absolute`.

**Task 3.6: The form.** Add one new field of a type that is not in the form yet — with a `label` and a `name`. Submit the form and find your data in the address bar.

**Task 3.7: Bring it to life.** Add `:hover` to the menu items and `:focus` to the form fields with a visible change (colour, border).

**Task 3.8: Submitting.** Commit and push following guide [04 Submitting](https://beata.stehlikova.website.tuke.sk/navody/04-odovzdavanie.html), part 5. Then, following part 7, right-click the `cv02` folder and choose **Upload Folder** at the very bottom of the menu. This also gets the dragged image to sigma: a file saved in the editor is uploaded by itself, a dragged image is not. Check in the browser `https://sigma.tuke.sk/student/name.surname/ti/cv02/`: both pages and the image.

**Grading:** 1 point. The repository *cv02* on GitHub and on sigma contains a working website: `index.html`, `form.html`, `css/style.css`, `img/photo.jpg`, and the tasks are done. Commit and push by the next lab at the latest.

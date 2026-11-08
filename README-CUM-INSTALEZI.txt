# Calendar Perpetuu Brai-Cata - Pachet pentru Instalare ca Aplicatie (PWA)

Acest folder contine tot ce ai nevoie ca sa instalezi calendarul ca aplicatie pe telefon / calculator.

## Ce contine folderul
- index.html - calendarul complet (perpetuu 2026 - infinit, ceas sub titlu, mod intunecat, cautare fara diacritice)
- manifest.webmanifest - buletinul aplicatiei (nume, iconita, culori, deschidere pe tot ecranul)
- sw.js - service worker, salveaza calendarul pentru offline
- icon-192.png, icon-512.png, icon-maskable-512.png, apple-touch-icon.png - iconite

## Cum il pui pe internet (obligatoriu pentru instalare completa)

Ai nevoie de HTTPS. Variante gratuite, 2 minute:

### Varianta 1 - Netlify Drop (cea mai simpla)
1. Intra pe https://app.netlify.com/drop
2. Trage tot folderul `calendar-pwa` in pagina
3. Iti da un link gen https://calendar-brai-cata.netlify.app
4. Deschide linkul pe telefon si instaleaza

### Varianta 2 - GitHub Pages
1. Creeaza un repo nou pe GitHub, de exemplu `calendar-brai-cata`
2. Uploadeaza toate fisierele din acest folder in repo (nu folderul, ci fisierele direct)
3. Settings > Pages > Branch: main, Folder: / (root) > Save
4. Linkul va fi https://NUMELE-TAU.github.io/calendar-brai-cata/

### Varianta 3 - Vercel / Cloudflare Pages
La fel ca Netlify: tragi folderul si primesti link.

## Cum instalezi dupa ce ai linkul

### Android - Chrome
1. Deschide linkul in Chrome
2. Apare automat butonul verde "Instaleaza aplicatia" jos in dreapta, apasa-l
3. Sau: meniu (3 puncte) > Adauga pe ecranul principal / Instaleaza aplicatia
4. Iti apare iconita Brai-Cata pe ecran

### iPhone - Safari
1. Deschide linkul in Safari (nu in Chrome pe iPhone, trebuie Safari)
2. Apasa Share (patrat cu sageata in sus) jos
3. Alege "Adauga pe ecranul principal"
4. Apasa Adauga
5. Aplicatia arata un mic mesaj explicativ automat la prima deschidere

### Calculator - Chrome / Edge
1. Deschide linkul
2. In bara de adresa apare o iconita de instalare, apasa-o
3. Alege Instaleaza
4. Se deschide ca aplicatie separata, fara bara de browser

## Ce se intampla dupa instalare
- Se deschide pe tot ecranul, ca o aplicatie
- Merge si fara internet dupa prima deschidere
- Tine minte modul intunecat
- Iconita pe ecran: cerc alb cu P galben, H albastru, S verde, pe fundal verde Brai-Cata

## Testare locala
Daca deschizi index.html direct din calculator (file://), butonul Instaleaza nu va aparea - e normal, browserul cere HTTPS.
Pentru testare, poti porni un server local:
  python3 -m http.server 8000
si deschizi http://localhost:8000

## Daca vrei sa schimbi ceva
Editeaza index.html, apoi re-uploadeaza folderul. Versiunea service worker-ului (v1) se va actualiza automat la urmatoarea deschidere.

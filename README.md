# Milica Divine Code — sajt

Statičan sajt (čist HTML/CSS/JS). Nema build-a, nema baze — samo fajlovi.
Da bi radio, **svi fajlovi moraju ostati u istom folderu** (HTML + slike + logo).

## Stranice
- `index.html` — početna
- `o-meni.html` — O meni
- `afirmacije.html` — Divine invokacija (dnevna afirmacija)
- Usluge: `golden-key.html`, `show-up.html`, `sunkissed.html`,
  `golden-timing.html`, `golden-key-mentorship.html`, `cosmic-match.html`,
  `golden-silence.html`
- Slike/logo: `milica-hero.jpg`, `milica-portrait.jpg`, `milica-smile.jpg`,
  `milica-yellow1.jpg`, `milica-yellow2.jpg`, `logo-full.png`, `logo-mark.png`,
  `workshop-popup.jpg` (popup banner)
- Besplatni PDF-ovi za preuzimanje: `divine-birthday-journal.pdf`,
  `inner-self-workbook.pdf`

## Ponašanje
- Popup sa radionicom (`workshop-popup.jpg`) iskoči pri ulasku na početnu,
  sa X za zatvaranje; ne pojavljuje se ponovo istog dana (pamti se u browseru).
- Sva „Zakaži"/kontakt dugmad otvaraju mejl na `milicadivinecode@gmail.com`.
- Footer: mejl + Instagram (@milica.divinecode). Broj telefona uklonjen.

## Deploy na Vercel — najlakši način (bez Git-a)
1. Instaliraj Node.js (nodejs.org) ako ga nemaš.
2. Otvori terminal u ovom folderu i pokreni:
   ```
   npx vercel
   ```
3. Prati pitanja (login, ime projekta, „directory" = enter za trenutni folder).
   Vercel odmah izbaci privremeni link za testiranje.
4. Za objavu na produkciju: `npx vercel --prod`

## Alternativa: GitHub + Vercel (bolje za buduće izmene)
1. Ubaci ceo folder u novi GitHub repo.
2. Na vercel.com → Add New → Project → Import taj repo → Deploy.
3. Svaka izmena u repou se automatski objavi.

## Povezivanje GoDaddy domena
1. U Vercel projektu: Settings → Domains → dodaj domen (i sa i bez `www`).
2. Vercel prikaže TAČNE DNS vrednosti za taj projekat (A i CNAME) — koristi baš njih.
3. U GoDaddy → DNS → Manage DNS: dodaj te zapise.
   - VAŽNO: obriši GoDaddy-jev postojeći „Parked" A zapis (`@`) i isključi
     parking/forwarding — inače Vercel ostaje na „Invalid Configuration".
4. Sačekaj propagaciju (par minuta do 24h). Vercel automatski izda besplatan HTTPS.

## Napomene / TODO (dogovoreno za kasnije)
- Newsletter forma trenutno samo prikazuje poruku „hvala" — još ne šalje nigde.
  Kad se izabere servis (MailerLite / Mailchimp / Buttondown), povezuje se forma.
- Popup slika za radionicu — dodaje se naknadno.
- Dugmad „Zakaži" vode na kontakt u futeru; kad bude Calendly, menjaju se linkovi.

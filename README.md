# Godimento Picerija

Sajt Godimento picerije, Pariske Komune 27, Novi Beograd.

Statična stranica bez build koraka: `index.html` i folder `images/`.
GSAP (ScrollTrigger, SplitText) i fontovi se učitavaju sa CDN-a.

## Objavljivanje na GitHub Pages

1. Postavi sve fajlove u koren repozitorijuma.
2. Settings > Pages > Source: Deploy from a branch, grana `main`, folder `/ (root)`.
3. Za domen godimento.rs: u Settings > Pages upiši `godimento.rs` u Custom domain,
   pa kod registra domena dodaj DNS zapise:
   - A zapisi za `@`: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - CNAME za `www`: `<korisnik>.github.io`
4. Uključi "Enforce HTTPS" kada se sertifikat izda.

## Izmena cenovnika (admin)

Cenovnik se nalazi u fajlu `menu.json`. Sajt ga učitava pri svakom otvaranju,
pa nema baze ni servera.

Admin stranica: `/admin.html` (na primer https://gru-webdesign.github.io/godimento/admin.html).
Na njoj se menjaju nazivi, sastojci i cene, i dodaju, uklanjaju i premeštaju stavke.
Dugme "Sačuvaj na sajt" upisuje novi `menu.json` u repozitorijum, a sajt prikazuje izmene za oko minut.

Za čuvanje je potreban GitHub ključ, jednom po browseru:
1. https://github.com/settings/personal-access-tokens/new
2. Repository access: Only select repositories, izaberi `godimento`
3. Repository permissions: Contents, Read and write
4. Generate token, pa ga nalepi u admin pod "GitHub ključ"

Ključ ostaje samo u tom browseru (localStorage). Bez ključa admin stranica može da prikaže cenovnik, ali ne može ništa da sačuva.
Admin nije povezan sa sajta i ima `noindex`, pa ga pretraživači ne prikazuju.

## Zasluge

- Fotografije sendviča, tortilje i palačinki: Unsplash (Unsplash licenca)
- Mapa: © OpenStreetMap saradnici

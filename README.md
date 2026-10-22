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

## Izmena cena

Cene su direktno u `index.html`:
- pice: atributi `data-p32`, `data-p42`, `data-p50` na svakom `<li class="pz">`, i prikazana cena za 32 cm u `<strong class="pz-cur">`
- palačinke: `data-v` i tekst u ćelijama tabela

## Zasluge

- Fotografije sendviča, tortilje i palačinki: Unsplash (Unsplash licenca)
- Mapa: © OpenStreetMap saradnici

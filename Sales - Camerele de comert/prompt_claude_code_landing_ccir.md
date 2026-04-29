Creează un landing page nou la `/ccir/` după același șablon ca `/imperia/` dar cu elemente vizuale grafica adaptate www.ccir.ro > vezi CCI

### Context comercial
- Pagina este dedicată membrilor Camerei de Comerț și Industrie a României (CCIR).
- Model: Camera = canal de distribuție, VOGO = furnizor, beneficii pentru membri (Camera nu plătește nimic).
- Ofertă valabilă pentru contractele încheiate până la **31 mai 2026**.
- 4 beneficii pentru membri:
  1. Prețuri preferențiale la licențe și servicii
  2. Suport premium inclus în preț
  3. Account manager dedicat
  4. Creșterea vânzărilor + scăderea/eliminarea comisioanelor pe platforme terțe (Glovo, Bolt Food, eMag, Tazz)
- Tonalitate: instituțională + premium (mai sobră decât Imperia, dar la fel de îngrijită).

### Pași concreți

**1. Copiază integral folderul `/imperia/` în `/ccir/`** (cu tot cu `/img/` și `index.html`).

**2. În `/ccir/index.html` aplică înlocuirile de mai jos.**

#### A. Meta tags & SEO
- `<title>`: `VOGO pentru membrii CCIR — aplicația ta mobilă, fără comisioane platformă`
- `meta description`: `Pagină dedicată membrilor Camerei de Comerț și Industrie a României: cum lansezi rapid o aplicație mobilă iOS și Android pentru afacerea ta, cu tehnologia VOGO. Ofertă specială până la 31 mai 2026.`
- `og:url` și `<link rel="canonical">`: `https://vogo.me/ccir/`
- `meta robots`: schimbă din `noindex, follow` în `index, follow` (CCIR e public)

#### B. Header & branding
- Textul nav-meta: `Pentru membrii CCIR` (în loc de `Pentru membrii Imperia Club`)
- Footer: `Imperia Club` → `Camera de Comerț și Industrie a României`; linkul `https://www.imperiaclub.ro/` → `https://ccir.ro/`

#### C. Hero
- Eyebrow: `Exclusiv · Pentru Membrii CCIR`
- H1: `Aplicația mobilă a afacerii tale + reducerea comisioanelor de pe platforme — la <em>un click distanță</em>.`
- Lead: `Pentru companiile membre CCIR, VOGO Technology oferă o cale directă, conformă și rapidă de a transforma WordPress sau WooCommerce într-o aplicație mobilă iOS și Android — cu canal de vânzare propriu și fără comisioanele platformelor terțe (Glovo, Bolt Food, eMag, Tazz).`
- CTA primar: `Cere aplicația mobilă`
- CTA secundar: `Vezi demo live`

#### D. Galerie (Preview)
- Kicker: `Preview`
- H2: `Aplicația ta. Brandul tău. Comisioane zero.`
- Sub: `<strong>Mai multe vânzări. Clienți care revin. Customer service direct — fără intermediari care iau 20-30% per comandă.</strong><br />Interfață curată, fluxuri scurte, mesagerie directă cu clientul — totul personalizat cu logo-ul, culorile și identitatea ta.`

#### E. Secțiune NOUĂ „Beneficii speciale CCIR" (chiar înainte de CTA, în stilul `imp-steps-section`)
- Kicker: `Pentru contractele până la 31 mai 2026`
- H2: `4 beneficii exclusive pentru membrii CCIR`
- 4 itemi în info-box (folosind aceeași listă numerotată ca la „Short Summary"):
  1. **Prețuri preferențiale** — la licențe și la servicii, sub tarifele standard de listă.
  2. **Suport premium inclus** — fără cost suplimentar pe durata contractului.
  3. **Account manager dedicat** — un singur punct de contact pentru toate solicitările tale.
  4. **+ Vânzări, − Comisioane** — canal direct cu clientul prin app-ul tău mobil, fără 20-30% datorați platformelor terțe.
- Sub info-box, banner de urgență: `Ofertă valabilă pentru contractele încheiate până la 31 mai 2026 · Disponibilă exclusiv membrilor CCIR`

#### F. Marquee gold (banda animată)
Înlocuiește textele actuale cu:
- `Made in Europe`
- `ISO 9001 · ISO 27001 · GDPR by Design`
- `Aplicații mobile native iOS + Android`
- `★ Special pentru membrii CCIR — până la 31 mai 2026`
- `Fără comisioane platformă · Canal direct cu clientul`

#### G. Video section
Păstrează cele două video-uri (sunt despre activarea plugin-ului WordPress și a aplicației mobile, valabile pentru orice membru). Schimbă doar:
- Sub titlu: `Două filme scurte. Activare WordPress + primul login mobil — în mai puțin de 4 minute total.`

#### H. CTA section (form WhatsApp)
- H2: `Pornim aplicația ta.`
- Sub: `Alege varianta rapidă — înregistrează-te și pornești singur — sau scrie-ne câteva detalii și un consultant VOGO te contactează direct pe WhatsApp. Contractele încheiate până la 31 mai 2026 beneficiază de prețuri preferențiale CCIR.`
- În JS handler-ul formularului: schimbă `[Chat initiat din /imperia]` → `[Chat initiat din /ccir]`
- Tot la fel pentru linkul WhatsApp de la „Discută cu colegii din suport" (din secțiunea Steps): pre-completare mesaj `[Chat initiat din /ccir - Suport] Salut! Sunt membru CCIR și am o întrebare despre activarea aplicației mobile:`

#### I. Linkuri utile („Resurse complementare")
- Cardul `Imperia Club` → înlocuit cu un card `Camera de Comerț și Industrie a României` → `https://ccir.ro/`
- Restul linkurilor rămân (Produse VOGO, Avantaje clienți, Program parteneri, Demo VOGO Family, Contact formal).

### Recomandări tehnice
- Redenumește prefixurile CSS din `.imp-` în `.ccir-` pentru izolare clară între cele două landing-uri (search-and-replace controlat în `<style>` și în clasele HTML).
- Păstrează același set de certificări (`credibility.png`) — sunt aceleași pentru orice client.
- Asigură-te că path-urile relative către `../img-general/` rămân funcționale după copiere.

### Verificare finală
- `grep -i "imperia"` în `/ccir/index.html` → nu trebuie să mai existe nicio mențiune textuală (referințele CSS dispar dacă ai redenumit prefixurile).
- Deschide `/ccir/index.html` în browser și verifică: hero, galerie, video, secțiunea nouă „Beneficii speciale CCIR", banner-ul cu deadline, formular WhatsApp pre-completat cu `[Chat initiat din /ccir]`.
- Confirmă că butonul „Înregistrează-te" încă duce la `https://vogo.family/register/` și că butonul WhatsApp folosește același număr `40742203383`.

### Raportare
La final spune-mi:
- ce ai schimbat (lista de modificări),
- dacă ai redenumit prefixurile CSS din `.imp-` în `.ccir-`,
- linkul local de preview (ex: `file:///C:/sources/vogo.me/ccir/index.html`).

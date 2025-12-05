# Plan for Fullstack-prosjekt – Tangen Torv

Dette prosjektet er en fullstack-løsning for restauranten **Tangen Torv**. Nettsiden skal vise informasjon om restauranten, meny, åpningstider og kontaktinformasjon. I tillegg skal brukere kunne bestille bord, og ansatte skal kunne se og administrere bestillinger.

Prosjektet består av tre moduler:

---

## Modul 1 – Database
Database for lagring av meny og bordbestillinger. Løsningen skal utvikles med **PostgreSQL**, og kjøres via **Docker/Docker Compose**.

### Planlagt funksjonalitet
- Lagre meny med kategorier (forrett, hovedrett, dessert, drikke)
- Registrere bordbestillinger med navn, kontaktinfo, dato, tidspunkt og antall personer
- Booking skal ha status: **Ny**, **Bekreftet**, **Avlyst**
- (Senere) Ansatte kan oppdatere status på booking

### Leveranser for modul 1
- ER-diagram
- SQL-fil (`schema.sql`) som oppretter tabeller og relasjoner
- SQL-fil (`queries.sql`) med eksempelspørringer (INSERT/SELECT/UPDATE)
- Docker Compose-fil som starter PostgreSQL

---

## 🌐 Modul 2 – Frontend
Statiske nettsider som demonstrerer funksjonalitet uten databasekobling.

### Teknologier
- **HTML**
- **CSS (Vanilla)**
- **JavaScript (vanlig / uten rammeverk)**

### Planlagte sider
| Side | Funksjon |
|------|----------|
| Forside | Info om restauranten |
| Meny | Vise menyer hentet fra hardkodede data |
| Kontakt / Åpningstider | Vise kontaktinfo og åpningstider |
| Bestilling | Skjema for bordbestilling (lagres ikke i modul 2) |
| Ansatt-side | Vise statiske eksempelbestillinger |

---

## ⚙️ Modul 3 – Backend (etter jul)
Backend utvikles med **Node.js + Express**, og kobles til PostgreSQL.

### Planlagt funksjonalitet
- Lagre bestilling i databasen
- Hente meny og bestillinger fra databasen
- Endre status på bestilling (Ny → Bekreftet/Avlyst)

---

## 🗓️ Tidsplan

| Dag | Oppgaver |
|-----|----------|
| Dag 1 | Opprette GitHub-repo, skrive Plan.md, starte README, lage ER-diagramskisse |
| Dag 2 | Ferdigstille ER-diagram og skrive `schema.sql`, opprette Docker Compose |
| Dag 3 | Lage `queries.sql`, teste databasekjøring, starte statisk frontend |
| Dag 4–5 | Ferdigstille statisk frontend (CSS, layout, alle sider), dokumentere |
| Etter jul | Utvikle backend med Express, koble database |

---

## 📚 Dokumentasjon
All dokumentasjon skal ligge i README.md i rotmappen, og lenke videre til andre dokumentasjonsfiler som `DATABASE.md`. Dokumentasjonen skal beskrive teknologier, hvordan systemet kjøres, samt eventuelle feil og videreutviklingsmuligheter.

---

## 🚀 Videreutvikling (frivillig)
Mulige utvidelser etter endt prosjekt:
- Automatisk e-postbekreftelse for booking
- Multispråklig nettside
- Admin-innlogging med roller

# Databasemodell

Dette prosjektet bruker PostgreSQL. Under er ER-diagrammet:

![ER Diagram](docs/er-diagram.png)

# PhoneBOOKV2.2

PhoneBOOK je aplikacija za upravljanje telefonskim imenikom sa lokalnom bazom podataka koristeći SQLite. Korisnici mogu pregledati, dodavati, uređivati i brisati unose u imeniku, a aplikacija koristi različite sigurnosne mjere kako bi zaštitila podatke.

## Zavisnosti

Ovaj projekat koristi sljedeće zavisnosti koje su specificirane u `package.json`:

- **body-parser**: Middleware za parsiranje tijela dolaznih zahtjeva (`req.body`).
- **csurf**: Middleware za zaštitu od CSRF napada.
- **dotenv**: Omogućava čuvanje osjetljivih podataka u `.env` fajlu.
- **ejs**: Šablonski jezik za generisanje dinamičkih HTML stranica.
- **express**: Web framework za Node.js.
- **express-session**: Middleware za rad sa sesijama.
- **helmet**: Middleware za postavljanje sigurnosnih HTTP zaglavlja.
- **joi**: Biblioteka za validaciju korisničkih podataka.
- **sqlite3**: Biblioteka za rad sa SQLite bazama podataka.
- **validator**: Biblioteka za validaciju i sanitizaciju stringova.

## Instalacija

1. Klonirajte repozitorij:
   ```bash
   git clone https://github.com/davud-gobeljic/PhonebookJS.git

2. npm install express sqlite3


Zadatak
Napraviti dinamičku tabelu za index.ejs u sjediste koja se povezuje sa tabelom sjediste.

Podesiti rutu: Kreirati GET rutu u routes/sjediste.js koja povlači podatke iz baze podataka (tabela sjediste) i prosljeđuje ih u index.ejs.

Kreirati dinamičku tabelu u index.ejs: Prikazati podatke iz tabele sjediste unutar tabele pomoću EJS petlji.

Podesiti rute nakon logina da ostane na istoj stranici.

Nakon uspješnog logina, korisnik treba ostati na istoj stranici (ili biti preusmjeren na željenu stranicu). Ovo možeš ostvariti koristeći req.originalUrl ili pohranom trenutne stranice prije login zahtjeva.
Podesiti URL i forma security.

Omogućiti sigurnosne postavke za URL-ove i forme kako bi se spriječile potencijalne prijetnje kao što su CSRF napadi. Dodaj CSRF zaštitu u forme koristeći csurf middleware i generiši CSRF token za svaku formu.

Validacija inputa može se raditi pomoću biblioteke joi za sigurnu obradu podataka.

Upotreba
Pokreni aplikaciju i posjeti localhost:3000 kako bi pristupio aplikaciji. Prilikom prijave u aplikaciju, podaci će biti validirani i aplikacija će osigurati CSRF zaštitu kako bi osigurala sigurnost podataka.

Zaključak
PhoneBOOK je robusna aplikacija koja upravlja unosima u imeniku s naglaskom na sigurnost i jednostavnost korištenja. Dinamički sadržaj se generiše korištenjem EJS-a, a baza podataka koristi SQLite za pohranu i dohvat podataka.



Model-View-Controller (MVC) Pristup
Model-View-Controller (MVC) je arhitektonski obrazac koji pomaže u organizaciji koda i pojednostavljuje razvoj aplikacija. MVC pristup dijeli aplikaciju na tri odvojena dijela:

Model: Odgovoran je za rukovanje podacima aplikacije. On komunicira s bazom podataka i obrađuje poslovnu logiku. U slučaju PhoneBOOK-a, modeli upravljaju podacima iz SQLite baze podataka.

View: Prikazuje podatke korisniku. To su šabloni (npr. EJS) koji renderuju dinamičke HTML stranice koristeći podatke koje im proslijede kontroleri.

Controller: Upravlja logikom aplikacije i posreduje između modela i prikaza (view). Kontroler prima zahtjeve korisnika, komunicira s modelom da dobije potrebne podatke i zatim prosljeđuje te podatke prikazima da ih prikažu korisnicima.

Ovaj pristup omogućava jasnu podjelu odgovornosti i bolju organizaciju koda, što olakšava održavanje, testiranje i proširenje aplikacije.


## Pokretanje aplikacije

Aplikacija se pokreće pomoću sljedeće komande:
node app.js


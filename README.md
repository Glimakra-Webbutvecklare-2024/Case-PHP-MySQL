# Case – PHP + MySQL (CRUD‑applikation)

I det här caset bygger du en full‑stack‑applikation där inloggade användare kan skapa, läsa, uppdatera och ta bort (CRUD) en valfri typ av resurs. Vilken resurs det är bestämmer du själv – t.ex. en receptbok, kontaktbok, diktsamling, twitterklon, fotodagbok … välj något som känns roligt och rimligt att färdigställa inom tidsramen.

Språken du ska använda är PHP, SQL, HTML, CSS och JavaScript.

## 1. Kod‑ & namngivningsprinciper

- Backend / PHP: snake_case för variabler, funktioner och databasnamn
- Frontend / HTML + CSS + JS:	camelCase för variabler & funktioner
- Gemensamt: Välj beskrivande namn, Engelsk namngivning, Kommentera din kod och Använd konsekvent indrag

## 2. Kom‑igång
1.	Skapa ett privat GitHub‑repo och koppla till din lokala miljö (VS Code).
2.	Bjud in lärarna senast 2 maj:
   - addkolon (Mattias)
   - andsju (Anders)
   - frozenbanana (Henry)

## 3. Krav

### 3.1 Projekt‑setup
1. Projektet ska kunna klonas och startas via Docker (t.ex. docker compose up).
2. En README.md ska steg‑för‑steg beskriva:
  3. Installation (krav, hur man startar containrar)
  4. Användning (inloggning, skapa poster, etc.)
  5. Minst en screenshot / gif av appen i drift

### 3.2 Databas‑schema (minimum)

| Tabell        | Kolumner                                                                                           |
|-------------- |----------------------------------------------------------------------------------------------------|
| user          | id INT PK AI<br>username VARCHAR UNIQUE<br>password VARCHAR *(hashad)*                              |
| *din_resurs*<br>ex. recipe, contact, poem | id INT PK AI<br>**minst tre egna fält** (t.ex. title, content, created_at)<br>user_id INT FK → user.id |

Tips: Om din idé behöver fler tabeller (t.ex. “ingredients” till ett recept) är det helt okej – se endast ovan som miniminivå.

### 3.3 Funktionalitet (minimum)

| Roll        | Måste kunna                                                                                           |
|-------------- |----------------------------------------------------------------------------------------------------|
| Besökare          | Se lista över alla resurser (read‑only)                              |
| Inloggad användare| Se samtliga resurser|
| Inloggad användare| Skapa ny resurs|
| Inloggad användare| Uppdatera endast egen resurs |
| Inloggad användare| Ta bort endast egen resurs |
| Applikationen | Hasha lösenord vid användarregistrering |
| Applikationen | Validera all indata som skickas från användaren |

### 3.4 GitHub commits
Du ska ha gjort minst 10 commits över tid.  

## 4. Utmaningar
  1.	Kommentarer – låta användare kommentera en resurs (t.ex. “Snygg dikt!”).
  2.	Bilduppladdning – ladda upp bild kopplad till resursen och spara filnamn/url på ett säkert sätt (filtypcheck, unika filnamn, osv.).
  3.	Publicera appen på t.ex. Hetzner.
  4.	“Draft”‑status: möjliggör privata utkast synliga bara för ägaren.
  5.	Betygsättningar (1‑5 stjärnor).
  7.	Objekt‑orienterad PHP (klasser + modeller).

## 5. Design
- Mobile first lo‑fi skisser.
- Hi‑fi mockups för mobil & desktop.
- Extra: logotyp och färgpalett om du vill.

## 6. Tidsplan & redovisning

| Datum        | Vad händer                                                                                           |
|-------------- |----------------------------------------------------------------------------------------------------|
|2 maj|  GitHub‑repo delat med lärare|
|14 maj|	kl 10.25 halvtidsredovisning – visa ditt pågående arbete
|22 maj| kl 10.25	Slutredovisning (ca 5 min per person, bokstavsordning efternamn)|

Slutredovisningen ska innehålla:

1. Demo: logga in, skapa, uppdatera & ta bort en resurs (och ev. utmaning).
2. Stolthet: det du är mest nöjd med (design, kod, struktur …).
3. Next steps: vad du skulle vilja hinna bygga vidare på.


Lycka till och ha kul!

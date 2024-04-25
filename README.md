# Case-PHP-MySQL

I det här caset ska du skapa en applikation som presenterar verksamheter (företag, föreningar, organisationer) utifrån olika kategorier.
Det ska skapa en fullstack applikation, och därmed använda PHP, MySQL, HTML, CSS och JavaScript. 

Vi vill att du strävar efter följande namngivningsprinciper:

Backend PHP
- använd latinska tecken för variabelnamn och funktioner
- använd namnstandard (PHP och MySQL snake_case)
  
Frontend HTML, CSS, JavaScript
- använd latinska tecken för variabelnamn och funktioner
- använd namnstandard (JavaScript camelCase)

Fler goda principer:
- använd förklarande namn 
- skriv kommentarer i din kod
- sträva efter att vara konsekvent
- skriv kod med indrag (indentation)


### Starta ditt arbete
Skapa ett privat repo på GitHub och koppla det till din lokala utvecklingsmiljö (Visual Studio Code). 

---

**TIPS** 

Använd Anders docker projekt som en grund för caset (Ta bort learn mappen).

eller

Använd en mall som finns för caset - https://github.com/Glimakra-Webbutvecklare-2022/Template-Case-PHP

---

Under projektet - senast 17 Maj bjuder du in dina lärare. Se Settings -> Manage access -> Add people

Lägg till

- addkolon (Mattias)
- andsju (Anders)
- frozenbanana (Henry)

***

## Krav
Applikationen ska kunna laddas ner / klonas från ditt Git repo. Repot ska hantera applikationen i Docker. Det ska finnas instruktioner och funktionalitet för att enkelt komma igång att använda projektet.

Något i stil med:

```sql
CREATE TABLE `user` IF NOT EXISTS ...
```

### Databas krav

Följande tabeller ska finnas:

tabell `user`, med föjande kolumner:
- id (INT, PRIMARY KEY AUTO_INCREMENT)
- username (VARCHAR, UNIQUE)
- password (VARCHAR, **hashed**)

tabell `category`, med föjande kolumner:
- id (INT, PRIMARY KEY AUTO_INCREMENT)
- category (VARCHAR)

tabell `business`, med föjande kolumner:
- id (INT, PRIMARY KEY AUTO_INCREMENT)
- name (VARCHAR)
- address (VARCHAR)
- open_hours (VARCHAR)
- image_url (VARCHAR)
- date_updated (DATETIME NOT NULL DEFAULT current_timestamp())
- user_id (INT FOREIGN KEY table user)
- category_id (INT FOREIGN KEY table category)


## Design minimum
- Low fidelity designskiss
- Mobile first
- Vyer för mobil och skärm

  
## Design Extra
- Logotyp
- Färgtema

## Code minimum
- En README.md i gitrepot med följande delar:
  - Installation: Vad behövs för att man själv ska kunna köra appen?
  - Screenshots: minst en screenshot (eller gif) som visar appen under använding
- En användare ska kunna registrera ett konto
- En användare ska kunna logga in och logga ut
- Inloggad användare ska kunna lägga till verksamheter
- Verksamheter ska kunna redigeras och raderas av den användare som skapat resursen
- Alla verksamheter ska finnas listade den som besöker applikationen
- Alla formulärsfält som registeras till databasen ska valideras (att rätt och rimlig typ att data lagras)

## Code Extra
- Publicerad via Linode eller motsvarade
- Det ska vara möjligt att sätta en verskamhet som draft (ej publicerad - visas endast för användare som skapat resursen)
- Det ska vara möligt att sätta betyg (1-5 stjärnor) på verksamheter
- Det ska vara möjligt att lägga till en kommenter för en verksamhet
- Det ska vara möjligt att lägga till och redigera kategorier via formulär
- 
***

### Redovisning - applikation under utveckling 
Tisdag 14 maj visar du upp ditt pågående arbete med case. Dela erfarenhetet, visa upp ngt från din applikation.


### Inlämning och redovisning
Redovisning av caset är den måndagen den 27 maj kl 10.30 

Vi önksar att alla får ta del av varandras redovisning. Det innebär att ni behöver förbereda er på att redovisningen är kort - ca 5 minuter per person. Då visar ni (demonstrerar) er applikation genom att dela skärm.

*Förbered 5 minuters redovisning enligt följande mall:*

#### I reovisningen ska du:
- demonstrera applikationen
- - visa hur man lägger till, markerar och tar bort resurser
- - visa exempel på annan funktionalitet (ex ngn av utmaningarna)
- berätta vad du är mest nöjd med (design, kod, struktur...)
- berätta vad du skulle vilja att applikationen kan göra, men inte hunnit att koda

Redovisningen sker i bokstavordning (efternamn a-ö)

### Handledning
Det kommer givetvis finnas möjlighet till handledning fram tills den 27 maj. I första hand är det under vanlig lektionstid.

Lycka till!

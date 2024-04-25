# Case-PHP-MySQL

I det här caset ska du skapa en fullstack applikation som presenterar verksamheter (företag, föreningar, organisationer) utifrån olika kategorier.
Språken du ska använda är PHP, SQL, HTML, CSS och JavaScript. 

Vi vill att du strävar efter följande namngivningsprinciper:

Backend PHP
- använd latinska tecken för variabelnamn och funktioner
- följ namnstandard (PHP och MySQL snake_case)
  
Frontend HTML, CSS, JavaScript
- använd latinska tecken för variabelnamn och funktioner
- följ namnstandard (JavaScript camelCase)

Fler goda principer:
- använd förklarande namn 
- skriv kommentarer i din kod
- skriv kod med indrag (indentation)


### Starta ditt arbete
Skapa ett privat repo på GitHub och koppla det till din lokala utvecklingsmiljö (Visual Studio Code). 

Senast 2 maj bjuder du in dina lärare till ditt repo. Se Settings -> Manage access -> Add people

Lägg till

- addkolon (Mattias)
- andsju (Anders)
- frozenbanana (Henry)

***

## Krav
Applikationen ska kunna laddas ner / klonas från ditt Git repo. Repot ska hantera applikationen i Docker. Det ska finnas funktionalitet för att enkelt komma igång att använda det projekt som  du utvecklar.

Ditt repo ska ha en README.md som steg-för-steg beskriver hur man kommer igång med applikationen, och hur man använder applikationen.

### Databas

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

### Design minimum
- Low fidelity designskiss
- Mobile first
- Vyer för mobil och skärm

  
### Design Extra
- Logotyp
- Färgtema

### Code minimum
- En README.md i gitrepot med följande delar:
  - Installation: Vad behövs för att man själv ska kunna köra appen?
  - Screenshots: minst en screenshot (eller gif) som visar appen under använding
- En användare ska kunna registrera ett konto
- En användare ska kunna logga in och logga ut
- Inloggad användare ska kunna lägga till verksamheter
- Verksamheter ska kunna redigeras och raderas av den användare som skapat resursen
- Alla verksamheter ska finnas listade den som besöker applikationen
- Alla formulärsfält som registeras till databasen ska valideras (att rätt och rimlig typ att data lagras)

## Utmaningar

Här finns exempel på utmaningar som du kan anta, Vi uppmuntrar dig till att anta utmaningar så att projketet kan bli en del av en kommande portfolio.

- Publicera applikationen via Linode eller motsvarade
- Skapa fler fält, tabeller
- Ladda upp bilder i applikationen så att du dynamiskt kan ange url till en bild
- Det ska vara möjligt att sätta en verskamhet som draft (ej publicerad - visas endast för användare som skapat resursen)
- Det ska vara möligt att sätta betyg (1-5 stjärnor) på verksamheter
- Det ska vara möjligt att lägga till en kommenter för en verksamhet
- Det ska vara möjligt att lägga till och redigera kategorier via formulär
- Använd PHP klasser för att omsätta resurser till modeller
- Använd Frontend (JavaScript) för att kommunicera med backend
- ...
***

### Redovisning - applikation under utveckling 
Tisdag 14 maj visar du upp ditt pågående arbete med case. Dela erfarenhetet, visa upp utvalda delar från din applikation och ditt pågående projekt.


### Inlämning och redovisning
Redovisning av caset är den måndagen den 27 maj kl 10.30 

Vi vill att alla får ta del av varandras redovisning. Det innebär att ni behöver förbereda er på att redovisningen är kort - ca 5 minuter per person. Då visar ni (demonstrerar) er applikation genom att dela skärm.

*Förbered 5 minuters redovisning enligt följande mall:*

#### I reovisningen ska du:
- demonstrera applikationen
- - visa hur man lägger till, markerar och tar bort olika resurser
- - visa exempel på annan funktionalitet (ex ngn av utmaningarna)
- berätta vad du är mest nöjd med (design, kod, struktur...)
- berätta vad du skulle vilja att applikationen kan göra, men inte hunnit att koda

Redovisningen sker i bokstavordning (efternamn a-ö)

### Handledning
Det kommer givetvis finnas möjlighet till handledning fram tills den 27 maj. I första hand är det under vanlig lektionstid.

Lycka till!

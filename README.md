# Simpele PGP Messenger

Volledig offline • Wachtwoord-gebaseerd • Echte OpenPGP (AES-256 + Argon2)

Live demo: [https://matje1984.github.io/pgp-messenger/](https://matje1984.github.io/pgp-messenger/)

---

## Nederlands

### Wat is dit?

Een eenvoudige, volledig offline web-app waarmee je tekst kunt versleutelen en ontsleutelen met een gedeeld wachtwoord.  
Alles gebeurt **alleen op jouw apparaat**. Er gaat geen data naar een server. De app werkt op iOS, Android (Samsung e.d.), Windows, Mac en Linux.

De versleuteling is echte OpenPGP met:
- AES-256
- Argon2 (sterke, memory-hard wachtwoordafleiding)
- AEAD (authenticated encryption)

### Belangrijke veiligheidsregels

1. **Gebruik altijd een lang en sterk wachtwoord**  
   Minimaal 12–16 tekens, met:
   - Hoofdletters
   - Kleine letters
   - Cijfers
   - Leestekens (bijv. `!@#$%^&*`)

2. **Deel het wachtwoord NOOIT via hetzelfde kanaal als de versleutelde tekst**  
   Stuur het wachtwoord persoonlijk (mondeling, apart beveiligd kanaal, briefje of andere messenger).  
   Als iemand zowel de versleutelde tekst als het wachtwoord onderschept, is de beveiliging weg.

3. **Gebruik een uniek wachtwoord per gesprekspartner**  
   Hergebruik niet hetzelfde wachtwoord voor meerdere mensen.

4. **De app is offline-first**  
   Zodra de pagina is geladen, kun je internet uitzetten. Alles werkt dan nog steeds.

5. **Vertrouw de bron**  
   Open de app bij voorkeur via de officiële GitHub Pages link of host hem zelf. Controleer de code als je twijfelt.

### Stap-voor-stap: Bericht versleutelen en versturen

1. Open de app: [https://matje1984.github.io/pgp-messenger/](https://matje1984.github.io/pgp-messenger/)
2. Zorg dat je op het tabblad **Versleutelen** zit.
3. Vul een **sterk wachtwoord** in (zie regels hierboven).
4. Typ of plak het bericht dat je wilt versleutelen.
5. Klik op **Versleutelen**.  
   Dit kan even duren omdat Argon2 zwaar is (dat is juist de bedoeling).
6. Kopieer de versleutelde PGP-tekst (knop **Kopieer**).
7. Stuur deze tekst via een willekeurige messenger (WhatsApp, Telegram, Signal, e-mail, sms, etc.).
8. Geef het wachtwoord **apart** door aan de ontvanger (niet via dezelfde chat).

### Stap-voor-stap: Bericht ontvangen en ontsleutelen

1. Open dezelfde app op je telefoon of computer.
2. Ga naar het tabblad **Ontsleutelen**.
3. Plak de ontvangen versleutelde PGP-tekst.
4. Vul het **zelfde wachtwoord** in dat je persoonlijk hebt gekregen van de verzender.
5. Klik op **Ontsleutelen**.
6. Het originele bericht verschijnt.

Het werkt precies hetzelfde de andere kant op.

### Offline gebruiken

- Open de pagina één keer terwijl je internet hebt.
- Voeg de pagina toe aan je startscherm (op telefoon) of bookmark hem.
- Daarna kun je internet uitzetten. De app blijft werken omdat OpenPGP.js lokaal is opgeslagen.

### Technische details

- OpenPGP.js v6.3.1 (lokale kopie)
- Symmetric encryption met wachtwoord (geen publieke/private sleutels nodig)
- Configuratie: AES-256 + Argon2 + AEAD (GCM)
- Content Security Policy aangescherpt (geen externe scripts)
- Geen tracking, geen cookies, geen server

---

## English

### What is this?

A simple, fully offline web app that lets you encrypt and decrypt text using a shared password.  
Everything happens **only on your device**. No data is sent to any server. The app works on iOS, Android (Samsung etc.), Windows, Mac and Linux.

The encryption is real OpenPGP with:
- AES-256
- Argon2 (strong, memory-hard password derivation)
- AEAD (authenticated encryption)

### Important security rules

1. **Always use a long and strong password**  
   At least 12–16 characters, containing:
   - Uppercase letters
   - Lowercase letters
   - Numbers
   - Special characters (e.g. `!@#$%^&*`)

2. **NEVER share the password through the same channel as the encrypted text**  
   Give the password in person (verbally, separate secure channel, note, or different messenger).  
   If someone intercepts both the encrypted text and the password, the protection is gone.

3. **Use a unique password per conversation partner**  
   Do not reuse the same password for different people.

4. **The app is offline-first**  
   Once the page is loaded, you can turn off the internet. Everything still works.

5. **Trust the source**  
   Preferably open the app via the official GitHub Pages link or host it yourself. Check the code if you have any doubts.

### Step-by-step: Encrypt and send a message

1. Open the app: [https://matje1984.github.io/pgp-messenger/](https://matje1984.github.io/pgp-messenger/)
2. Make sure you are on the **Encrypt** tab.
3. Enter a **strong password** (see rules above).
4. Type or paste the message you want to encrypt.
5. Click **Encrypt**.  
   This may take a moment because Argon2 is deliberately heavy.
6. Copy the encrypted PGP text (button **Copy**).
7. Send this text via any messenger (WhatsApp, Telegram, Signal, email, SMS, etc.).
8. Give the password to the recipient **separately** (not in the same chat).

### Step-by-step: Receive and decrypt a message

1. Open the same app on your phone or computer.
2. Go to the **Decrypt** tab.
3. Paste the received encrypted PGP text.
4. Enter the **same password** that you received personally from the sender.
5. Click **Decrypt**.
6. The original message appears.

It works exactly the same the other way around.

### Using it offline

- Open the page once while you have internet.
- Add the page to your home screen (on mobile) or bookmark it.
- After that you can turn off the internet. The app continues to work because OpenPGP.js is stored locally.

### Technical details

- OpenPGP.js v6.3.1 (local copy)
- Symmetric encryption with password (no public/private keys needed)
- Configuration: AES-256 + Argon2 + AEAD (GCM)
- Strict Content Security Policy (no external scripts)
- No tracking, no cookies, no server

---

## License

This project uses [OpenPGP.js](https://openpgpjs.org) (LGPL-3.0).  
The rest of the code is free to use and modify.

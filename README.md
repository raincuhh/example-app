
# Veiledning for opprettelsen av Vite boilerplate prosjekt, og deployment til Nett gjennom Vercel.

## Forutsetninger

Før du begynner med denne guiden, så sørg for at du har følgende verktøy installert på datamaskinen din.

- **Git**: [https://git-scm.com/downloads/win](https://git-scm.com/downloads/win) - et versjonskontrollsystem, som lar deg holde styr på endringer i kodebasen din og samarbeide med andre utviklere eller medelever, gjennom å lage en Git Repo, som har koden din i.
- **Github konto**: [https://github.com](https://github.com) - en plattform for versjonskontroll, som lar deg lagre din Git Repo i clouden/github servere.
- **Node.js og npm**: [https://nodejs.org/en](https://nodejs.org/en) - noe som lar deg kjøre Javascript utenfor nettleseren og bruke npm (Node Package Manager) til å håndtere avhengigheter i prosjektet ditt.

## Steg 1. Opprettingen av et Vite Boilerplate prosjekt.

### Installer Vite

Åpne terminalen på datamaskinen og kjør følgende kommando for å opprette et nytt Vite-prosjekt med JavaScript.

(Jeg anbefaler å lage en mappe spesielt for Git Repos, jeg har min spesifikt i `C:\Dev\Repos\`)

```bash
npm create vite@latest navn-på-prosjekt --template vanilla
```

Følg trinnene for hva koden sier etter å ha skrevet kommandoen, (ved å velge rammeverk: Vanilla, og velge en variant, enten typescript eller JavaScript (vi velger JavaScript)).

### Naviger til prosjektmappen

Etter at prosjektet har opprettet, gå til prosjektmappen.

### Installer avhengigheter (dependencies)

Etter at du er inni prosjektmappen, så må du installere avhengighetene som prosjektet trenger for å fungere.

```bash
npm install
```

## Steg 2. Kjør en utviklingsserver.

### Start utviklingsserveren

Kjør følgende kommando for å starte utviklingsserveren:

```bash
npm run dev
```

Etter å ha kjørt kommandoen `npm run dev`, gå til nettleseren din og skriv inn koblingen du ser `Local:` vises.

PS: hvis du får en feil i nettleseren, kan du også bare CTRL + venstreklikk på lenken du ser i lokal for å åpne opp siden.

Når du går inn på siden, vil du se en standardplate som dere bare kan slette hvis dere åpner mappen i Visual Studio Code eller en hvilken som helst koderedigerer.

## Steg 3. Opprett en github repository.

### Lag en ny Repository på GitHub

Gå på [github.com](https://github.com), og hvis du ikke er logget inn, logg inn. og i dashbordet ditt, bør du se en knapp som heter "new" eller “ny”, trykk på den.

Generelt, bare følg trinnene i skjemaet, fyll ut depotnavn, beskrivelse er valgfri, gjør den offentlig eller privat, spiller ingen rolle. prøv å holde navnet det samme som navnet på mappen til prosjektet ditt. for eksempel mitt-vite-prosjekt, og gjør det samme i skjemaet.

Så er det bare å trykke "create repository".

### Lag en Git Repo

I terminalen, initialiser Git i prosjektmappen:

Hvis vite fortsatt kjører, trykk (CTRL + c) for å avslutte serveren.

```bash
git init
```

Legg til prosjektfilene i Git Repoen.

```bash
git add .
```

Commit filene til git repoen.

```bash
git commit -m "Initial commit"
```

### Koble git og Github Reposene

Koble din lokal Git Repo til den remote Github Repoen:

Kopier denne lenken fra GitHub:

```bash
git remote add origin <GitHub-repository-URL>
```

Push filene til GitHub.

```bash
git push -u origin master
```

Etter alt dette, oppdater GitHub-repository-siden din, og du bør se filene dine der.

## Steg 4. Deploy til Vercel.

### Logg inn i Vercel

Gå til [vercel.com/new](https://vercel.com/new), og logg inn med GitHub-kontoen din. Trykk på "Continue with GitHub".

Etter pålogging vil du se GitHub-repositoriene dine. Velg viteprosjektet ditt og trykk på "Import".

Klikk deretter på “Deploy”. (Du trenger ikke å endre noe)

Venter litt mens prosjektet blir bygget for produksjon og internett. Når det er ferdig distribuert, kan du klikke på vinduet som vises.

Du vil se at prosjektet ditt er på internett. Du kan sende lenken til vennene dine, eller hvem du egentlig vil. 

For eksempel:

```
https://mitt-vite-prosjekt.vercel.app
```

Navnet vil kanskje endre seg litt hvis andre brukere bruker spesifikt ditt prosjekt navn til å hoste sine prosjekter.

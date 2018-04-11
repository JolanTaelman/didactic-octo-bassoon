# Opstart

## TODOs

- [ ] Installeer de nodige software (zie verder)
- [ ] Kloon deze repository (`git clone`)
- [ ] Vul je naam en contactinfo aan in het README-bestand
- [ ] Pas de naam aan van het LaTeX document voor het artikel aan in "familienaam-voornaam.tex".
- [ ] Nog niet vertrouwd met het gebruik van Git? Kijk verder in dit document

## Werken met Git

De meesten werken wellicht met een grafische tool als SourceTree of Github Desktop, maar de command-line tool is eigenlijk heel goed en geeft ook telkens aan wat de volgende stap is en hoe je een stap kan ongedaan maken. De foutboodschappen (als je ze goed leest) geven ook meestal een goed idee van wat er is misgegaan en hoe je dit kan oplossen.

Probeer Git zo snel mogelijk onder de knie te krijgen en te begrijpen, je zal dit toch voortdurend nodig hebben... Commit regelmatig (meerdere keren per werksessie). Geef een goede beschrijving van wijzigingen die je gecommit hebt (je toekomstige zelf zal je dankbaar zijn).

### Configuratie Git

Bij installatie van [Git voor Windows](https://git-scm.com/download/), zorg er voor dat ook Git Bash geïnstalleerd wordt. Om synchronisatie met Github te vereenvoudigen, is het best om een [SSH-sleutelpaar](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/) aan te maken. Wanneer gevraagd wordt om een "passphrase" in te voeren, mag je die leeg laten. Volg de instructies van Github om je [SSH-sleutel te registreren](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/).

Start een console en voer volgende stappen uit voor de basisconfiguratie van Git. Gebruik het emailadres dat gekoppeld is aan je Github-account.

```
$ git config --global user.name "VOORNAAM NAAM"
$ git config --global user.email "VOORNAAM.NAAM@EXAMPLE.COM"
$ git config --global push.default simple
```

### Opstart project

Maak lokaal een kopie (kloon) van de Github repository.

1. Ga naar de repository op Github (`ozt-tile-USERNAAM`), klik rechts op de groene knop "Clone or Download". zorg dat "Use SSH" geselecteerd is. Kopieer de URL (begint met `git@github.com:HoGentTIN`)
2. Open Git Bash in een directory waar je de lokale repository wil bijhouden
3. `git clone git@github.com:HoGentTIN/ozt-tile-USERNAAM.git`

Je kan de naam van de lokale directory wijzigen in wat je zelf wil, of die verplaatsen.

### Workflow

Om wijzigingen bij te houden ga je als volgt te werk.

0. Doe steeds `git pull` voor je begint te werken. Dit is vooral belangrijk als je op meerdere machines werkt, of als je af en toe iets rechtstreeks op GitHub.com commit.
1. Maak wijzigingen in bestanden, voeg nieuwe bestanden toe, enz.
2. Gebruik het commando `git add FILE...` om bestanden klaar te zetten om te committen. `FILE...` vervang je dan door de namen van de bestanden die je wil committen. Als je *alle* lokale wijzigingen ineens wil committen gebruik je `git add .` (de punt betekent de huidige directory en alle onderliggende).
3. Met `git commit -m "Commit-boodschap"` registreer je een nieuwe revisie in het versiebeheersysteem. Vul een betekenisvolle commit-boodschap in die beschrijft wat je gewijzigd hebt.
4. Met `git push` kan je tenslotte al je lokale wijzigingen naar Github publiceren.

# IT Operations Flow Game

## Første regelsæt – version 0.1

## Formål

Spillet skal vise, hvordan IT Operations-systemer producerer arbejde, rework, forsinkelser, misforståelser og tab af tillid.

Spillet har ikke et perfekt facit.

Formålet er ikke, at alle opgaver skal løses.
Formålet er at vise, hvordan lokale rationelle valg kan skabe systemisk belastning.

Deltagerne skal opleve:

* begrænset kapacitet
* prioritering under usikkerhed
* rework
* afhængigheder mellem teams
* forsinket information
* lokale mål kontra samlet reliability
* Service Desk som organisationens oplevelse af IT
* konsekvensen af manglende kommunikation

---

# 1. Roller

Spillet har tre tekniske teams og ét konsekvenslag.

## Team 1 – Network / DHCP

Ansvar:

* netværksadgang
* VLAN
* DHCP scopes
* IP-konflikter
* routing/firewall-afhængigheder
* klientplacering

## Team 2 – IAM / DNS

Ansvar:

* Active Directory
* DNS
* login/autentificering
* AD Sites and Services
* identitet
* navneopslag

## Team 3 – Server / Storage / Backup

Ansvar:

* servere
* VMware/hypervisor
* storage
* backup
* server performance
* platformstabilitet

## Service Desk

Service Desk løser ikke root cause.

Service Desk viser, hvordan organisationen oplever IT.

Service Desk-tavlen viser efter hver runde:

* antal opkald
* antal tickets
* gentagne incidents
* bruger-/forretningstillid
* business impact
* kommunikationskvalitet

---

# 2. Kapacitet

Hvert teknisk team har som udgangspunkt:

## 5 kapacitetspoint pr. runde

Kapacitet bruges på:

* normale opgaver
* incidents
* fejlsøgning
* root cause-analyse
* kommunikation
* koordinering
* dokumentation
* forbedringer

Kapacitet kan ikke gemmes til næste runde.

Hvis et team ikke bruger hele sin kapacitet, er den tabt.

Hvis et team får mere arbejde end kapacitet, bliver resten til backlog.

---

# 3. Arbejdstyper

Der findes fire hovedtyper arbejde.

## New Work

Nye opgaver, der kommer ind i runden.

Eksempler:

* ny server
* brugerproblem
* alarm
* change request
* backup warning
* DHCP warning
* DNS latency

## Backlog

Arbejde fra tidligere runder, som ikke blev færdigt.

Backlog overføres til næste runde.

## Rework

Arbejde skabt af tidligere valg.

Eksempler:

* alarm lukket uden årsag
* løsning lavet uden fælles forståelse
* opgave udført på forældet information
* eskalering uden ejerskab

## Invalidated Work

Arbejde der viser sig ikke længere at være relevant.

Eksempler:

* andet team har allerede løst problemet
* opgaven er udskudt
* krav er ændret
* dependency findes ikke længere
* problemet var et symptom fra et andet team

Invalidated Work bruger stadig kapacitet.

Det er vigtigt:
Teamet handlede rationelt ud fra den information, de havde.

---

# 4. Grundformel

Hver runde beregnes arbejdet sådan:

## Total Work = New Work + Backlog + Rework

Hvis Total Work er større end teamets kapacitet, flyttes resten til næste runde som Backlog.

Eksempel:

* Capacity: 5
* New Work: 4
* Backlog: 3
* Rework: 1

Total Work = 8

Teamet kan kun udføre 5.
3 opgaver flyttes til næste runde.

---

# 5. Fælles systemmålinger

Spillet har fælles systemmålinger, som påvirkes af alle teams.

## Reliability

Viser systemets samlede sundhed.

Starter på 5.

Falder ved:

* gentagne incidents
* unresolved root cause
* stigende rework
* dårlig kommunikation
* høj backlog

Stiger ved:

* root cause fjernet
* forbedret information flow
* fælles koordinering
* reduceret rework

## Information Quality

Viser hvor god, aktuel og brugbar informationen er.

Starter på 5.

Falder ved:

* forældede opgaver
* manglende statusopdateringer
* ukendte dependencies
* uafklarede handoffs

Stiger ved:

* fælles statusmøder
* dependency validation
* klare handoffs
* dokumenteret beslutningsgrundlag

## Cross-Team Trust

Viser hvor villige teams er til at dele information og hjælpe hinanden.

Starter på 5.

Falder ved:

* blame
* eskalering uden kontekst
* opgaver der sendes frem og tilbage
* manglende kommunikation

Stiger ved:

* fælles analyse
* tidlig advarsel
* tydelig status
* hjælp på tværs

## Rework Level

Viser hvor meget ekstraarbejde systemet skaber.

Starter på 0.

Stiger ved:

* hurtige lukninger uden læring
* kendte fejl ignoreres
* symptombehandling
* dårlige handoffs
* forældet information

Falder ved:

* root cause
* forbedret monitorering
* dokumentation
* forbedret proces

---

# 6. Service Desk-tavle

Efter hver runde opdaterer facilitator Service Desk-tavlen.

## Service Desk-målinger

| Måling                | Betydning                                 |
| --------------------- | ----------------------------------------- |
| Calls                 | Hvor mange brugere kontakter Service Desk |
| Tickets               | Hvor mange sager oprettes                 |
| Repeat Incidents      | Hvor mange problemer vender tilbage       |
| User Trust            | Hvordan brugerne oplever IT               |
| Business Impact       | Hvor meget organisationen påvirkes        |
| Communication Quality | Hvor godt IT kommunikerer udadtil         |

Service Desk viser forskellen mellem:

* teknisk status
* oplevet status

En ticket kan være lukket i IT, mens brugerne stadig oplever problemet.

---

# 7. Korttyper

Spillet bruger seks korttyper.

## 1. Incident Cards

Beskriver et problem, en alarm eller et driftssignal.

Eksempel:

Slow Login Monday Morning
Repeated DNS Warning
Backup Job Overrun
DHCP Scope Warning
Application Timeout
Storage Latency Alert

## 2. Task Cards

Beskriver almindeligt arbejde.

Eksempel:

Install server
Create firewall request
Clean up monitoring rule
Update documentation
Review backup policy
Patch server

## 3. Action Cards

Beskriver mulige handlinger.

Eksempel:

Close as known noise
Escalate to another team
Investigate pattern
Coordinate with dependency team
Perform root cause analysis
Communicate status to Service Desk
Document finding
Create workaround

## 4. Dependency Cards

Afslører skjulte afhængigheder.

Eksempel:

DNS issue depends on DHCP scope
Login issue depends on AD Site mapping
Application timeout depends on storage latency
Backup delay affects server performance
Network change impacts IAM

## 5. Delay Cards

Forsinker konsekvenser.

Eksempel:

Effect appears in 2 rounds
Users report later
Monitoring signal appears next round
Rework returns after delay
Business escalation occurs later

## 6. Status Update / Perception Cards

Afslører ændret eller manglende information.

Eksempel:

Already resolved by another team
Deferred by dependency team
Requirement changed
Hidden dependency found
Poor communication increases calls
Clear status update reduces noise

---

# 8. Rundeforløb

Hver runde følger samme struktur.

## Step 1 – Nye opgaver

Facilitator giver hvert team nye opgaver.

Opgaver kan være:

* almindelige tasks
* incidents
* alarmer
* dependency requests
* rework fra tidligere runder

## Step 2 – Kapacitet fastlægges

Hvert team har 5 kapacitetspoint.

Eventuelle konsekvenser fra tidligere runder kan reducere kapaciteten.

Eksempel:

Business escalation
Alle teams mister 1 kapacitetspoint pga. koordinationsmøde.

## Step 3 – Teamet prioriterer

Teamet vælger, hvilke opgaver de vil bruge kapacitet på.

De kan ikke nå alt, hvis workload overstiger kapacitet.

## Step 4 – Handling vælges

For incidents/alarmer vælger teamet en handling.

Eksempel:

* luk hurtigt
* eskalér
* undersøg mønster
* koordinér med andet team
* udfør root cause
* kommunikér status

## Step 5 – Facilitator afslører konsekvens

Facilitator trækker eller afslører relevante kort:

* Dependency Card
* Delay Card
* Status Update Card
* Perception Card

## Step 6 – Systemmålinger opdateres

Facilitator justerer:

* Reliability
* Information Quality
* Cross-Team Trust
* Rework Level
* Backlog
* Service Desk-tavle

## Step 7 – Backlog beregnes

Alt arbejde, der ikke blev udført, overføres til næste runde.

## Step 8 – Service Desk opdateres

Service Desk-tavlen vises for alle.

Dette viser organisationens oplevelse af IT efter runden.

---

# 9. Standardhandlinger og konsekvenser

## Close as Known Noise

Cost: 1

Effekt nu:

* opgaven fjernes lokalt

Effekt senere:

* Rework +1 eller +2
* Repeat Incidents +1
* User Trust -1
* Reliability -1 efter forsinkelse

## Escalate to Another Team

Cost: 2

Effekt nu:

* opgaven flyttes

Effekt senere:

* modtagende team får workload +1 eller +2
* Information Quality -1 hvis kontekst mangler
* Cross-Team Trust -1 hvis opgaven sendes uden forklaring

## Investigate Pattern

Cost: 3

Effekt nu:

* opgaven lukkes ikke nødvendigvis
* mindre kapacitet til andre opgaver

Effekt senere:

* Rework -1
* Information Quality +1
* bedre beslutningsgrundlag næste runde

## Coordinate Across Teams

Cost: 2 for hvert deltagende team

Effekt nu:

* mindre kapacitet i flere teams

Effekt senere:

* Information Quality +1
* Cross-Team Trust +1
* risiko for invalidated work reduceres

## Root Cause Analysis

Cost: 5

Effekt nu:

* hele teamets kapacitet bruges
* andre opgaver bliver backlog

Effekt senere:

* recurring incident fjernes
* Rework -2
* Reliability +1
* men backlog kan vokse på kort sigt

Vigtig pointe:

Root cause kan stadig drukne teamet, hvis systemet ikke beskytter kapacitet til forbedring.

## Communicate Status to Service Desk

Cost: 1

Effekt nu:

* mindre kapacitet til teknisk arbejde

Effekt senere:

* Calls -1 eller -2
* User Trust +1
* Communication Quality +1
* færre duplicate tickets

## Document Finding

Cost: 2

Effekt nu:

* mindre kapacitet

Effekt senere:

* Knowledge Debt -1
* Rework -1
* fremtidige lignende opgaver koster 1 mindre

## Create Workaround

Cost: 2

Effekt nu:

* impact reduceres hurtigt

Effekt senere:

* Technical Debt +1
* Rework +1 hvis workaround ikke følges op
* Reliability ændres ikke nødvendigvis

---

# 10. Tværgående konsekvenser

Handlinger i ét team kan påvirke andre teams.

Eksempel:

Network/DHCP lukker DHCP warning som kendt støj.

Næste runde:

* IAM/DNS får login incident +2 workload
* Service Desk Calls +2
* User Trust -1

Eksempel:

Server/Storage udskyder storage latency review.

Næste runde:

* IAM/DNS får authentication timeout
* Application tickets stiger
* Service Desk Business Impact +1

Eksempel:

IAM/DNS ændrer DNS uden kommunikation.

Næste runde:

* Network/DHCP får klientplacering-relaterede incidents
* Server/Storage får service timeout alerts
* Information Quality -1

---

# 11. Nulstilling og invalidated work

Nogle opgaver kan blive nulstillet.

Dette sker når:

* et andet team allerede har løst opgaven
* dependency er udskudt
* krav er ændret
* problemet er forsvundet
* informationen var forældet

Hvis teamet allerede har brugt kapacitet på opgaven, tæller arbejdet som spildt kapacitet.

Effekt:

* Information Quality -1
* Cross-Team Trust -1
* teamet mister den brugte kapacitet
* opgaven giver ingen forbedring

Læringspunkt:

Prioritering uden aktuel information skaber spild, selv når teamet træffer rationelle valg.

---

# 12. Kommunikation

I første gennemspilning bør kommunikation være begrænset.

Eksempelregler:

* teams må kun kommunikere via handoff cards
* teams må kun tale sammen 1 minut pr. runde
* Service Desk får kun information, hvis et team bruger kapacitet på status
* dependencies er ikke synlige, før facilitator afslører dem

Efter teoridelen kan anden gennemspilning ændre reglerne:

* teams må lave fælles status før prioritering
* Service Desk må dele brugerdata
* dependency validation bliver tilladt
* hvert team kan reservere 1 point til forbedring
* fælles system-review hver anden runde

---

# 13. Første gennemspilning

Første gennemspilning skal vise det normale problem.

Regler:

* hvert team har 5 kapacitetspoint
* teams måles lokalt
* kommunikation er begrænset
* root cause koster fuld kapacitet
* ingen reserveret forbedringskapacitet
* Service Desk opdaterer tavlen efter hver runde
* facilitator afslører forsinkede konsekvenser

Forventet resultat:

* backlog vokser
* rework stiger
* Service Desk-belastning stiger
* teams prioriterer lokalt
* nogle opgaver viser sig at være spildte
* root cause bliver svært at vælge
* teamene oplever frustration

---

# 14. Refleksion efter første gennemspilning

Facilitator spørger:

* Hvornår begyndte systemet at blive presset?
* Hvilke valg virkede rationelle i øjeblikket?
* Hvilke valg skabte rework senere?
* Hvilke konsekvenser ramte et andet team end det team, der tog beslutningen?
* Hvor manglede I information?
* Hvad blev aldrig prioriteret?
* Hvad skete der med Service Desk?
* Hvad skete der med brugerens oplevelse af IT?
* Hvor så I local optimization?
* Hvor så I hidden dependencies?
* Hvor så I delay?
* Hvor så I mangel på læringskapacitet?

---

# 15. Teorikobling

Efter første gennemspilning kobles oplevelsen til teori.

## Deming

Systemet producerer resultatet.
Målesystemer påvirker adfærd.
Uden læring gentager systemet sine mønstre.

## Goldratt

Der er altid en constraint.
Når én constraint løses, flytter den sig.
Lokal optimering skaber ikke nødvendigvis samlet forbedring.

## Peter Senge

Feedback loops, delays og mental models former adfærd.
Information flow er en systemegenskab.

## Amy Edmondson

Hvis det ikke er sikkert at sige “jeg ved det ikke”, skjules usikkerhed.
Mangel på psykologisk tryghed skaber knowledge bottlenecks.

## Sidney Dekker

Folk gør det, der giver mening lokalt.
Fejl og rework er ofte symptomer på systemets design.

## Gene Kim

Flow, feedback og læring er nødvendige for stabil IT.
Hvis feedback ikke omsættes til læring, bliver arbejdet reaktivt.

---

# 16. Anden gennemspilning

Anden gennemspilning bruger samme type opgaver, men ændrede systemregler.

Mulige ændringer:

* 1 kapacitetspoint reserveres til forbedring
* fælles system-review hver anden runde
* teams må dele status før prioritering
* Service Desk må dele brugerdata
* dependency validation kan købes for 1 point
* root cause kan deles mellem teams
* statuskommunikation reducerer Service Desk-load
* fælles reliability-mål indføres

Formål:

Ikke at løse alt.

Formål:

At vise at samme mennesker får andre resultater, når systemreglerne ændres.

---

# 17. Spillets slutning

Spillet slutter efter 6-8 runder.

Der findes ingen vinder.

I stedet vurderes systemets tilstand.

## Mulige sluttilstande

### Stabil drift

Workload og rework er håndterbart.
Service Desk-load er lavt.
Reliability er stabil.

### Presset drift

Backlog vokser langsomt.
Nogle teams er begyndt at mangle kapacitet.
Service Desk ser stigende gentagelser.

### Reaktiv drift

Teams bruger størstedelen af kapaciteten på rework.
Root cause vælges sjældent.
Service Desk-load er høj.

### Brandkamp

Teams når kun symptomer.
Backlog og rework vokser.
Tillid falder.

### Systemisk nedbrud

Ingen teams har kapacitet til læring.
Service Desk drukner i gentagne sager.
Organisationen oplever IT som ustabilt.

---

# 18. Centrale læringspointer

Spillet skal vise:

* IT-teams fejler ikke nødvendigvis, fordi de vælger forkert.
* De vælger ofte rationelt ud fra det system, de er placeret i.
* Hurtige løsninger kan skabe rework.
* Root cause kræver kapacitet.
* Hvis forbedringskapacitet ikke beskyttes, vinder daglig drift.
* Lokal optimering kan skabe arbejde for andre teams.
* Service Desk ser konsekvenser før de tekniske teams gør.
* Kommunikation er ikke overhead.
* Information quality påvirker prioritering.
* Backlog er ikke bare manglende produktivitet.
* Rework er systemets gæld.
* Reliability er en systemegenskab, ikke en lokal teamopgave.

---

# 19. Første prototype

Første prototype bør være lille.

Anbefalet minimum:

* 3 teams
* 1 Service Desk-tavle
* 6 runder
* 12 Incident Cards
* 12 Task Cards
* 12 Status/Perception Cards
* 9 Dependency Cards
* 6 Delay Cards
* 5 systemmålinger

Målet med første prototype er ikke perfektion.

Målet er at teste, om deltagerne mærker:

* kapacitetsmangel
* rework
* frustration
* forsinket information
* lokal optimering
* Service Desk-effekt

---

# 20. Arbejdstitel

Mulige navne:

## IT Operations Flow Game

## The Reliability Flow Game

## Operations Rework Simulation

## The Hidden Work Game

## Flow, Feedback and Rework

## IT Operations Systems Simulation

Foreløbig anbefaling:

# The IT Operations Flow Game

Undertitel:

A systems thinking simulation for IT Operations teams.


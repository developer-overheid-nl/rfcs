---
title: "RFC-0000: Het RFC-proces"
short_title: RFC-proces
status: Draft
implementation: Partially implemented
date: '2026-10-07'
authors:
  - Anne Schuth
---

## Behandeling

Dit document beschrijft hoe voorstellen in deze repository worden ingediend, besproken en vastgesteld. Het geldt voor zichzelf: wijzigingen aan dit proces gaan als pull request, langs dezelfde weg als elk ander voorstel.

Reacties op dit document kunnen tot 30 november 2026, via een issue of een pull request.

## Waarvoor een RFC

Een RFC is voor een besluit dat meer dan één repository raakt, dat moeilijk terug te draaien is, of waarover anderen iets te zeggen hebben voordat het vastligt. Denk aan een afspraak tussen organisaties, een formaat waar anderen op gaan bouwen, of het beleggen van een voorziening.

Een RFC is niet nodig voor een wijziging binnen één repository die het team zelf kan overzien. Dat is een gewone pull request. Bij twijfel: schrijf de pull request en kijk of de discussie over de code gaat of over de afspraak. Gaat zij over de afspraak, dan wordt het een RFC.

## De route

**Schrijven.** Kopieer `0000-template.md` naar `text/0000-korte-naam.md` en vul hem in. Het nummer blijft `0000` tot de pull request openstaat.

**Indienen.** Open een pull request. Het nummer van die pull request wordt het nummer van de RFC: hernoem het bestand van `0000-` naar dat nummer, met voorloopnullen tot vier cijfers. Een RFC die als pull request 12 binnenkomt, wordt `text/0012-korte-naam.md`.

**Bespreken.** De discussie staat in de pull request, bij de regel waar zij over gaat. Wie een punt maakt dat de tekst raakt, krijgt antwoord in de tekst of in de pull request, niet alleen in een gesprek ernaast. De auteur werkt de RFC bij tijdens de behandeling; de geschiedenis van die wijzigingen is de verantwoording.

**Reactietermijn.** Elke RFC noemt in zijn eigen Behandeling-sectie tot wanneer er gereageerd kan worden, met een minimum van vier weken. Wie niet reageert, stemt nergens mee in; de RFC wordt vastgesteld met de reacties die er dan liggen.

**Vaststellen.** De beheerders van developer.overheid.nl stellen vast en leggen bij het samenvoegen vast wat er met elke reactie is gedaan. Een RFC die meer vraagt dan het portaal zelf kan waarmaken, zoals financiering of een wettelijke grondslag, noemt dat als open besluit en wordt vastgesteld met die besluiten open.

**Daarna.** Samenvoegen betekent dat de afspraak geldt voor wat erin staat, niet dat er gebouwd is. Elke RFC houdt daarom twee velden bij: `status` en `implementation`.

## Statuswaarden

| status | Betekenis |
| --- | --- |
| Draft | in bewerking, nog niet ingediend of nog in behandeling |
| Proposed | ingediend, reactietermijn loopt |
| Accepted | vastgesteld; de afspraak geldt |
| Rejected | niet vastgesteld; de tekst blijft staan met de reden |
| Superseded | vervangen door een latere RFC, die erbij genoemd wordt |

| implementation | Betekenis |
| --- | --- |
| Not implemented | er is nog niets gebouwd |
| Partially implemented | een deel draait |
| Implemented | het staat er zoals beschreven |

Een afgewezen RFC wordt niet verwijderd. De overweging is het product, ook wanneer het antwoord nee is.

## Vorm

Elke RFC is één markdownbestand in `text/`, met frontmatter die `title`, `status`, `implementation`, `date` en `authors` bevat. Wie op een eerdere RFC voortbouwt, noemt die in `depends_on`.

Verder gelden drie dingen. De tekst is Nederlands. Een RFC noemt wat hij niet regelt, want dat is wat een lezer als eerste zoekt. En een RFC die een alternatief verwerpt, schrijft op waarom, zodat die afweging niet opnieuw hoeft.

## Wie beslist

De beheerders van developer.overheid.nl. Dat is een lichte procedure, passend bij een proces dat niemand iets oplegt: een RFC bindt het portaal zelf en is richtinggevend voor anderen.

Groeit dit uit tot afspraken waar organisaties op leunen, dan is dit niet het juiste gremium meer en hoort vaststelling naar een bestuurlijk verband te verhuizen. Dat besluit hoort bij de eerste RFC die het nodig heeft, niet hier.

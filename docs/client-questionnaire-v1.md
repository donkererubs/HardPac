# Kick-off vragenlijst — ITL B.V. × HardPac

Versie 1.0 · datum: 2026-09-03 · status: concept ter review (Ruben)
Doel: ontdekfase voor de opvolger van de huidige (Softpak-)software.
Verwant: zie `softpac-discovery.md` voor de achterliggende onderzoeksnotities.

---

## Waarom deze vragenlijst?

ITL wil verkennen hoe de huidige logistieke software vervangen kan worden door
**eigen, moderne software die precies op ITL is toegesneden** — in plaats van
een generiek pakket waar ITL zich aan moet aanpassen. Er is nog **niets
besloten**; dit is geen technisch document, maar een gespreksstarter.

**Zo gebruiken:** antwoorden mogen schattingen zijn. Wat niet van toepassing
is, sla je over. Invullen duurt ± 30–45 min, of we lopen het samen door in een
gesprek van ± 60–90 min. Alles wordt vertrouwelijk behandeld.

---

## A. Bedrijf & mensen

- [ ] A1. Hoeveel mensen werken er dagelijks in de systemen, per groep: operatie/planning, verkoop/offertes, administratie/financiën, directie?
- [ ] A2. Zijn er meerdere vestigingen/locaties die met dezelfde systemen werken?
- [ ] A3. Is dit een ITL-vraagstuk, of moet de oplossing ook elders in de groep (Euro-Rijn / ER Logistics) kunnen draaien?

## B. Huidige softwarelandschap

- [ ] B1. Welke Softpak-producten gebruikt ITL vandaag? (ProFor/expeditie · CDS/douane · ProStore/WMS · anders) — sinds wanneer en hoeveel gebruikers tegelijk?
- [ ] B2. Waar draait dat (eigen server, door Softpak gehost, per kantoor)?
- [ ] B3. Wat kost het jaarlijks (licenties, support, updates)? Een indicatie is genoeg.
- [ ] B4. Welke andere software is er nog in gebruik: boekhoudpakket, Transporeon, Portbase/NxtPort, Eurorijn-app, Office/Excel-maatwerk, klantportalen?
- [ ] B5. Hoe verloopt de support van Softpak vandaag — wie is het aanspreekpunt en hoe snel/soepel gaat dat?

## C. Dagelijkse kernprocessen — volg één zending

*Doel: begrijpen hoe een zending van aanvraag tot factuur loopt en waar tijd
en geld blijven zitten. Neem één typische zending als voorbeeld (bijv. een
containertransport Rotterdam → Duitsland).*

- [ ] C1. **Offerte:** wie maakt offertes en op basis waarvan (tarieflijsten, inkoopprijzen per vervoerder)? Hoe snel is een offerte er?
- [ ] C2. **Order binnenkomst:** hoe komt een opdracht binnen (e-mail, telefoon, EDI, portaal)? Wordt er handmatig overgetypt?
- [ ] C3. **Planning:** wie plant welke ritten? Gebeurt dat in een overzicht/planningbord? Hoe krijgen chauffeurs hun opdracht (app, papier, telefoon)?
- [ ] C4. **Uitvoering & POD:** hoe wordt bewijs van levering vastgelegd (handtekening, CMR, foto's)? Wat gebeurt er daarna mee (naar klant, archief, factuur)?
- [ ] C5. **Facturatie:** hoe ontstaat een factuur (per zending, verzamelnota, nacalculatie)? Wie controleert? PDF of digitaal (UBL/Peppol)? Hoe zit het met inkoopfacturen en doorbelasting?
- [ ] C6. **Rapportage:** welke overzichten gebruikt ITL nu (omzet/marge per klant of route, volumes)? Uit welk systeem komen die?
- [ ] C7. Wat is in dit hele proces het meest handmatige, trage of foutgevoelige?

## D. Pijnpunten & aanleiding — "waarom nu"

- [ ] D1. Wat zijn de top-3 frustraties met de huidige software? *Graag concreet: "voor elke nieuwe wens moet Softpak … en dat duurt …"*
- [ ] D2. Waar remt de software de groei of de kwaliteit van de dienstverlening?
- [ ] D3. Wat kost de huidige situatie naar schatting (licenties + maatwerk + eigen uren + fouten)?
- [ ] D4. Zijn er eerder pogingen geweest om te veranderen? Wat gebeurde er?
- [ ] D5. Wat moet nieuwe software écht anders doen dan Softpak? (top 5)

## E. Data & koppelingen

- [ ] E1. Waar ligt de historie (database, mappen, papier)? Hoe ver terug, en moet die meeverhuizen of mag die gearchiveerd blijven?
- [ ] E2. Hoeveel actieve klanten/opdrachtgevers en vaste vervoerders/partners?
- [ ] E3. Hoe worden tarieven bijgehouden (inkoop per vervoerder, verkoop per klant, per route)?
- [ ] E4. Welke koppelingen zijn er vandaag: EDI/XML met klanten of vervoerders, boekhoudpakket, Transporeon, Portbase/NxtPort, GPS/telemetrie?
- [ ] E5. Welke documenttypen spelen (CMR, offertes, facturen, douanestukken, klantdocumenten) en waar worden die bewaard?

## F. Ambities — pariteit vs. droom

- [ ] F1. **Pariteit:** wat moet op dag 1 gewoon kunnen, niet slechter dan nu?
- [ ] F2. **Droom:** als alles kon, wat zou ITL dan willen? (klantportaal met track & trace, automatische documenten, chauffeurs-app, dashboards, …)
- [ ] F3. Wat heeft ITL nu *niet*, maar zou het willen inzetten om zich te onderscheiden?
- [ ] F4. Hoe ziet succes er over 12 maanden uit — waaraan merk je dat de vervanging is gelukt?

## G. Randvoorwaarden

- [ ] G1. Tijdlijn: wanneer zou ITL willen starten, wanneer live? Harde deadline?
- [ ] G2. Budgetframe (bandbreedte is prima) en wie neemt de beslissing?
- [ ] G3. Wie is het dagelijkse aanspreekpunt voor dit traject — operatie, directie, beiden?
- [ ] G4. Eisen rond privacy/compliance: AVG (klant- en chauffeursdata), bewaarplicht, e-facturatie; specifieke eisen van grote klanten (portalen, audits)?
- [ ] G5. Hoe belangrijk is eigenaarschap: data in eigen beheer, ontsluitbaar via API, geen lock-in bij één leverancier?

## H. Branchespecifiek

- [ ] H1. **Douane:** doet ITL zelf aangiften (in-/uitvoer, NCTS, AES) of via een douane-expediteur? Hoe zwaar weegt douane in het dagelijkse proces?
- [ ] H2. **Lading & markten:** welke ladingsoorten domineren (containers, stukgoed, projectlading, koel/vries, ADR)? Welke landen/routes?
- [ ] H3. **Eurorijn-app:** wie gebruikt die waarvoor — hoort die bij dit traject (vervangen, koppelen, ongemoeid laten)?
- [ ] H4. **Klanten:** hoeveel klanten zouden een portaal met status/POD willen? Vragen klanten nu al om track & trace?
- [ ] H5. Speelt er een magazijncomponent mee (eigen opslag, cross-dock, de-consolidatie)?

---

## Afsluiting

- [ ] Wie doet er mee aan dit traject bij ITL (namen + rollen)?
- [ ] Wat is hét belangrijkste dat we moeten begrijpen vóórdat we iets bouwen?
- [ ] Zijn er mensen bij ITL die we apart moeten spreken (planning, financiën, chauffeurs)?

**Volgende stap:** wij werken dit uit tot een beknopt beeld — huidige situatie,
kansen, en een voorstel voor één eerste werkende workflow (geen techniek, geen
beloftes). Daarna bepalen we samen de aanpak.

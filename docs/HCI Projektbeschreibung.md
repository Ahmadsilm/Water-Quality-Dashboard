## 2. Problemstellung und Motivation

Der Sommer 2026 war in Hessen der heißeste seit Messbeginn 1881, der Juli der trockenste je gemessene (14 l/m², 82 % unter dem Mittel). Bereits das Winterhalbjahr 2025/26 war mit 259 l/m² rund 28 % zu trocken. Ende August lagen 64 % der Grundwassermessstellen im niedrigen oder sehr niedrigen Bereich. Mehrere Kreise und Städte (u. a. Wetteraukreis, Vogelsbergkreis, Werra-Meißner-Kreis, Darmstadt) untersagten die Wasserentnahme aus Gewässern, andere Kommunen schränkten die Gartenbewässerung ein oder blieben bei Appellen.

Für Privatpersonen mit Garten entsteht daraus eine Unsicherheit: Es gibt keine landesweite Regel. Jede untere Wasserbehörde entscheidet per Allgemeinverfügung selbst, sodass sich Betroffene den für ihren Wohnort geltenden Stand selbst zusammensuchen müssen. Die Wasserdaten dahinter veröffentlicht das HLNUG vor allem in Fachberichten (Monatsberichte als PDF) und Messportalen für Fachpersonal. Unsere Annahme: Laien können daraus nicht ableiten, wie ernst die Lage vor Ort ist und was sie für das eigene Gießen bedeutet. Ob dies das zentrale Problem der Zielgruppe ist, prüfen wir im User Research und schärfen es danach nach.

**Zielgruppe:** Privatpersonen mit Garten in Hessen (Hausgarten, Kleingarten).

**Ziel:** Ein Web-Dashboard, das verständlich zeigt, wie die Wasserlage am eigenen Wohnort ist (Grundwasser, Pegel, Niederschlag) und was aktuell gilt. Geplant (vorläufig): Karte und Ortssuche, Ampelstatus, Zeitreihe im Vergleich zum langjährigen Mittel, Hinweise zu Einschränkungen. Der genaue Funktionsumfang ergibt sich aus dem User Research.

## 3. Kleine Recherche

**Datenquellen**

- HLNUG-Datenportal Grundwasser und Pegel (Messwerte; Download-/API-Möglichkeit wird geprüft, bei Bedarf Anfrage beim HLNUG).
- Pegel Online (WSV): REST-API ohne Authentifizierung, v. a. Wasserstand und Abfluss, allerdings nur rund 30 Tage Historie.
- HLNUG Open Data: Grundwassermessstellen (CC BY 4.0, Standorte); DWD Open Data für Niederschlag.
- Fallback: Pseudodatensatz, der sich an den Klassen der HLNUG-Monatsberichte orientiert (sehr niedrig bis sehr hoch); die Verwendung wird offengelegt.

**Bestehende Angebote**

- HLNUG-Monatsberichte: aktuell und fundiert, aber PDF mit Fachbegriffen, kaum interaktiv.
- HLNUG-Pegelseiten und App „Meine Pegel“: Fokus Hochwasser und Fachpublikum.
- „Grundwasserstandonline“ (Niedersachsen): zeigt Machbarkeit einer klassifizierten Grundwasserkarte für die Öffentlichkeit; für Hessen haben wir kein vergleichbares öffentliches Angebot gefunden.
- Drittanbieter-Übersichten zu Bewässerungsverboten: hilfreich, aber nicht amtlich; maßgeblich bleibt die jeweilige Allgemeinverfügung.

**Technik:** React (Version 19), Leaflet (Karte), Recharts (Diagramme), Figma (Prototyp).

## 4. Vorgehen (Mini-Projektplan)

|   |   |   |   |
|---|---|---|---|
|Meilenstein|Gewicht|Geplante Arbeit|Termin|
|M1 User Research|20 %|Problemraum klären; 5–8 Interviews und Kurzumfrage mit Gartenbesitzern; mind. 2 Personas, Nutzungskontext, 3–4 valide Anforderungen|lt. Moodle-Semesterplan|
|M2 Prototyping|20 %|Paper-Prototyp, danach Mid-/High-Fidelity-Prototyp in Figma; wichtigste User Flows aus den User Journeys|lt. Moodle-Semesterplan|
|M3 Implementierung|45 %|React-App, Anbindung der Datenquellen, responsive UI; Code-Kommentare, README, Release Notes|lt. Moodle-Semesterplan|
|M4 Evaluation|15 %|Hypothesen (H0/H1), mind. 4 Aufgaben, 2 Aspekte (Usability, Zeit), Auswertung mit Verfahren aus der Vorlesung, Signifikanzniveau, Handlungsempfehlung|lt. Moodle-Semesterplan|

**Risiken:** Datenverfügbarkeit (Fallback Pseudodaten); Erreichbarkeit von Interviewpartnern (Start der Rekrutierung in der ersten Woche). Die Projektmappe wird laufend von allen Mitgliedern gepflegt.

**KI-Hinweis:** Gliederung und Rohtext dieser Projektbeschreibung wurden mit Claude Sonnet 5.5 (Anthropic) erstellt, einschließlich Websuche für die Recherche. Die Gruppe hat Inhalt und Quellen geprüft und überarbeitet. [Umfang bei Bedarf anpassen]

**Quellen:** HLNUG (Pressemitteilung Sommerbilanz 2026, Monatsberichte April/Juli/August 2026, hlnug.de/themen/wasser), hessenschau.de (Wassersparaufrufe der Kommunen), t-online.de (Wasserentnahmeverbote Hessen 2026), WSV Pegel-Online-API, NLWKN (Grundwasserstandonline).
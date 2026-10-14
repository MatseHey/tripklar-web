# Offene Prüfpunkte der Website

Diese Hinweise standen bis zum 01.10.2026 gelb markiert (`<mark class="todo">`) direkt auf den Seiten.
Sie sind dort entfernt und hier gesammelt. Erledigte Punkte bitte streichen.

## Impressum (`impressum.html`, Abschnitt „Bildnachweise“)

- [ ] Apple verlangt die Quellenangabe „Apple Weather“ samt Link in der App (Umsetzung:
  `WeatherAttributionView`, vor Release gegen die aktuelle WeatherKit-API prüfen). Am Wetter-Chip
  der Startseite (Karte des aktiven Trips) wird sie derzeit nicht angezeigt.

## Datenschutz (`datenschutz.html`) und Privacy Policy (`privacy.html`)

- [ ] **Titelbilder / Pexels-Altdaten** (DE: Abschnitt „Titelbilder“, EN: „Cover photos“).
  Trips, die vor der Umstellung angelegt wurden, können noch eine Bild-Adresse von Pexels als
  Titelbild gespeichert haben. Diese Bilder werden direkt von den Servern von Pexels geladen;
  dabei erhält Pexels technisch bedingt die IP-Adresse des Geräts.

  Ursprünglicher Absatz zum Wiedereinsetzen, solange solche Trips existieren können
  (streichen, sobald keine mehr vorhanden sind bzw. die Altlogik in `TripCoverImage` entfernt ist):

  > Trips, die vor der Umstellung angelegt wurden, können noch eine Bild-Adresse von Pexels als
  > Titelbild gespeichert haben. Diese Bilder werden direkt von den Servern von Pexels geladen;
  > dabei erhält Pexels technisch bedingt die IP-Adresse des Geräts (Rechtsgrundlage Art. 6 Abs. 1
  > lit. f DSGVO).

  > Trips created before this change may still have a Pexels image address stored as their cover.
  > Those images are loaded directly from Pexels' servers, so Pexels technically receives the
  > device's IP address (legal basis Art. 6(1)(f) GDPR).

- [ ] **WeatherKit / Drittland** (DE: Abschnitt „Wetterdaten (Apple WeatherKit)“, EN: „Weather“).
  Ob Apple bei WeatherKit-Abfragen selbst Daten speichert oder in Drittländer (USA) übermittelt,
  ist nicht verifiziert. Aktuelle Angaben von Apple zu WeatherKit einholen und ggf. einen
  Drittlandhinweis (DPF/SCC) in beiden Sprachen ergänzen.

## GetYourGuide (Datenschutz Abschnitt 7, seit 14.10.2026)

Grundlage des Abschnitts: Code auf `main` (`GetYourGuideLink.swift`, `GetYourGuideOffer.swift`,
`GetYourGuideSlider.swift`), GetYourGuide-Partnerbedingungen (Fassung 2. August 2024, Nr. 8.5:
beide Seiten eigenständige Verantwortliche) und GetYourGuide-Datenschutzerklärung (Verantwortlicher
GetYourGuide Deutschland GmbH, Berlin; Dienstleister außerhalb der EU über Standardvertragsklauseln).
Ausführlicher Entwurf und Begründung: `docs/legal/datenschutz-abschnitt-getyourguide-widget.md` im App-Repo.

- [ ] **Netzwerkmitschnitt des Widgets** (Proxyman/Charles oder Web-Inspector): Stimmt die Datenliste
  in Abschnitt 7? Lädt das Widget weitere Domains nach (CDN, Analyse)? Falls ja, Text DE/EN anpassen.
- [ ] **Apple-Datenschutzangaben / `PrivacyInfo.xcprivacy`:** Device ID (Besucher-Kennung) und ggf.
  Product Interaction angeben; Entscheidung „Tracking ja/nein“ (davon hängen ATT-Dialog und
  Tracking-Domains ab). Am besten schriftlich bei GetYourGuide nachfragen, ob die Besucher-Kennung
  firmenübergreifend für Werbung genutzt wird.
- [ ] **Einwilligungszeile in der App:** Link zur Datenschutzerklärung (Abschnitt 7) und kurzer Hinweis
  auf Widerruf ergänzen; „Ausblenden“ ggf. deutlicher als Widerruf beschriften.
- [ ] **Anwaltliche Kurzprüfung:** Wirksamkeit der Einwilligung, § 25 TDDDG bei WebViews in Apps,
  Rechtsgrundlage lit. f für die Partnerlinks.
- [ ] Schriftliche Bestätigung des GetYourGuide-Partner-Supports, dass Widget und Partnerlinks in
  einer iOS-App zulässig sind (laut Bedingungen erlaubt, Bestätigung empfohlen).

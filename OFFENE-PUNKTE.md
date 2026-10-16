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

## GetYourGuide (Datenschutz Abschnitt 7, Stand 16.10.2026)

Das Aktivitäten-Widget ist aus der App entfernt; es gibt nur noch den nativen Partnerlink
(`GetYourGuideLink.swift`, `GetYourGuideOffer.swift`). Der Abschnitt beschreibt jetzt nur diesen Link.
Grundlage: GetYourGuide-Partnerbedingungen (Fassung 2. August 2024, Nr. 8.5: beide Seiten
eigenständige Verantwortliche) und deren Datenschutzerklärung. Ausführliche Fassung mit
Begründungen: `docs/legal/datenschutzerklaerung-de.md` (Abschnitt 8) im App-Repo.

- [ ] **GetYourGuide-Angaben prüfen** (Verantwortlicher, Anschrift Sonnenburger Straße 73 vs. 71–75,
  Speicherdauer, Drittland-Garantien) gegen deren eigene Datenschutzerklärung und Impressum — für die
  Recherche waren die Seiten nicht abrufbar. In der App-Repo-Fassung stehen die [PRÜFEN]-Marker.
- [ ] **Apple-Datenschutzangaben:** Nach Einschätzung nichts anzugeben (die App überträgt nichts an
  GetYourGuide; Seitenbesuch im Browserfenster). Unsicher, ob Apple einen festen Link als „navigate the
  open web“ wertet; im Altersfreigabe-Fragebogen „Advertising/Web access“ prüfen. `PrivacyInfo.xcprivacy`
  bleibt unverändert.
- [ ] **Anwaltliche Kurzprüfung:** Rechtsgrundlage lit. f mit Interessenabwägung, § 25 TDDDG für den
  Link, Formulierung „kein Reisevermittler“ (Nutzungsbedingungen 2) neben einem Provisions-Link.
- [ ] Schriftliche Bestätigung des GetYourGuide-Partner-Supports, dass der Partnerlink in einer iOS-App
  zulässig ist (laut Bedingungen erlaubt, Bestätigung empfohlen).

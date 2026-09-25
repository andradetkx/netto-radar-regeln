# Datenschutzerklärung – Netto-Radar

*English version below.*

Stand: 25. September 2026 (ergänzt: Österreich)

## Verantwortlicher

Kauê Andrade
E-Mail: mauezx@gmail.com

## Kurz gesagt

Netto-Radar berechnet Ihr Nettogehalt **vollständig lokal in Ihrem Browser**. Ihre Angaben (Steuerklasse, Bundesland, Kinder, Gehälter usw.) verlassen Ihren Browser nicht. Es gibt keine Tracker, keine Werbung, kein Nutzerkonto und keinen Verkauf von Daten.

## Was im Einzelnen passiert

**1. Ihre Einstellungen.** Steuerklasse, Bundesland, Kirchensteuer, Kinder, Alter, Wochenstunden, Ihr aktuelles Gehalt und Ihr Mindest-Netto werden mit `chrome.storage.sync` im Browser gespeichert. Wenn Sie in Ihrem Browser die Synchronisierung eingeschaltet haben, gleicht der Browser-Hersteller (z. B. Google) diese Einstellungen zwischen Ihren Geräten ab – nach dessen Datenschutzbestimmungen. Wir erhalten diese Daten nie.

**2. Lesen der Stellenseiten.** Auf StepStone (.de und .at), Indeed, LinkedIn Jobs, der Jobbörse der Bundesagentur für Arbeit und karriere.at liest die Erweiterung den Gehaltstext der Anzeigen, um daneben das Netto anzuzeigen. Auf anderen Seiten nur dann, wenn Sie dort selbst einen Betrag markieren und „Netto berechnen“ wählen. Der gelesene Text wird nur lokal verarbeitet und nicht übertragen.

**3. Regeldatei.** Zweimal täglich lädt die Erweiterung eine öffentliche Datei mit Wortlisten und Schaltern (`raw.githubusercontent.com/andradetkx/netto-radar-regeln`). Dabei werden keine Daten von Ihnen mitgeschickt; GitHub erhält wie bei jedem Abruf einer Webseite technisch Ihre IP-Adresse (Datenschutzerklärung von GitHub: https://docs.github.com/site-policy/privacy-policies).

**4. Schaltfläche „Interessiert?“ (Premium – bald verfügbar).** Nur wenn Sie darauf klicken, sendet die Erweiterung eine **leere** Anfrage an unseren Server (Cloudflare Workers, `netto-radar-api.mauezx.workers.dev`). Sie enthält keine Einstellungen, keine Kennung und kein Cookie. Der Server erhöht einen anonymen Zähler um 1. Damit ein Klick nicht mehrfach gezählt wird, speichert er für **24 Stunden** einen nicht umkehrbaren, mit einem geheimen Schlüssel gebildeten Hashwert aus Ihrer IP-Adresse und dem Datum; danach wird er automatisch gelöscht. Die IP-Adresse selbst speichern wir nicht; unsere Protokolle enthalten nur Pfad, Status und Dauer der Anfrage.
Rechtsgrundlage: Art. 6 Abs. 1 lit. f DSGVO (berechtigtes Interesse, die Nachfrage nach einer geplanten Funktion zu messen); der Klick ist freiwillig.
Cloudflare, Inc. verarbeitet die Anfrage als Auftragsverarbeiter; dabei ist eine Übermittlung in die USA möglich. Cloudflare ist nach dem EU-US Data Privacy Framework zertifiziert (https://www.cloudflare.com/privacypolicy/).

**5. „Problem melden“.** Öffnet Ihr eigenes E-Mail-Programm mit einem Entwurf (Seitenadresse, Gehaltstext, Ausschnitt der Anzeige). Sie sehen alles und entscheiden selbst, ob Sie ihn senden. Die Erweiterung überträgt dabei nichts.

**6. Bitte um Bewertung.** Die Erweiterung zählt lokal (`chrome.storage.local`), wie oft Sie die Aufschlüsselung geöffnet haben, um einmalig um eine Bewertung im Chrome Web Store zu bitten. Dieser Zähler verlässt Ihren Browser nicht.

## Geplante Premium-Funktion

Ein Abgleich des Lebenslaufs mit Stellenanzeigen ist geplant, aber **noch nicht aktiv**. Bevor er startet, wird diese Erklärung aktualisiert und die Funktion nur nach Ihrer ausdrücklichen Nutzung Daten übertragen.

## Ihre Rechte

Sie haben das Recht auf Auskunft, Berichtigung, Löschung, Einschränkung der Verarbeitung, Widerspruch und Datenübertragbarkeit (Art. 15–21 DSGVO) sowie das Recht, sich bei einer Datenschutz-Aufsichtsbehörde zu beschweren. Da wir keine Daten speichern, die Sie identifizieren, können wir Ihnen in der Regel keine Daten zuordnen. Schreiben Sie uns bei Fragen gern an mauezx@gmail.com.

Wenn Sie die Erweiterung entfernen, löscht der Browser alle lokal gespeicherten Einstellungen.

---

# Privacy Policy – Netto-Radar

Last updated: 25 September 2026 (added: Austria)

## Controller

Kauê Andrade
Email: mauezx@gmail.com

## In short

Netto-Radar calculates your net salary **entirely locally in your browser**. Your inputs (tax class, state, children, salaries, etc.) never leave your browser. No trackers, no ads, no account, no sale of data.

## In detail

**1. Your settings** are stored with `chrome.storage.sync`. If browser sync is on, your browser vendor (e.g. Google) syncs them between your devices under its own privacy policy. We never receive them.

**2. Reading job pages.** On StepStone (.de and .at), Indeed, LinkedIn Jobs, the Federal Employment Agency job board and karriere.at, the extension reads the salary text of job ads to show the net amount next to it; on other pages only when you select an amount and choose "Calculate German net pay". This text is processed locally and not transmitted.

**3. Rules file.** Twice a day the extension downloads a public file of word lists and switches from `raw.githubusercontent.com/andradetkx/netto-radar-regeln`. No data of yours is sent; like any web request, GitHub technically receives your IP address (GitHub privacy statement: https://docs.github.com/site-policy/privacy-policies).

**4. "Interested?" button (Premium – coming soon).** Only when you click it, the extension sends an **empty** request to our server (Cloudflare Workers). It contains no settings, no identifier and no cookie. The server adds 1 to an anonymous counter. To avoid counting a click twice, it keeps a non-reversible keyed hash of your IP address and the date for **24 hours**, then deletes it automatically. We do not store the IP address itself; our logs contain only the path, status and duration of the request. Legal basis: Art. 6(1)(f) GDPR (legitimate interest in measuring demand for a planned feature); clicking is voluntary. Cloudflare, Inc. processes the request as a processor; a transfer to the USA is possible. Cloudflare is certified under the EU-US Data Privacy Framework.

**5. "Report a problem"** opens your own email program with a draft (page address, salary text, snippet of the ad). You see everything and decide whether to send it. The extension transmits nothing.

**6. Review prompt.** The extension counts locally how often you opened the breakdown, to ask once for a Chrome Web Store review. This counter never leaves your browser.

## Planned premium feature

Matching your CV against job ads is planned but **not active yet**. Before it launches, this policy will be updated.

## Your rights

You have the rights of access, rectification, erasure, restriction, objection and data portability (Art. 15–21 GDPR) and the right to lodge a complaint with a supervisory authority. Since we store no data that identifies you, we generally cannot link any data to you. Questions: mauezx@gmail.com.

Removing the extension deletes all locally stored settings.

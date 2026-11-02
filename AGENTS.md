# Agentenleitfaden — AdScroll

## Einstieg
Offline-Android-Feed mit fiktiven Anzeigen und geprüftem Sponsor-Kataloggenerator; Enzyklopädie und echte Partnerschaften sind Ausbauziele.

Lies README.md, TESTING.md und HANDOFF.md. Anforderungen und vorhandene Funktionen unterscheiden. Technische Grundlagen: SPONSORS.md. Die bestehenden Detaildokumente bleiben maßgeblich; keine leeren SPEC-/ARCHITECTURE-/TODO-Kopien erzeugen. Offene Arbeit und Verlauf: PROGRESS.md; konkrete Einnahmegrenzen: MONETIZATION.md, soweit vorhanden.

## Umgebung und Start
JDK 21; Android SDK Platform/Build Tools 36; PowerShell 7; Node 24 für Katalogtests.

Frische isolierte Kopie: ./build.ps1 -SdkPath $env:ANDROID_SDK_ROOT -JavaHome $env:JAVA_HOME. Sponsoroptionen ohne Rechte-/Vertragsprüfung nicht verwenden.

Tests: `node --test tests/*.test.mjs`. Bei mehreren Befehlen einzeln ausführen und jeden Exitcode prüfen. Vorhandene Installationen verwenden; fehlende Voraussetzungen melden statt automatisch globale Pakete oder Modelle zu installieren.

## Grenzen
- Größere Änderungen auf einem eigenen Branch; zuerst git status und fremde Änderungen prüfen. Keine parallelen widersprüchlichen Arbeiten am selben Branch.
- Keine Dateien/Repos löschen oder verschieben, keine Historien umschreiben, kein Force-Push. Keine Lizenzänderungen ohne konkrete Freigabe.
- Keine Secrets, privaten Daten, echten Nutzerinhalte oder großen generierten Dateien committen. Keine Sichtbarkeitsänderungen oder zusätzlichen Veröffentlichungen ohne Freigabe.
- Keine bezahlten Dienste, Werbenetzwerke, Zahlungsanbieter oder externe Nachrichten aktivieren.
- Kein Klickbetrug, kein erzwungenes Ad-Engagement; fremde Anzeigen/Logos nicht ungeprüft übernehmen. Demo bleibt sichtbar gekennzeichnet.
- Projektwerkzeuge ändern keine anderen Projektquellen. Build-/Testartefakte in isolierten, ignorierten Arbeitsordnern halten. Vorhandene Ausgaben nicht unbesehen überschreiben.

## Nächste sichere Etappe
Eigene, quellenbelegte Werbe-Lerninhalte ergänzen und vom fiktiven Feed unterscheiden; danach Sponsor-Testkatalog auf Emulator prüfen.

## Übergabe
HANDOFF.md aktualisieren: Ausgangscommit/Branch, konkrete Änderungsliste, ausgeführte Befehle, Ergebnis, ausgelassene Tests samt Grund, Risiken und nächste Etappe. Nur tatsächlich ausgeführte Tests als bestanden ausweisen. Vor Merge Diff und Tests prüfen; externe Freigaben bleiben offen.

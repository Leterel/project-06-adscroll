# Tests und Reproduzierbarkeit — AdScroll

## Voraussetzungen
JDK 21; Android SDK Platform/Build Tools 36; PowerShell 7; Node 24 für Katalogtests.

## Befehle
```text
node --test tests/*.test.mjs
```

Start/Build: Frische isolierte Kopie: ./build.ps1 -SdkPath $env:ANDROID_SDK_ROOT -JavaHome $env:JAVA_HOME. Sponsoroptionen ohne Rechte-/Vertragsprüfung nicht verwenden.

## Tatsächlicher Befund vom 02.11.2026
7 Tests: 5 bestanden, 2 Signiertests ausgelassen. Java-Katalog wurde tatsächlich kompiliert und geprüft; frischer APK-Build/Signatur/Ausrichtung bestanden.

Bei fehlenden Paketen/Hardware/Betriebssystemen ist das Ergebnis „nicht ausgeführt“, kein Pass. Plattformnachweise aus älteren Detailberichten gelten nur für die dort genannten Versionen. Android-Automatisierung ausschließlich mit expliziter emulator-Seriennummer und bestätigtem ro.kernel.qemu=1. Physische Geräte, persönliche Medien und Produktionskonten sind keine Testfixtures.

## Vor Merge
`git diff --check` ausführen; relevante Funktionstests wiederholen, wenn Codeänderungen ihren Befund entwerten. Speicherdaten/alte Versionen erhalten. Fehlende externe Abnahmen in HANDOFF.md benennen.

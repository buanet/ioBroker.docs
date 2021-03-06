---
translatedFrom: en
translatedWarning: Wenn Sie dieses Dokument bearbeiten möchten, löschen Sie bitte das Feld "translationsFrom". Andernfalls wird dieses Dokument automatisch erneut übersetzt
editLink: https://github.com/ioBroker/ioBroker.docs/edit/master/docs/de/adapterref/iobroker.homee/README.md
title: ioBroker homee Adapter
hash: FhOuxeUOxXI0VM55+mR5qD8k0SJ09JRQMcCp5MY++ds=
---
![Logo](../../../en/adapterref/iobroker.homee/admin/homee.png)

![Anzahl der Installationen](http://iobroker.live/badges/homee-stable.svg)
![Greenkeeper-Abzeichen](https://badges.greenkeeper.io/Apollon77/ioBroker.homee.svg)

# IoBroker homee Adapter
** Dieser Adapter verwendet Sentry-Bibliotheken, um Ausnahmen und Codefehler automatisch an die Entwickler zu melden. ** Weitere Details und Informationen zum Deaktivieren der Fehlerberichterstattung finden Sie unter [Sentry-Plugin-Dokumentation](https://github.com/ioBroker/plugin-sentry#plugin-sentry)! Sentry Reporting wird ab js-controller 3.0 verwendet.

## Beschreibung
Dieser Adapter verbindet ioBroker mit homee und bietet die folgenden Funktionen:

* ermöglicht die Verbindung über IP oder Homee-ID und Benutzername / Passwort
* Lesen Sie alle Geräte (Knoten) und Status (Attribute) und zeigen Sie deren Werte einschließlich Aktualisierungen in ioBroker an
* Erlaube das Ändern von Werten in ioBroker und sende sie an homee zurück, um Geräte zu steuern
* fungiert als ioBroker-Verlaufsanbieter für alle Geräte mit Status, bei denen der Verlauf in homee aktiviert ist. Dies bedeutet, dass Sie die in homee gespeicherten Verlaufswerte verwenden können, um sie in ioBroker mithilfe von Flot, Admin oder auch JavaScript anzuzeigen, einschließlich aller Aggregationen auf Datenebene, wie z. Verlaufsadapter

(noch) nicht unterstützt:

* Gruppen, weil sie keine Funktionen wie einen Status auf Gruppenebene oder echtes Schreiben für alle Geräte gleichzeitig in homee anbieten
* Heizpläne

Dieser Adapter basiert auf der herausragenden Arbeit von [stfnhmplr] (http://twitter.com/stfnhmplr) und seine [homee-api](https://github.com/stfnhmplr/homee-api).

## Bekannte Probleme
* Auf js-controller <1.5.0 kann es seltsame Auswirkungen haben, wenn andere Verlaufsanbieter für einige der Rollen aktiviert werden (z. B. "switch").

## So melden Sie Probleme und Funktionsanforderungen
Bitte verwenden Sie dazu GitHub-Probleme.

Am besten stellen Sie den Adapter auf den Debug-Protokollmodus (Instanzen -> Expertenmodus -> Spaltenprotokollstufe). Dann holen Sie sich bitte die Protokolldatei von der Festplatte (Unterverzeichnis "log" im ioBroker-Installationsverzeichnis und nicht von Admin, da Admin die Zeilen abschneidet). Wenn Sie es nicht gerne in der GitHub-Ausgabe bereitstellen, können Sie es mir auch per E-Mail senden (iobroker@fischer-ka.de). Bitte fügen Sie einen Verweis auf das relevante GitHub-Problem hinzu UND beschreiben Sie auch, was ich zu welchem Zeitpunkt im Protokoll sehe.

## Changelog

### 1.0.7 (2020-06-12)
* (Apollon77) Fix Admin finally

### 1.0.6 (2020-06-12)
* (Apollon77) Fix Admin

### 1.0.5 (2020.04.12)
* (Apollon77) update homee lib to prevent a crash case

### 1.0.4 (2020.04.12)
* (Apollon77) fixes and optimizations
* (Apollon77) use js-controller 3.0 features if available 

### 1.0.2 (2020.03.22)
* (Apollon77) fixes and optimizations 

### 1.0.1 (2020.03.18)
* (Apollon77) fixes and optimizations 

### 1.0.0 (2020.03.13)
* (Seraphis411) fixed writing of HomeeMode
* (Seraphis411) bumped version of homee-api to 0.12.0 (no new features adopted)
* (Seraphis411) now support for nodejs 10 thanks to newer ws-library (^7.1.2) in homee-api
* (Apollon77) add sentry for error reporting
* (Apollon77) update homee api to 0.15.0

### 0.3.2 (2018.08.07)
* (Apollon77) corrected automatic role determination and added playing state for homeegrams

### 0.3.1 (2018.07.27)
* (Apollon77) Special handling for RGB values (delete objects and restart adapter)
* (Apollon77) Also allow enabling/disabling of Homeegrams (best delete objects unter Homee-0.Homeegrams!)
* (Apollon77) Optimize some roles, more Role feedback via Github issues please!

### 0.2.0 (2018.07.04)
* (Apollon77) Fix History logic (try) and add Homeegram support

### 0.1.1 (2018.07.04)
* (Apollon77) initial version

## License
The MIT License (MIT)

Copyright (c) 2018-2020 Apollon77 <iobroker@fischer-ka.de>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
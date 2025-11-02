**Symmetrische Verschlüsselung**
- Schlüsselaustauschproblem:
- Ein schlüssel -> der Empfänger und Absender haben die gleiche Schlüssel
- schnelleres Verfahren
- Entschlüsselung: einen geheimen Schlüssel wird definiert, mit der gleichen Schlüssel verwendet der Empfänger den gleichen Algotihmus in umgekehrter Richtung, Ergebnis ist der Klartext
- Beispiel: Cäsar, Vigenère

<img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/6a01a97e-721f-409a-af1d-8b54a1e2a739" />

<img width="1458" height="763" alt="image" src="https://github.com/user-attachments/assets/646fc6f2-c002-4500-b4d9-0edb4dea02fa" />

**Asymmetrische Verschlüsselung**
- erzeugt ein Schlüsselpaar, besteht aus einem privaten und öffentlichen Schlüssel
- der verschlüsselte Nachricht mit dem öffentlichen Schlüssel kann nur mit einem privaten Schlüssel entschlüsselt werden
- es kann niemand die Nachricht entschlüsseln da man die private Schlüssel dazu benötigt
- nur den Empfänger hat die private Schlüssel
- öffentliche Schlüssel: verwendet zum verschlüsseln und überprüfung
- langsameres Verfahren
- verwendet in digitalen Kommunikationen
- Beispiel: RSA, Rabin, Elgamal


**Hyprid Verfahren**  
- Absender: hat schlüssel für symmetrische verfahren und verschlüsselt mit dem öffentlichen schlüssel von empfänger und sendet an Empfänger
- Empfänger: verschlüsselt mit privaten schlüssel die symmetrische Schlüssel
- der symmetrische Schlüssel wird mit dem asymmetrischen verfahren verschlüsselt
- mit dem symmetrischen verfahren mit n teilnehmern werden n * (n-1) Schlüssel benötigt
- asymmetrisch nur 2 * n Schlüssel


**Hashfunktion**  
Zweck der Sicherstellung des Datenintegrität: 
- Veränderung an Daten erkennen
- laden der Daten wird der Hashwert erneut berechnet und mit der ursprünglichen verglichen
- stimmen beide Hashwerte überein sind die daten integer & unverändert
- unterscheiden sie sich, wurde die datei verändert, manipuliert oder beschädigt

Funktionsweise:
- öfters in Hexdezimalform (0-9, A-F), auch in Binärform
- Eine Hashfunktion erzeugt aus beliebigen Daten einen eindeutigen Fingerabdruck
- mit dem man Daten schnell vergleichen und ihre Unverändertheit prüfen kann.


**Authentifizierung & Autorisierung**  
Authentifizierung:
- prüft Identität
- wer bist du? (Mehrfaktor-Authentifizierung)
- erfolgt vor autorisierung

Autorisierung:
- berechtigung um zuweisen zu können
- gewährt/verweigert den Zugriff auf bestimmte Ressourcen
- was darfst du tun? (Zugriffskontrolle)


**Datensicherung & Backupstrategien**  
Datenkompression
- Speicherplatz sparen & Übertragungszeiten verringern​
- Originaldaten bleiben exakt erhalten
- Nicht vollständig wiederherstellbar (z.B. ZIP, Deduplizierung)

**Vollsicherung, Differenzielle Sicherung, Inkrementelle Sicherung**  
Vollsicherung
- Alle Daten vollständig gesichert​
- komplette Kopie des Systems oder Verzeichnisses.​
- einfache und schnelle Wiederherstellung

Differenzielle  
- Änderungen seit letzter Sicherung​
- Braucht wenig Speicherplatz​
- Alle inkrementelle Sicherungen + Vollsicherung​

Inkrementelle 
- Alle geänderten Daten seit letzten Vollsicherung​
- Braucht immer mehr Speicherplatz​
- Letzte differenzielle Sicherung + Vollsicherung​

**Block-Level vs File-Level Backup**

Block
- Sichert einzelne Dateien und Verzeichnisse über das Dateisystem
- nur bestimmte Ordner sichern (z.B. Home-Ornder)
- Einfach zu verwalten und wiederherzustellen
- Systeminformationen können verloren gehen

File
- Sichert die Daten auf der Ebene der Datenblöcke des Speichermediums
- Erstellung eines kompletten Festplatten-Images
- Ideal für vollständige Systemabbilder
- Benötigt meist mehr Speicherplatz

**Hot Backup vs Cold Backup**  
- **Hot**: Durchführung, während das System oder Datenbank in Betrieb ist -> Sie werden gesichert, während Benutzer aktiv damit arbeiten.
- **Einsatzwerke**: Online-Banking Systeme, E-Commerce Websiten (z.B. Zalando)
- **Cold**: Wird gemacht, wenn das System vollständig heruntergefahren oder nicht aktiv ist -> Im Ruhestand durchführen
- **Einsatzwerke**: Unternehmensdatenbank in Wartungszeiten, Server vor großen Systemupdates

**Datensicherungsstrategie**  
- Häufigkeit: weniger wichtig -> wöchentlich, ansonsten täglich  
- verschiedene Datenträger: 3, 2, 1 Regel


**Lizenzmodell & Urheberecht**  
**proprietär-MS Office**
- recht: nutzung gemäss Lizenzvertrag
- pflicht: zahlung, keine modifikation/Weitergabe

**OS-Linux Firefox** 
- recht: Nutzung, Weitergabe, Änderung
- pflicht: Einhaltung Lizenzbedingungen

**Creative Commons**
- recht: Nutzung von Inhalten
- pflicht: Namensnennung, ggf. weitergabe unter gleichen Bedingungen


**Ransomeware**  
Funktionsweise
- Phishing Email, links, unsichere Download file
- Verschlüsselung, Erpressung, lösegeld forderung

Bedrohungslage
- zugriff blockiert, verhindert zugang zu wichtigen Daten/information(Compi, Daten)
- sperrt Bildschirm, Datei nicht mehr öffnen/benutzen
- Drohung, Erpressungsnachricht

Schutz
- regelmässige Backups, antiviren Software
- zugriffsrechte beschränken, system-/softwareupdates

Reaktionsmassnahme
- Backup prüfen/wiederherstellen, **Meldung**
- IT-Sicherheitsdienst / IT-Support Team

Ransomware: Key Takeaways
- Täter zielen oft auf Backups, Domain-Controller und kritische Daten — **Backup-Sicherheit entscheidet häufig über Ausfallzeit.**
- **Infektionsvektoren: Phishing-Mails**, unsichere RDP/Remote-Zugänge, ungepatchte Dienste, bösartige **Makros/Dateianhänge.**
- Ransomware-Gruppen betreiben oft **„double extortion“**: Daten werden **gestohlen und veröffentlicht**, falls kein Lösegeld gezahlt wird.
- **Schnelle Isolierung** des betroffenen Hosts/Netzwerks **reduziert** lateral movement und **Schadensumfang**.
- Regelmäßige, getestete Wiederherstellungsprozesse (Restore-Tests) sind oft wichtiger als reine Backup-Existenz.
- Transparenz & **Meldepflichten**: In vielen Jurisdiktionen (z. B. EU **DSGVO**) kann Datenverlust meldepflichtig sein — rechtlichen Rat frühzeitig einholen.
- **Beweissicherung** (**Logs**, Images) ist wichtig für forensische Analyse und ggf. Strafverfolgung/Versicherung.

**Warum machen wir ein Backup?**

```mermaid
mindmap
  root((Warum wir ein Backup machen))
    Datensicherheit
      Schutz vor Datenverlust
      Wiederherstellung nach Defekten
      Absicherung gegen versehentliches Löschen
    Schutz vor Bedrohungen
      Malware & Viren (z. B. Ransomware)
      Hackerangriffe
      Sabotage oder Diebstahl
    Technische Probleme
      Festplattencrash
      Softwarefehler
      Stromausfall
    Rechtliche & organisatorische Gründe
      Einhaltung gesetzlicher Vorgaben
      Nachvollziehbarkeit (z. B. bei Audits)
      Schutz geschäftskritischer Daten
    Zeit & Kosten sparen
      Schnelle Wiederherstellung
      Vermeidung von Ausfallzeiten
      Geringere Folgekosten
    Flexibilität & Mobilität
      Zugriff von überall (Cloud-Backup)
      Versionierung & Historie verfügbar
  ```

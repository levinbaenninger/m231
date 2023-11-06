# Datenlöschung, data resilience &amp; data masking

## Datenlöschung

Gelöschte Daten können nicht mehr kompromittiert werden, daher ist die Löschung von Daten ein zentrales Werkzeug eines Datenschutz Management
Systems. Jedoch muss man beachten, dass Löschen nicht gleich Löschen ist. Je nachdem, wie die Daten gelöscht werden, können sie mit geeigneten
Tools wiederhergestellt werden.

Wenn nicht spezifisch verlangt, gibt man mit einem Löschbefehl den Speicher wieder frei. Dies führt dazu, dass die entsprechenden Einträge für das
Auffinden der Dateien im Dateisystem gelöscht werden, die tatsächlichen Daten jedoch einfach auf dem Speichermedium bleiben. Dasselbe gilt für das
Formatieren einer Festplatte.

Um eine sichere Löschung zu gewährleisten, muss daher auf spezielle Werkzeuge wie `SDelete` auf Windows bzw. `shred` auf Linux zurückgegriffen werden.

## Data Masking

Beim Data Masking will man die Verwendung von Daten auf die Personengruppen einschränken, welche die Daten auch tatsächlich benötigen.

Jedoch brauchen Entwickler realitätsnahe Daten, um Funktionen zu testen. Um ihnen realitätsnahe Datenbasen bieten zu können, bedient man sich beim
Maskieren. Dabei wird grundsätzlich mit der echten Datenbasis gearbeitet, allerdings werden Personendaten maskiert, indem z.B. Informationen
vertauscht werden oder aber gewisse Teile durch Platzhalter 'überschrieben' werden (z.B. alle Zahlengruppen einer Kreditkarten-Nr. bis auf die
Letzte werden durch `XXXX` ersetzt). Auch können Zufallsgeneratoren zum Einsatz kommen.

## Data Resiliency

Die Widerstandsfähigkeit von Daten beschreibt, die Fähigkeit eines IT-Systems, mit Störungen umgehen zu können.

| Störung                           | Beispiele von Gegenmassnahmen                                               |
|-----------------------------------|-----------------------------------------------------------------------------|
| Ausfall von Hardware              | Redundanzen im System vorsehen, um die Ausfallsicherheit zu erhöhen.        |
| Fälle 'höherer Gewalt'            | Geographische Redundanzen mit engmaschiger Synchronisation einplanen.       |
| Ausfälle in der Energieversorgung | Notstrom-Konzept erarbeiten: USV, Notstromaggregate, etc.                   |
| Störungen des Internetzugangs     | Redundanz in der Vernetzung vorsehen: Verschiedene Anbieter, mehrere Routen |
| Störung in Softwarediensten       | Backupdienste vorhalten                                                     |
| ...                               |                                                                             |

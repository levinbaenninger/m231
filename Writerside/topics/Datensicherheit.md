# Datensicherheit

Unter Datensicherheit versteht man Schutz digitaler Informationen vor unautorisiertem Zugriff, Datenkorruption sowie Diebstahl, während dem ganzen
Lebenszyklus der Daten.

Wenn ein Datenschutzsystem aufgebaut wurde, sollte dieses nicht nur gegen Cyberangriffe, sondern auch gegen weitere Gefahren wie z.B. Diebstahl von
Daten durch Insider, (`insider data breach`) oder menschliches Fehlverhalten schützen.

Datensicherheit bedeutet unter anderem Systeme so zu konstruieren und notwendige Tools bereitzustellen, mit welchen klar sichtbar gemacht werden
kann, wo sich geschützte Daten befinden und wie diese genutzt werden. Insbesondere sollten diese Systeme auch Verschlüsselung und `data
redaction` (z.B. Kreditkarten-Nr. bei SQL-Datenbank) bereitstellen. Generell müssen die Systeme mit den aktuellen Gesetzen konform sein.

Die Datensicherheit kann man auch unter dam Akronym `VIVA` zusammenfassen.

<tabs>
    <tab title="V">
        <b>V</b>ertraulichkeit: nur Admins haben Zugriff, TFA, Login
    </tab>
    <tab title="I">
        <b>I</b>ntegrität: Daten können nicht verändert werden, ohne dass es jemand mitbekommt
    </tab>
    <tab title="V">
        <b>V</b>erfügbarkeit: Daten sollen immer verfügbar sein.
    </tab>
    <tab title="A">
        <b>A</b>uthentizität: die Quelle ist authentisch, bspw. Phishing-Mails
    </tab>
</tabs>
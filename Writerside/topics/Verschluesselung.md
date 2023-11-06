# Verschlüsselung

<show-structure depth="2" />

Durch die Verschlüsselung kann ein wirksamer Schutz der Daten erreicht werden. Dabei wird mithilfe eines Schlüssels die Daten verändert, sodass
sie wie zufällige Bitmuster aussehen (`Verschlüsselung`). Ein Verschlüsselungsvorgang (Algorithmus) ist immer umkehrbar (`Entschlüsselung`). Dabei
unterscheidet man zwischen zwei kryptographischen Verfahren:

## Symmetrische Verschlüsselung

- Ein einziger Schlüssel
- Für alle Teilnehmer umkehrbar, die über den Schlüssel verfügen
- Man spricht auch von `Shared Secret`
- Jeder Teilnehmer kann den Klartext lesen

![Symmetrische Verschlüsselung](symmetrisch.jpg) { thumbnail="true" }

### Vor- und Nachteile (Symmetrisch)

<tabs>
    <tab title="Vorteile">
        <list type="bullet">
            <li>Sicher</li>
            <li>Einfach</li>
        </list>
    </tab>
    <tab title="Nachteile">
        <list type="bullet">
            <li>Austausch des Schlüssels darf nicht übers Internet geschehen</li>
            <li>Birgt einige Risiken</li>
        </list>
    </tab>
</tabs>

## Asymmetrische Verschlüsselung

- Unterschiedliche Schlüssel für Ver- und Entschlüsselung, sog. `Public-Key Verfahren`
- Schlüsselpaar bestehend aus öffentlichem und privatem Schlüssel
- Nur Kombination von beiden erlaubt Entschlüsselung
- Öffentlicher Schlüssel wird wirklich veröffentlicht, privater Schlüssel bleibt geheim
- Daten, die mit dem öff. Schlüssel verschlüsselt werden, können nur durch den Besitzer des privaten Schlüssels entschlüsselt werden
- Daten, die mit dem privaten Schlüssel verschlüsselt werden, können mit dem öffentlichen Schlüssel entschlüsselt werden.

![Asymmetrische Verschlüsselung](assymetrisch.jpg) { thumbnail="true" }

### Vor- und Nachteile (Asymmetrisch)

<tabs>
    <tab title="Vorteile">
        <list type="bullet">
            <li>Sehr sicher</li>
        </list>
    </tab>
    <tab title="Nachteile">
        <list type="bullet">
            <li>Rechenintensiv</li>
            <li>Hoher Datenverbrauch</li>
            <li>Langsam</li>
        </list>
    </tab>
</tabs>

## Hybride Verschlüsselung

Tatsächlich findet in technischen Lösungen oft eine hybride Verschlüsselung statt. Dateien und Datenströme werden symmetrisch verschlüsselt (z.B.
bei HTTPS), während das geteilte Geheimnis mit einem asymmetrischen Verfahren ausgetauscht wird.

## Man in the Middle Attacke

Bei einer `Man in the Middle Attacke` handelt es sich um eine Möglichkeit, die Asymmetrische Verschlüsselung zu 'attackieren'.

Das funktioniert so:

![Man in the Middle](man_middle.jpg) { thumbnail="true" }
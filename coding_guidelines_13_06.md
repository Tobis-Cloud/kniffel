# KI-Coding-Guideline: Soft Modern Neon Glassmorphism

## WICHTIGE SYSTEM-ANWEISUNG FÜR DIE KI
* **Sprachvorgabe:** Antworte immer kurz, klar und einfach auf Deutsch.
* **Prozess:** Erstelle den Implementierungsplan, Erklärungen und alle Texte auf Deutsch.
* **Code-Ausgabe:** Bei Codeänderungen immer den gesamten Code mit den Änderungen ausgeben. Excel-Formeln immer in separaten Code-Blöcken bereitstellen.

---

## 1. Visuelle Stil-Beschreibung (Wie es aussehen MUSS)

### Grundstimmung & Atmosphäre
Die Anwendung muss wie eine edle, futuristische Software-Schnittstelle wirken. Das Design basiert auf absolutem Minimalismus, kombiniert mit dreidimensionaler Tiefenwirkung durch geschliffenes Glas und sanft leuchtende Lichtquellen im virtuellen Raum.

### Hintergrund & Beleuchtung
* **Die Basis:** Ein tiefes, absolutes Schwarz als Fundament. Keine grauen Flächen.
* **Die Raum-Aura:** Im Hintergrund liegt eine extrem dezente, fixierte lila Farb-Aura. Sie leuchtet unaufdringlich aus der Mitte heraus und verhindert, dass das Schwarz leblos wirkt.
* **Das Glühen (Ambient Glow):** Alle farbigen Elemente und Texte haben keine harten Lichtkanten, sondern ein weiches, diffuses Nebel-Glühen, das in den Raum strahlt.

### Der Milchglas-Effekt (Glassmorphismus)
* Jede Karte, jeder Container und jedes Steuerungs-Panel sieht aus wie hochwertiges, dickes Milchglas mit starker Unschärfe (`blur`).
* **Lichtkante:** Um die Glaskarten perfekt vom schwarzen Hintergrund zu trennen, besitzt jedes Element eine hauchdünne, fast transparente weiße Oberflächenkante (Subpixel-Rahmen), die das Umgebungslicht reflektiert.

### Typografie & Formen
* **Schriftstil:** Moderne, serifenlose System-Schriften. Haupttitel sind riesig, extrem dünn geschrieben, haben weite Zeichenabstände und sind komplett in GROSSBUCHSTABEN.
* **Labels:** Kleine Funktionstexte oder Beschriftungen sind winzig, fett und dunkelgrau gedimmt.
* **Formen:** Extrem weiche, moderne Abrundungen. Große Karten haben stark abgerundete Ecken, Buttons und Eingabefelder sind elegant, aber etwas dezenter abgerundet.

### Interaktionen & Eingaben
* **Formularfelder:** Eingabefelder und Dropdowns sind fast unsichtbar im Glas integriert. Erst beim Reinklicken (Fokus) leuchtet der Rahmen in einem weichen Neon-Blau auf und wirft einen sichtbaren Lichtstrahl.
* **Buttons:** Knöpfe sind standardmäßig transparent und haben nur eine feine Neon-Lichtkante. Erst beim Darüberfahren (Hover) füllen sie sich ganz dezent mit der jeweiligen Akzentfarbe. Alle Übergänge geschehen fließend und butterweich.
* **Pulsieren:** Haupt-Aktionsknöpfe (z.B. "Starten") haben ein beruhigendes, langsames "Atmen" – das Leuchten schwillt im Sekundentakt organisch an und ab.

---

## 2. Struktur- & Feature-Vorgaben

### Platzoptimierung (PC vs. Smartphone)
* **Allgemein:** Die App nutzt ein Full-Bleed-Schnittstellen-Konzept. Das bedeutet: Das globale Scrollen der gesamten Webseite ist komplett gesperrt. Die App fühlt sich an wie eine native Desktop- oder iOS/Android-App. Scrollen ist nur innerhalb von klar definierten Listen oder Tabellen erlaubt.
* **Auf dem PC:** Die Inhalte werden auf eine edle maximale Breite zentriert und harmonisch im Raum platziert.
* **Auf dem Smartphone:** Das Layout schaltet sofort auf maximale Platzausnutzung um. Die äußeren Abstände werden auf ein Minimum reduziert, die Eckenradien der Karten leicht gestrafft und Steuerungselemente klappen untereinander, um jeden Millimeter des Displays effizient mit App-Inhalten zu füllen.

### Automatisches App-Icon & Meta-System
* Jedes Projekt muss im Header sofort als native Web-App konfiguriert werden (Ganzer Bildschirm, statusbar-style transparent).
* Das System bindet automatisch eine Bilddatei namens `[projektname].jpeg` (exakt baugleich zum Namen der App/des Projekts) als Standard-Browser-Favicon sowie als Apple-Touch-Icon für iOS-Startbildschirm-Lesezeichen ein.

### Zustands-Speicherung (localStorage)
* Alle App-Zustände, Benutzereingaben oder Spielstände müssen im Hintergrund atomar im `localStorage` gesichert werden.
* **FOUC-Schutz (Flacker-Schutz):** Um beim Laden der Seite ein unschönes visuelles Ruckeln oder Aufblitzen zu verhindern, muss die App den Speicher über ein Inline-Skript sofort beim Öffnen des `<body>`-Tags auslesen, noch bevor die Elemente auf dem Bildschirm gezeichnet werden.

### High-End Zusatzfeatures
* **Glas-Scrollbars:** Da normale Browser-Scrollbalken das edle Design zerstören, werden diese durch hauchdünne, teiltransparente Neon-Scrollbalken ersetzt.
* **Geräte-Schonung (Performance Fallback):** Wenn ein Smartphone im Stromsparmodus läuft oder der Nutzer "reduzierte Bewegung" aktiviert hat, schaltet die App den rechenintensiven Milchglas-Filter automatisch ab und ersetzt ihn durch ein performantes, mattes Tiefschwarz.

# **Changelog \- Screensaver Woods**

Alle wichtigen Änderungen an diesem Projekt werden in dieser Datei dokumentiert. Das Projekt nutzt Semantic Versioning (SemVer).

## **\[1.32.0-alpha.1\] \- Planung / In Arbeit**

### **Geplant**

* **Wettersystem (Niederschlag)**: Implementierung von Regen- und Schneeeffekten, die auf den Tag-Nacht-Zyklus reagieren.  
* **Interaktive Kamera**: Optionale Steuerung des Parallax-Offsets durch Mausbewegungen für eine stärkere Immersion.  
* **Performance-Audit**: Untersuchung der all.sort()-Operation in der Render-Schleife zur Optimierung bei hoher Entitäten-Dichte.

## **\[1.31.0\] \- 2024-05-24**

### **Verbessert**

* **Intelligente Welt-Generierung**:  
  * **Kollisionsvermeidung**: Der Platzierungs-Algorithmus für den See wurde überarbeitet. Er prüft nun aktiv auf Überschneidungen mit dem ForestPath und hält einen Sicherheitsabstand zum Dorf (Village) ein. Dies verhindert unnatürliche Überlagerungen wichtiger Landschaftselemente.  
* **Tiefensortierung (Z-Indexing)**:  
  * Implementierung eines stabilen Sortier-Algorithmus (all.sort), der alle Entitäten (inklusive der neuen Hunde und Felsen) präzise voreinander oder hintereinander rendert.  
  * Besondere Berücksichtigung finden nun fliegende Objekte wie Libellen (Dragonfly) und Vögel (Bird), die unabhängig von ihrer vertikalen Position korrekt über den jeweiligen Boden-Layern gezeichnet werden.

## **\[1.30.1\] \- 2024-05-23**

### **Optimiert**

* **Atmosphärische Beleuchtung für Hunde**: Die Hunde nutzen nun denselben Tiefen- und Licht-Algorithmus (globalAlpha-Berechnung basierend auf Y-Tiefe) wie die Umgebungsobjekte. Sie fügen sich dadurch bei Nebel oder Dunkelheit natürlicher in die Landschaft ein.  
* **Lokalisierte Farmer-KI**: Der Arbeitsradius der Farmer wurde auf den Bereich ihrer jeweiligen Gehöfte begrenzt, um eine logischere Zuordnung von Wohn- und Arbeitsplatz zu gewährleisten.

## **\[1.30.0\] \- 2024-05-23**

### **Hinzugefügt**

* **Hunde-System**: Einführung von Hunden auf den Farmen mit eigenständiger KI (Zustände: SITTING, WALKING, IDLE) und Animationen für wedelnde Schwänze.  
* **Farmer-Tagesabläufe**: Farmer folgen einem zeitabhängigen Zyklus (Warten am Haus, Weg zum Feld, Arbeit mit Werkzeug-Animation, Heimkehr am Abend).  
* **Erweiterte Tier-KI**: Rehe besitzen nun eine verfeinerte Pausen-Logik mit graze-Animationen (Grasen) für ein realistischeres Verhalten.

### **Optimiert**

* **Z-Sorting (Tiefenebenen)**: Die Libellen wurden in das globale Sortierungssystem integriert. Sie werden nun korrekt hinter Bäumen gerendert, bleiben aber visuell über dem Wasserspiegel des Sees.

## **\[1.29.2\] \- 2024-05-22**

### **Geändert**

* **Rebranding**: Das Projekt wurde offiziell von "Woods Engine" in **Screensaver Woods** umbenannt.  
* Update der UI-Statusanzeige (uiStatus) und des Dokumenttitels zur neuen Namensgebung.

## **\[1.29.1\] \- 2024-05-22**

### **Optimiert**

* **Rauch-Begrenzung**: Die Anzahl der gleichzeitig aktiven smokeActive-Schornsteine wurde auf maximal 3 zufällig ausgewählte Gebäude begrenzt (Performance-Schonung).  
* **Partikel-Physik**: Die Aufstiegsgeschwindigkeit (vy) der Rauchpartikel wurde signifikant verringert, um einen ruhigeren Effekt zu erzielen.  
* **Lebensdauer**: Die decay-Rate der Rauchpartikel wurde angepasst, damit der Rauch sanfter verweht und transparenter ausfadet.

## **\[1.29.0\] \- 2024-05-22**

### **Hinzugefügt**

* **Rauch-System**: Implementierung der SmokeParticle-Klasse für Schornsteine an Wohnhäusern und Farmen.  
* **Prozedurale Felsen**: Ergänzung der Landschaftsgenerierung durch die Rock-Klasse mit individuellen Polygon-Punkten und Lichtkanten.  
* **Hohes Gras**: Einführung von Tall Grass in den Arbeitsbereichen der Farmer zur besseren visuellen Zonen-Trennung.

### **Geändert**

* **Gebäude-Logik**: Erweiterung der Village-Klasse zur Unterscheidung zwischen Wohngebäuden (mit Schornstein) und sakralen Bauten wie der Kirche (ohne Schornstein-Logik).

## **\[1.28.1\] \- Basis-Version**

### **Features**

* Dynamischer Tag-Nacht-Zyklus via SKY\_PHASES und LERP-Interpolation.  
* Prozedurale Generierung von Bäumen (Tree), Tieren (Animal), Vögeln (Bird) und dem Waldpfad (ForestPath).  
* Dynamisches See-System (Lake) mit Rippel-Effekten und automatischer Schilf-Platzierung.  
* Parallax-Kameraführung für atmosphärische Tiefe.
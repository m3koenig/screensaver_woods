# **Changelog \- Screensaver Woods**

Alle wichtigen Änderungen an diesem Projekt werden in dieser Datei dokumentiert. Das Projekt nutzt Semantic Versioning (SemVer).

## **\[1.35.0\] \- 2024-05-26**

### **Verbessert**

* **Vogel-Physiologie**: Alle Vögel verfügen nun über einen visuell abgesetzten, goldfarbenen Schnabel für mehr Detailreichtum.  
* **Flugpfad-Glättung**: Die Wellenbewegung (Undulation) des Spechts wurde stabilisiert und die Frequenz reduziert, um unnatürliche "Zick-Zack"-Effekte zu eliminieren.  
* **Farmer-Interaktion**: Die Animationsgeschwindigkeit des Winkens wurde auf ein natürliches Minimum reduziert, um eine ruhige, dörfliche Atmosphäre zu unterstützen.

## **\[1.34.0\] \- 2024-05-26**

### **Verbessert**

* **Flügel-Rendering**: Die Flügel-Geometrie der Vögel wurde von einfachen Linien auf volumetrische Polygone (Quadratic Curves) umgestellt. Die Flügel wirken dadurch massiver und realistischer.  
* **Fachwerk-Detailgrad**: Die Village-Klasse generiert nun detaillierte Holzstreben (K-Streben und vertikale Balken) auf den Hauswänden der Wohnhäuser.  
* **Animations-Timing**: Erste Verlangsamung der Winken-Animation der Bauern für bessere Erkennbarkeit.

## **\[1.33.0\] \- 2024-05-25**

### **Optimiert**

* **Akteur-Sichtbarkeit**: Die Transparenz-Logik für Bauern und Hunde wurde korrigiert. Der minimale Alpha-Wert wurde angehoben, sodass die Figuren auch in der Tiefe nicht mehr zu stark ausfaden.  
* **Reiter-Skalierung**: Die Grafik des Reiters (Rider) wurde um ca. 40% vergrößert, um eine bessere visuelle Präsenz auf dem Waldpfad zu erzielen.

### **Verbessert**

* **Dorf-Architektur**: Überarbeitung der Village-Klasse. Einführung von Giebelhäusern, markanteren Türmen und farblich abgesetzten Dächern für ein schöneres Stadtbild.

## **\[1.32.0\] \- 2024-05-25**

### **Hinzugefügt**

* **Hunde-KI-Spezialaktionen**: Hunde führen nun alle 1 bis 2,5 Minuten zufällige Aktionen aus (Sitz, Platz/Liegen oder Stehen).  
* **Interaktive Bauern**: Bauern prüfen nun auf die Anwesenheit eines Reiters. Bei Sichtung besteht eine 50%-Chance, dass der Bauer dem Reiter zuwinkt.

### **Verbessert**

* **Grafische Lebendigkeit**:  
  * **Steine**: Die Farbpalette der Felsen wurde aufgehellt und mit einer Lichtkante versehen.  
  * **Vögel**: Die Flügel wurden deutlicher vom Körper abgesetzt und die Fluggeschwindigkeit wurde verringert.  
  * **Hunde**: Implementierung einer Blickrichtung; Hunde drehen sich nun visuell (scaleX) in ihre jeweilige Laufrichtung.

## **\[1.31.0\] \- 2024-05-24**

### **Verbessert**

* **Intelligente Welt-Generierung**:  
  * **Kollisionsvermeidung**: Der Platzierungs-Algorithmus für den See wurde überarbeitet. Er prüft nun aktiv auf Überschneidungen mit dem ForestPath und hält einen Sicherheitsabstand zum Dorf (Village) ein.  
* **Tiefensortierung (Z-Indexing)**:  
  * Implementierung eines stabilen Sortier-Algorithmus (all.sort), der alle Entitäten präzise voreinander oder hintereinander rendert.  
  * Besondere Berücksichtigung finden nun fliegende Objekte wie Libellen (Dragonfly) und Vögel (Bird), die korrekt über den jeweiligen Boden-Layern gezeichnet werden.

## **\[1.30.1\] \- 2024-05-23**

### **Optimiert**

* **Atmosphärische Beleuchtung für Hunde**: Die Hunde nutzen nun denselben Tiefen- und Licht-Algorithmus wie die Umgebungsobjekte.  
* **Lokalisierte Farmer-KI**: Der Arbeitsradius der Farmer wurde auf den Bereich ihrer jeweiligen Gehöfte begrenzt.

## **\[1.30.0\] \- 2024-05-23**

### **Hinzugefügt**

* **Hunde-System**: Einführung von Hunden auf den Farmen mit eigenständiger KI (Zustände: SITTING, WALKING, IDLE).  
* **Farmer-Tagesabläufe**: Farmer folgen einem zeitabhängigen Zyklus (Warten am Haus, Weg zum Feld, Arbeit, Heimkehr).  
* **Erweiterte Tier-KI**: Rehe besitzen nun eine verfeinerte Pausen-Logik mit Grasen-Animationen.

## **\[1.29.2\] \- 2024-05-22**

### **Geändert**

* **Rebranding**: Das Projekt wurde offiziell in **Screensaver Woods** umbenannt.

## **\[1.29.1\] \- 2024-05-22**

### **Optimiert**

* **Rauch-Begrenzung**: Die Anzahl der gleichzeitig aktiven Schornsteine wurde auf maximal 3 begrenzt.  
* **Partikel-Physik**: Verlangsamung der Rauchpartikel für einen ruhigeren Effekt.

## **\[1.29.0\] \- 2024-05-22**

### **Hinzugefügt**

* **Rauch-System**: Implementierung der SmokeParticle-Klasse für Schornsteine.  
* **Prozedurale Felsen**: Ergänzung der Landschaftsgenerierung durch die Rock-Klasse.  
* **Hohes Gras**: Einführung von Tall Grass in den Arbeitsbereichen der Farmer.

## **\[1.28.1\] \- Basis-Version**

### **Features**

* Dynamischer Tag-Nacht-Zyklus via SKY\_PHASES.  
* Prozedurale Generierung von Bäumen, Tieren, Vögeln und Waldpfad.  
* Dynamisches See-System mit Rippel-Effekten.  
* Parallax-Kameraführung.
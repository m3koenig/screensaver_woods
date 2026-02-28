# **Changelog \- Screensaver Woods**

Alle wichtigen Änderungen an diesem Projekt werden in dieser Datei dokumentiert. Das Projekt nutzt Semantic Versioning (SemVer).

## **\[1.30.1\] \- 2024-05-23**

### **Optimiert**

* **Atmosphärische Beleuchtung für Hunde**: Die Hunde nutzen nun denselben Tiefen- und Licht-Algorithmus wie die Umgebungsobjekte (Bäume/Gräser). Sie fügen sich dadurch bei Nebel oder Dunkelheit natürlicher in die Landschaft ein.  
* **Lokalisierte Farmer-KI**: Der Arbeitsradius der Farmer wurde auf den Bereich ihrer jeweiligen Gehöfte begrenzt, um eine logischere Zuordnung von Wohn- und Arbeitsplatz zu gewährleisten.

## **\[1.30.0\] \- 2024-05-23**

### **Hinzugefügt**

* **Hunde-System**: Einführung von Hunden auf den Farmen mit eigenständiger KI (Zustände: Sitzen, Laufen, IDLE) und Animationen für wedelnde Schwänze.  
* **Farmer-Tagesabläufe**: Farmer sind nicht mehr statisch, sondern folgen einem zeitabhängigen Zyklus (Warten am Haus, Weg zum Feld, Arbeit mit Werkzeug-Animation, Heimkehr am Abend).  
* **Erweiterte Tier-KI**: Rehe besitzen nun eine verfeinerte Pausen-Logik mit Grasing-Animationen für ein realistischeres Verhalten.

### **Optimiert**

* **Z-Sorting (Tiefenebenen)**: Die Libellen wurden in das globale Sortierungssystem integriert. Sie werden nun korrekt hinter Bäumen und anderen Vordergrundobjekten gerendert, bleiben aber über dem Boden-Layer.

## **\[1.29.2\] \- 2024-05-22**

### **Geändert**

* **Rebranding**: Das Projekt wurde offiziell von "Woods Engine" in **Screensaver Woods** umbenannt.  
* Update der UI-Statusanzeige und des Dokumenttitels zur neuen Namensgebung.

## **\[1.29.1\] \- 2024-05-22**

### **Optimiert**

* **Rauch-Begrenzung**: Die Anzahl der gleichzeitig rauchenden Schornsteine wurde auf maximal 3 zufällig ausgewählte Gebäude begrenzt, um die visuelle Überladung zu reduzieren.  
* **Partikel-Physik**: Die Aufstiegsgeschwindigkeit der Rauchpartikel wurde signifikant verringert, um einen ruhigeren, atmosphärischeren Effekt zu erzielen.  
* **Lebensdauer**: Die Zerfallsrate der Rauchpartikel wurde angepasst, damit der Rauch sanfter verweht.

## **\[1.29.0\] \- 2024-05-22**

### **Hinzugefügt**

* **Rauch-System**: Implementierung eines Partikelsystems für Schornsteine an Wohnhäusern und Farmen.  
* **Prozedurale Felsen**: Ergänzung der Landschaftsgenerierung durch Steine mit individuellen Lichtkanten.  
* **Hohes Gras**: Einführung von "Tall Grass" in den Arbeitsbereichen der Farmer zur besseren visuellen Differenzierung der Zonen.

### **Geändert**

* Erweiterung der Gebäude-Logik zur Unterscheidung zwischen Wohngebäuden (mit Schornstein) und sakralen Bauten wie der Kirche (ohne Schornstein).

## **\[1.28.1\] \- Basis-Version**

* Initialer Stand der Woods Engine.  
* Dynamischer Tag-Nacht-Zyklus.  
* Prozedurale Generierung von Bäumen, Tieren, Vögeln und dem Waldpfad.  
* Dynamisches See-System mit Libellen und Wellen-Effekten.
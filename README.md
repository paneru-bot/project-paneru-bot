# Station Météo avec Arduino Uno

| | |
|---|---|
| `Author` | Curti Taner |

## Description

Ce projet consiste à concevoir une station météo compacte basée sur une carte Arduino Uno, capable de mesurer en temps réel la température et l'humidité ambiante à l'aide d'un capteur DHT11. Les données sont affichées en permanence sur un écran LCD 1602, permettant à l'utilisateur de consulter les conditions climatiques actuelles d'un simple coup d'œil. Le système effectue une nouvelle lecture toutes les deux secondes et met à jour l'affichage automatiquement. Un bouton poussoir permet de basculer entre deux modes d'affichage : le premier montre la température (en °C) et le second affiche le taux d'humidité (en %).

## Motivation

Ce projet a été choisi pour sa simplicité de réalisation tout en impliquant l'utilisation de plusieurs composants matériels essentiels : un capteur numérique, un écran LCD avec communication parallèle, et une interface utilisateur basique via bouton. Il permet de comprendre comment lire des données depuis un capteur, les traiter dans un microcontrôleur, et les présenter de manière claire sur un afficheur. La station météo constitue une application concrète et utile du quotidien, ce qui renforce l'intérêt pédagogique du projet.

## Architecture

```
[Capteur DHT11]
       |
       | Données (température + humidité)
       ↓
[Arduino Uno]
       |
       |──────────────→ [Écran LCD 1602]
       |                  (affichage des valeurs)
       |
       ←── [Bouton poussoir]
              (changement de mode d'affichage)
```

### Block diagram

[![Block Diagram](schematics/block_diagram.png)](schematics/block_diagram.png)

### Schematic

[![Schematic](schematics/kicad_schematic.png)](schematics/kicad_schematic.png)

### Components

| Dispositif | Utilisation | Prix estimé |
|---|---|---|
| Arduino Uno | Microcontrôleur principal | ~45 RON |
| Capteur DHT11 | Mesure de température et humidité | [5 RON](https://www.optimusdigital.ro/ro/senzori-senzori-de-temperatura/99-modul-senzor-de-temperatura-si-umiditate-dht11.html) |
| Écran LCD 1602 | Affichage des données | [15 RON](https://www.optimusdigital.ro/ro/optoelectronice-lcd-uri/2894-lcd-cu-interfata-i2c-si-backlight-albastru.html) |
| Potentiomètre 10kΩ | Réglage du contraste LCD | [2 RON](https://www.optimusdigital.ro/ro/componente-electronice-potentiometre/901-rezistor-variabil-10k.html) |
| Bouton poussoir | Changement de mode d'affichage | [1 RON](https://www.optimusdigital.ro/ro/butoane-i-comutatoare/1119-buton-6x6x6.html) |
| Résistance 10kΩ | Pull-down pour le bouton | [0.10 RON](https://www.optimusdigital.ro/ro/componente-electronice-rezistoare/859-rezistor-025w-10k.html) |
| Résistance 220Ω | Limitation de courant LCD | [0.10 RON](https://www.optimusdigital.ro/ro/componente-electronice-rezistoare/856-rezistor-025w-220.html) |
| Breadboard 830 points | Plaque de prototypage | [10 RON](https://www.optimusdigital.ro/ro/prototipare-breadboard-uri/8-breadboard-830-points.html) |
| Set fils de connexion | Connexions entre composants | [7 RON](https://www.optimusdigital.ro/ro/fire-fire-mufate/884-set-fire-tata-tata-40p-10-cm.html) |
| Câble USB | Alimentation et programmation | inclus avec Arduino |

### Libraries

| Bibliothèque | Description | Utilisation |
|---|---|---|
| [DHT sensor library](https://github.com/adafruit/DHT-sensor-library) | Bibliothèque Adafruit pour capteurs DHT11/DHT22 | Lecture de la température et de l'humidité depuis le DHT11 |
| [LiquidCrystal](https://www.arduino.cc/reference/en/libraries/liquidcrystal/) | Bibliothèque officielle Arduino pour écrans LCD | Contrôle de l'affichage LCD 1602 en mode 4 bits |

## Log

### Week 6 - 12 May

### Week 7 - 19 May

### Week 20 - 26 May

## Reference links

[Tutoriel DHT11 avec Arduino](https://www.youtube.com/watch?v=OogldLc9uYc)

[Documentation capteur DHT11](https://www.mouser.com/datasheet/2/758/DHT11-Technical-Data-Sheet-Translated-Version-1143054.pdf)

[Arduino LiquidCrystal reference](https://www.arduino.cc/reference/en/libraries/liquidcrystal/)

[Arduino Project Hub - Weather Station](https://projecthub.arduino.cc/search?q=weather+station)

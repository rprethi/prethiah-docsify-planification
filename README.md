# Planification Luminatura

## Synoptique
```mermaid

graph TD;

    %% Composants
        Ordinateur[Contrôle central - Ordinateur]
        DMX[USB DMX]
        Lumiere[Lumière]
        Ampoule[Ampoule]
        CarteSon[Carte de son]
        HautParleur[Haut-parleur]
        SortieAudio[Sortie audio]
        PlaqueMetalique[Plaque métallique]
        CapteurSensing[Capteur sensing]

    %% Emplacements
    subgraph Rideaux
        Ordinateur
    end

    subgraph Plafond
        DMX
        Lumiere
        Ampoule
    end

    subgraph Sol
        CarteSon
        HautParleur
        SortieAudio
    end

    subgraph Studio
        PlaqueMetalique
        CapteurSensing
    end

    %% Connexions
    Ordinateur -->|USB| DMX
    Ordinateur -->|USB| CarteSon
    Ordinateur -->|Signal| PlaqueMetalique
    PlaqueMetalique -->|Signal| CapteurSensing
    DMX -->|Câble DMX| Lumiere
    Lumiere -->|Câble électrique| Ampoule
    CarteSon -->|Câble audio| HautParleur
    HautParleur -->|Câble audio| SortieAudio

```

## Scénarimage
---
![scenario-01](https://github.com/user-attachments/assets/d41d4dce-4b6a-4922-97ff-12884e7b8079) ![scenario-02](https://github.com/user-attachments/assets/d72a3d0d-e8c1-4bf6-8a8d-80d27c868063)
![scenario-03](https://github.com/user-attachments/assets/eae70c4e-f6a7-4944-8863-c7126459fb40) ![scenario-04](https://github.com/user-attachments/assets/d50373c7-be7c-4c39-bb6c-e9024a0f8159)
![scenario-04a](https://github.com/user-attachments/assets/2e0a0d2e-1b04-467d-8c49-f1acf2bee7f8) ![scenario-04b](https://github.com/user-attachments/assets/82d4bab8-3c75-4102-bcc8-095d7487d53e)
![scenario-05](https://github.com/user-attachments/assets/90535f8f-8f83-4c30-8807-055a73e752f0) ![scenario-06](https://github.com/user-attachments/assets/fcc12c72-bfbe-4a13-90ab-e313f6e03afa)

## Devis Technique
---
### Équipements et matériaux
---
### Équipement fourni par l’artiste

- 15 Vignes Artificielles
- 10 Ampoules LED 
- 1 Plaque métallique 
- 10 Lanternes en polycarbonate
- Régulateur de tension
- Fil de cuivre ou d'acier

#### Capteurs et Évaluation

| Capteur de type «sensing capacitif»                       | Composants                   |
| --------------------------------------------------------- | ---------------------------- |
| Cartes d'évaluation pour microcontrôleurs embarqués (MCU) | Arduino A000066              |
| Résistances traversantes                                  | YAGEO CFR-25JB-52-3M6        |
| Cartes d'évaluation de capteurs                           | Adafruit Industries LLC 1374 |

#### Support en Métal

| Support en métal pour la plaque métallique | Composants                          |
| ------------------------------------------ | ----------------------------------- |
| 1 Tube en acier ou en aluminium            | Structure principale du « stand »   |
| 1 Base plate                               | Assurer la stabilité du « stand »   |
| Vis et boulons                             | Assembler et garantir la durabilité |

### Équipement fourni par le cégep

- Câbles (HDMI, Ethernet, audio)
- Éléments de fixation
- Fils de prototypage
- 1 Ordinateur (gestion des interactions en temps réel)
- 2 Haut-parleurs

### Logiciels
---
### Logiciels fournis par l’artiste
  
| Logiciel | Technique                                                                |
| -------- | ------------------------------------------------------------------------ |
| Reaper   | Montage sonore (base)                                                    |
| Arduino  | Capteur de type «sensing capacitif» et connecter les composants ensemble |

### Logiciels fournis par le cégep

| Logiciel  | Technique                                                 |
| --------- | --------------------------------------------------------- |
| Pure Data | Modifier des paramètres audio en réponse à des événements |
| QLC+      | Création des scènes lumineuses                            |
| Plugdata  | Modifier la couleur des lumières                          |

### Mise en réseau et de communication
---
### Fournis par le cégep

| Système de communication | Logiciel | Interaction         |
| ------------------------ | -------- | ------------------- |
| Protocole MIDI           | LoopMidi | QLC+ et Plugdata    |
| Protocole DMX            | QLC+     | Lumiere et logiciel |

### Allocation des responsabilités
#### Préparation des espaces

* Électricité
* Connexion réseau
* Espace pour le montage des dispositifs (extérieur du cyclorama)

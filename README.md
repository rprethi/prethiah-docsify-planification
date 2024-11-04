# Planification Luminatura

***Luminatura***, où la lumière et la nature s'entrelacent pour éclairer l'esprit à travers la magie des lanternes.

## Concept
---

***Luminatura*** est une installation immersive alliant art et technologie, où des lanternes illuminent votre parcours et des vignes décorent l'espace, créant une atmosphère accueillante. En touchant une plaque métallique, la chaleur corporelle de l'utilisateur déclenche une réponse lumineuse et sonore, illustrant le potentiel de transformation que chacun détient sur son environnement.

### Mise en contexte

À l'entrée de l'installation, le visiteur est accueilli par la douce lumière des lanternes suspendues et les vignes décoratives qui créent une ambiance de tranquillité.

En touchant la plaque, le visiteur déclenche une lumière douce et chaleureuse, accompagnée de sons apaisants de la nature. Ce moment intime lui permet de réfléchir à ses propres expériences de transformation et d’éveiller des émotions profondes, soulignant le pouvoir de l'art et de la technologie pour toucher l’âme humaine.

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
![scenario-01](https://github.com/user-attachments/assets/9aede9dd-d5b6-4808-b45a-95dfe7e4c233)
![scenario-02](https://github.com/user-attachments/assets/04ce7d77-a2de-42be-998f-3d444e2fe6f4)
![scenario-03](https://github.com/user-attachments/assets/d1291c5d-6dbb-418e-a073-022658baba4a)
![scenario-04](https://github.com/user-attachments/assets/9f59cde4-f6aa-4ddd-9897-40f5cf599bc8)
![scenario-04a](https://github.com/user-attachments/assets/2a518ee8-364f-4ba6-b51e-d1ad4614ee29)
![scenario-04b](https://github.com/user-attachments/assets/5b174ecf-6f65-491b-a74e-7dd27ceb3d23)
![scenario-05](https://github.com/user-attachments/assets/43d34f12-878a-479e-88b4-d0d0daf2f5f9)
![scenario-06](https://github.com/user-attachments/assets/5a4d3004-954a-4236-8454-8a070206b60d)

## Plantation
---
![plantation](https://github.com/user-attachments/assets/5cff1cb5-a3b5-452f-9c55-9d30dc855938)

## Simulation
---


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
---
#### Préparation des espaces

* Électricité
* Connexion réseau
* Espace pour le montage des dispositifs (extérieur du cyclorama)

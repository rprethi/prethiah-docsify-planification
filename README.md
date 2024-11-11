# Planification Luminatura
---

***Luminatura***, où la lumière et la nature s'entrelacent pour éclairer l'esprit à travers la magie des lanternes.

## Concept
---

***Luminatura*** est une installation immersive alliant art et technologie, où des lanternes illuminent votre parcours et des vignes décorent l'espace, créant une atmosphère accueillante. En touchant une plaque métallique, le capteur de capacitance détecte la conductibilite de la main de l'utilisateur déclenche une réponse lumineuse et sonore, illustrant le potentiel de transformation que chacun détient sur son environnement.

### Mise en contexte

À l'entrée de l'installation, le visiteur est accueilli par la douce lumière des lanternes suspendues et les vignes décoratives qui créent une ambiance de tranquillité.

En touchant la plaque, le visiteur déclenche une lumière douce et chaleureuse, accompagnée de sons apaisants de la nature. Ce moment intime lui permet de réfléchir à ses propres expériences de transformation et d’éveiller des émotions profondes, soulignant le pouvoir de l'art et de la technologie pour toucher l'âme humaine.

## Synoptique
---
```mermaid

graph TD;

    %% Composants
        Ordinateur[Contrôle central - Ordinateur]
        DMX[USB DMX]
        Lumiere[Lumière]
        Ampoule[Ampoules]
        CarteSon[Carte de son]
        HautParleur[Haut-parleurs]
        SortieAudio[Sortie audio]
        PlaqueMetalique[Plaque métallique]
        CapteurSensing[Capteur sensing]

    %% Emplacements
    subgraph Derrière les rideaux
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
![scenario-01](https://github.com/user-attachments/assets/a54621fa-502e-4c3b-9c82-e8a2c6e8e206)
![scenario-02](https://github.com/user-attachments/assets/0d2f6dec-a817-47af-9a71-5d9ce60fcc40)
![scenario-03](https://github.com/user-attachments/assets/def078e0-8fc6-487d-962b-027fd4cad235)
![scenario-04](https://github.com/user-attachments/assets/701b852c-0cbf-4c8f-bbe6-f0b9e9da430c)
![scenario-04a](https://github.com/user-attachments/assets/c9a0209f-8149-4012-a36e-ee601884a354)
![scenario-04b](https://github.com/user-attachments/assets/b9cea884-b4b6-4ebc-96ee-8ec67fb17bec)
![scenario-05](https://github.com/user-attachments/assets/a62c15fd-c0d2-43dd-8de9-72c86e65d8b7)
![scenario-06](https://github.com/user-attachments/assets/000ac2a7-be45-46e3-93d9-22949cdac398)

## Plantation
---
![schema-plantation-01](https://github.com/user-attachments/assets/66ec237c-0b91-4a3f-b786-73da600bc25c)
![schema-plantation-02](https://github.com/user-attachments/assets/4d6c2dc3-6f01-41d4-8944-909f7c4e9e41)

## Simulation
---
![rendu3d-01](https://github.com/user-attachments/assets/f430819c-2b87-4be4-9444-83088abfe75a)
![rendu3d-02](https://github.com/user-attachments/assets/65222d73-c413-46ed-921c-93ff0e1e6542)

## Devis Technique
---
### Équipements et matériaux
---
### Équipements fournis par l’artiste

- 15 vignes artificielles
- 10 ampoules LED 
- 1 plaque métallique 
- 10 lanternes en polycarbonate
- Régulateur de tension
- Fil de cuivre ou d'acier
  
#### Capteurs et évaluation

| Capteur de type « sensing capacitif »                    | Composants                   |
| -------------------------------------------------------- | ---------------------------- |
| Carte d'évaluation pour microcontrôleurs embarqués (MCU) | Arduino A000066              |
| Résistances traversantes                                 | YAGEO CFR-25JB-52-3M6        |
| Carte d'évaluation de capteurs                           | Adafruit Industries LLC 1374 |

#### Support en métal

| Support en métal pour la plaque métallique | Composants                        |
| ------------------------------------------ | --------------------------------- |
| 1 tube en acier ou en aluminium            | Structure principale du « stand » |
| 1 base plate                               | Assurer la stabilité du « stand » |
| Vis et boulons                             | Assemblage et durabilité          |

### Équipements fournis par le cégep

- Câbles (HDMI, Ethernet, audio)
- Éléments de fixation
- Fils de prototypage
- 1 ordinateur (gestion des interactions en temps réel)
- 2 haut-parleurs

### Logiciels 

---
### Logiciels fournis par l’artiste
  
| Logiciel | Technique                                                         |
| -------- | ----------------------------------------------------------------- |
| Reaper   | Montage sonore (de base)                                          |
| Arduino  | Capteur de type « sensing capacitif » et connexion des composants |

### Logiciels fournis par le cégep

| Logiciel  | Technique                                                     |
| --------- | ------------------------------------------------------------- |
| Pure Data | Modification des paramètres audio en réponse à des événements |
| QLC+      | Création des scènes lumineuses                                |
| Plugdata  | Modification de la couleur des lumières                       |

### Mise en réseau et communication

---
### Fourni par le cégep

| Système de communication | Logiciel | Interaction         |
| ------------------------ | -------- | ------------------- |
| Protocole MIDI           | LoopMidi | QLC+ et Plugdata    |
| Protocole DMX            | QLC+     | Lumière et logiciel |

### Répartition des responsabilités
---
#### Préparation des espaces

* Électricité
* Connexion réseau
* Espace pour le montage des dispositifs (extérieur du cyclorama)

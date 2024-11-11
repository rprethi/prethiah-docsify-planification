# Planification Luminatura
---

***Luminatura***, où la lumière et la nature s'entrelacent pour éclairer l'esprit à travers la magie des lanternes.

## Concept
---

***Luminatura*** est une installation immersive alliant art et technologie, où des lanternes illuminent votre parcours et des vignes décorent l'espace, créant ainsi une atmosphère accueillante. En touchant une plaque métallique, le capteur capacitif détecte la conductivité des mains de l'utilisateur et déclenche une réponse lumineuse et sonore, illustrant le potentiel de transformation que chacun peut exercer sur son environnement.

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
    ArduinoA000066[Arduino A000066]

    %% Emplacements
    subgraph Caché des utilisateurs
        Ordinateur
    end

    subgraph Plafond
        DMX
        Lumiere
        Ampoule 
        CarteSon
        HautParleur
        SortieAudio
    end

    subgraph GrandStudio
        PlaqueMetalique
        ArduinoA000066
    end

    %% Connexions
    Ordinateur -->|USB| DMX
    Ordinateur --> CarteSon
    Ordinateur -.-> PlaqueMetalique
    PlaqueMetalique -->|Capteur de capacitance Adafruit Industries LLC 1374| ArduinoA000066
    ArduinoA000066 -->|Contrôle Lumière| Lumiere
    ArduinoA000066 -->|Contrôle Son| CarteSon
    DMX -->|Câble DMX| Lumiere
    Lumiere -->|Câble électrique| Ampoule
    CarteSon -->|Câble audio| HautParleur
    HautParleur -->|Câble audio| SortieAudio

```

## Scénarimage
---

![scenario-01](https://github.com/user-attachments/assets/e597c977-b1c5-4dfd-8b9c-83bfbe3e72b0)
![scenario-02](https://github.com/user-attachments/assets/ecc1e5af-1933-4973-9602-2ac58491bcbc)
![scenario-03](https://github.com/user-attachments/assets/f8774a51-9381-4b0a-98d5-d689ee50e82e)
![scenario-04](https://github.com/user-attachments/assets/a19fff93-4384-4fa9-9a9b-584257b17cc7)
![scenario-04a](https://github.com/user-attachments/assets/bf37e673-a302-4bf9-bcf9-1136d143d3d2)
![scenario-04b](https://github.com/user-attachments/assets/f0736406-3102-43ae-bf77-663714c9afeb)
![scenario-05](https://github.com/user-attachments/assets/fea4d88f-dbbd-4661-ba69-dd6fbaa159cb)
![scenario-06](https://github.com/user-attachments/assets/17ce3b5c-8e26-4f5f-9548-8fe42c1f8353)


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

- 15 vignes artificielles en plastique 
- 10 ampoules LED 
- 1 plaque acier inoxydable 
- 10 lanternes en polycarbonate
- Régulateur de tension
- Câbles en acier inoxydable
- Boucles avec embouts pour câble inoxydable
- Éléments de fixation
- Plaque ronde d'acier (épaisseur 1mm)
- Plaques isolantes 
  
#### Capteurs et évaluation

| Capteur de type « sensing capacitif »                    | Composants                   |
| -------------------------------------------------------- | ---------------------------- |
| Carte d'évaluation pour microcontrôleurs embarqués (MCU) | Arduino A000066              |
| Résistances traversantes                                 | YAGEO CFR-25JB-52-3M6        |
| Carte d'évaluation de capteurs                           | Adafruit Industries LLC 1374 |

#### Support en métal

| Support en métal pour la plaque métallique | Composants                        |
| ------------------------------------------ | --------------------------------- |
| 1 tube en acier                            | Structure principale du « stand » |
| 1 base plate                               | Assurer la stabilité du « stand » |
| Vis et boulons                             | Assemblage et durabilité          |

### Équipements fournis par le cégep

- Câbles (HDMI, Ethernet, audio)
- Fils de prototypage
- 1 ordinateur (gestion des interactions en temps réel)
- 2 haut-parleurs GENELEC 8040B

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

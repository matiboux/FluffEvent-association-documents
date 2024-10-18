# Diagramme des instances de l'Association

```mermaid
graph LR

AG{{"Assemblée Générale"}}

BU{{"Bureau"}}
BUA{{"Membres administratifs<br>(président, trésorier, etc.)<br>du Bureau"}}
BUM{{"Membres opérationnels<br>du Bureau"}}

CA{{"Conseil d'Administration"}}
CAP{{"Président du<br>Conseil d'Administration"}}
CAF{{"Membres fondateurs<br>(membres de droit du<br>Conseil d'Administration)"}}
CAM{{"Membres mandatés du<br>Conseil d'Administration"}}

Statuts([Statuts])
Reglement([Règlement Intérieur])

subgraph Docs[Documents]
  Statuts
  Reglement
end

subgraph BU[Bureau]
  BUA
  BUM
end

subgraph CA[Conseil d'Administration]
  CAP
  CAF
  CAM
end

AG -->|"Élit en son sein les<br>membres administratifs"| BUA
AG -->|"Peut révoquer<br>(vote majorité absolue)"| BUA

AG -->|"Valide la nomination"| CAM
AG -->|"Peut révoquer<br>(vote majorité absolue)"| CAM

CAF -->|"Élit aux sein des membres"| CAP
CAM -->|"Élit aux sein des membres"| CAP

CA -->|"Contrôle régulier de l'activité"| BU
CA -->|"Valide la nomination"| BUM
CA -->|"Peut révoquer un membre<br>(vote deux tiers)"| BUM

AG -->|"Vote les amendements"| Statuts
CA -->|"Vote les amendements"| Reglement

style AG fill:#600,color:#eee,stroke:#800,stroke-width:2px

style BU stroke:#369,stroke-width:2px
style BUA fill:#369,color:#eee,stroke:#48c,stroke-width:2px
style BUM fill:#369,color:#eee,stroke:#48c,stroke-width:2px

style CA stroke:#063,stroke-width:2px
style CAP fill:#396,color:#eee,stroke:#4c8,stroke-width:2px,stroke-dasharray: 5 5
style CAF fill:#c80,color:#eee,stroke:#fa0,stroke-width:2px
style CAM fill:#396,color:#eee,stroke:#4c8,stroke-width:2px

style Docs stroke:#333,stroke-width:2px
style Statuts fill:#333,color:#eee,stroke:#444,stroke-width:2px
style Reglement fill:#333,color:#eee,stroke:#444,stroke-width:2px
```

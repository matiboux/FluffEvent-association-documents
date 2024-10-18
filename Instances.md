# Diagramme des instances de l'Association

```mermaid
graph LR

AG{{"Assemblée Générale"}}

BU{{"Bureau"}}
BUP{{"Président du Bureau<br>(membre administratif)"}}
BUT{{"Trésorier du Bureau<br>(membre administratif)"}}
BUM{{"Membres opérationnels<br>du Bureau"}}

CA{{"Conseil d'Administration"}}
CAP{{"Président du CA"}}

Statuts([Statuts])
Reglement([Règlement Intérieur])

Fonda{{Membres fondateurs}}

AG -->|"Élit en son sein les<br>membres administratifs<br>(président, trésorier, etc.)"| BU
AG -->|"Peut révoquer un membre<br>(vote majorité absolue)"| BU
BU -->|"Membre administratif"| BUP
BU -->|"Membre administratif"| BUT
BU -->|"Membres opérationnels"| BUM

AG -->|"Vote les amendements"| Statuts
 
AG -->|"Valide les nominations<br>de membres mandatés"| CA
AG -->|"Peut révoquer<br>un membre mandaté<br>(vote majorité absolue)"| CA

CA -->|"Élit en son sein"| CAP

CA -->|"Valide les nominations<br>de membres opérationnels"| BU
CA -->|"Peut révoquer un membre<br>(vote deux tiers)"| BU

CA -->|"Vote les amendements"| Reglement

Fonda -->|"Membres de droit"| CA

style AG fill:#600,color:#eee,stroke:#800,stroke-width:2px
style BU fill:#036,color:#eee,stroke:#048,stroke-width:2px
style BUP fill:#369,color:#eee,stroke:#48c,stroke-width:2px,stroke-dasharray: 5 5
style BUT fill:#369,color:#eee,stroke:#48c,stroke-width:2px,stroke-dasharray: 5 5
style BUM fill:#369,color:#eee,stroke:#48c,stroke-width:2px,stroke-dasharray: 5 5
style CA fill:#063,color:#eee,stroke:#084,stroke-width:2px
style CAP fill:#396,color:#eee,stroke:#4c8,stroke-width:2px,stroke-dasharray: 5 5

style Statuts fill:#333,color:#eee,stroke:#444,stroke-width:2px
style Reglement fill:#333,color:#eee,stroke:#444,stroke-width:2px

style Fonda fill:#c80,color:#eee,stroke:#fa0,stroke-width:2px,stroke-dasharray: 5 5
```

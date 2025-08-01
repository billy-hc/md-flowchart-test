graph TD
    subgraph "IDENTIFICATION"
        A["<b>Records identified from databases</b><br/>(Scopus, Web of Science, Google Scholar)<br/>n = 1,250"]
    end

    subgraph "SCREENING"
        B["<b>Records after duplicates removed</b><br/>n = 1,040"]
        Rem1[("<b>Duplicate records removed</b><br/>n = 210")]
        C["<b>Records screened by title and abstract</b><br/>n = 1,040"]
        Rem2[("<b>Records excluded</b><br/>n = 890<br/><br/><i>Reason: Clearly irrelevant to study scope</i>")]
    end

    subgraph "ELIGIBILITY"
        D["<b>Full-text articles assessed for eligibility</b><br/>n = 150"]
    end

    %% Flow and Connections
    A --> B
    B --> Rem1
    B --> C
    C --> Rem2
    C --> D

    %% Styling
    style A fill:#e6f3ff,stroke:#4a90e2,stroke-width:2px
    style B fill:#e6f3ff,stroke:#4a90e2,stroke-width:2px
    style C fill:#e6f3ff,stroke:#4a90e2,stroke-width:2px
    style D fill:#e6f3ff,stroke:#4a90e2,stroke-width:2px
    style Rem1 fill:#ffe6e6,stroke:#d0021b,stroke-width:1px,stroke-dasharray: 5 5
    style Rem2 fill:#ffe6e6,stroke:#d0021b,stroke-width:1px,stroke-dasharray: 5 5

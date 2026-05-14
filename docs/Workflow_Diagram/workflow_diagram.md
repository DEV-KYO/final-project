graph LR
    %% Define Styles
    classDef mobile fill:#e1f5fe,stroke:#0288d1,stroke-width:2px;
    classDef internal fill:#fff3e0,stroke:#f57c00,stroke-width:2px;
    classDef cloud fill:#e8f5e9,stroke:#388e3c,stroke-width:2px;

    %% Nodes
    subgraph Client-Side Device
        A[User Mobile App UI/UX]:::mobile
        B[On-Device Controllers Location, Camera, Routing]:::internal
    end

    subgraph External Infrastructure
        C[(Valhalla Routing Engine Docker)]:::cloud
        D[CSULA Events Website]:::cloud
    end

    %% Connections
    A <-->|User Input / Audio & Haptic Feedback| B
    B <-->|JSON Route Request / Polyline Response| C
    B <-->|HTTP Fetch / HTML Event Data| D

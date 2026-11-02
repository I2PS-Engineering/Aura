# Aura

**Aura** is the central coordination system for I2PS Engineering's modular, distributed computing infrastructure. It is the new name for the project formerly known as **Atlas Nexus**.

## Architecture

```text
                  Logica Sofia
             (standalone AI system)
                        |
             Future controlled link
                        |
                       Aura
              (central coordination)
                        |
                   Orion Core
              (orchestration / routing)
                        |
                    Data Core
              (storage / persistence)

       Phoenix Core                Horizon Core
    (resilience / recovery)     (monitoring / optimization)
          \                          /
           Cross-cutting infrastructure services
```

| Component | Responsibility |
| --- | --- |
| **Aura** | Coordinates the cores, nodes, and shared infrastructure. |
| **Logica Sofia** | Independent AI system for reasoning, tools, and future integration with Aura. |
| **Orion Core** | Node coordination, communication, workload routing, and orchestration. |
| **Data Core** | Shared storage, datasets, and persistent services. |
| **Phoenix Core** | Hardware, software, and electrical resilience, monitoring, and recovery. |
| **Horizon Core** | Resource telemetry, performance analysis, and optimization. |

These are **logical responsibilities**, not a requirement for one physical machine per core. Phoenix and Horizon operate across the infrastructure rather than as stages in the Orion–Data path.

## Nodes and infrastructure

- **Administration/control:** Management access to the infrastructure; not tied to a permanent inference machine.
- **Linux compute workers:** Modular hosts for workloads, experiments, and future AI inference.
- **Storage hosts:** Persistent services and data capacity, including planned use of server hardware.
- **Networking:** LAN-connected workers, with WLAN support where configured; stable addressing and centralized management are being developed.
- **Power and recovery:** UPS/solar-backed power work and planned Phoenix hardware monitoring.

## Project status

The architecture is defined and hardware is being validated incrementally. A Linux rack worker has undergone sustained benchmarking. Distributed scheduling, automated failover, full cross-core coordination, and Logica Sofia integration are **planned or under development**, not claimed as production-ready.

Kubernetes may be introduced where useful; it is **not** a prerequisite for Aura.

---

**Built by I2PS Engineering.**

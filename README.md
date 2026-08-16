# Industrial Digital Twin: OPC UA and MQTT Performance Evaluation

## Overview

This project develops a software-based digital twin framework for evaluating communication performance in Industrial Internet of Things (IIoT) systems.

The framework simulates an industrial environment and compares two widely used communication technologies:

* OPC UA
* MQTT

The objective is to investigate how these protocols perform under different operating conditions, including variations in message frequency, payload size, number of simulated devices, and network conditions.

## Research Objectives

This project aims to:

1. Develop a software-based digital twin representing a simplified industrial system.
2. Implement communication using both OPC UA and MQTT.
3. Evaluate communication performance using measurable metrics.
4. Investigate the impact of workload and system scale on protocol performance.
5. Develop a reproducible experimental framework that does not require physical industrial hardware.

## Proposed Metrics

The experimental evaluation may include:

* End-to-end latency
* Throughput
* Message delivery reliability
* Scalability
* CPU utilization
* Memory utilization

The final set of metrics and experiments will be refined following a detailed literature review.

## Proposed Architecture

```text
                ┌───────────────────────┐
                │  Virtual Industrial   │
                │        System         │
                │                       │
                │ Sensors / Machines    │
                └───────────┬───────────┘
                            │
                     Simulated Data
                            │
              ┌─────────────┴─────────────┐
              │                           │
              ▼                           ▼
        ┌───────────┐               ┌───────────┐
        │  OPC UA   │               │   MQTT    │
        │  Stack    │               │  Broker   │
        └─────┬─────┘               └─────┬─────┘
              │                           │
              └─────────────┬─────────────┘
                            │
                            ▼
                  ┌─────────────────┐
                  │  Digital Twin   │
                  │  State Manager  │
                  └────────┬────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │ Performance &   │
                  │ Resource        │
                  │ Monitoring      │
                  └─────────────────┘
```

## Project Structure

```text
.
├── src/
│   ├── digital_twin/    # Virtual industrial system and state models
│   ├── mqtt/            # MQTT implementation
│   ├── opcua/           # OPC UA implementation
│   └── common/          # Shared utilities
├── experiments/         # Experimental configurations and scripts
├── analysis/            # Data analysis and visualization
├── data/                # Experimental datasets
├── figures/             # Generated figures
└── docs/                # Project documentation
```

## Technology Stack

The project is expected to use:

* Python
* MQTT
* Mosquitto
* OPC UA
* Docker
* Wireshark
* Pandas
* Matplotlib

The final technology stack may evolve as the experimental methodology is refined.

## Current Status

**Project stage:** Initial setup and literature review.

Current activities:

* [x] Define initial research direction
* [x] Draft preliminary abstract
* [x] Set up Overleaf project
* [x] Create GitHub repository
* [ ] Conduct literature review
* [ ] Identify research gap
* [ ] Define experimental methodology
* [ ] Implement virtual industrial system
* [ ] Implement MQTT communication
* [ ] Implement OPC UA communication
* [ ] Conduct experiments
* [ ] Analyze results
* [ ] Prepare manuscript

## Reproducibility

The long-term goal of this repository is to provide a reproducible software-based experimental environment for evaluating industrial communication protocols in a digital-twin context.

## License

This project is released under the MIT License.

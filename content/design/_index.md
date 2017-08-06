+++
title= "Design"
date= 2017-07-30T16:17:49-04:00
description = "How does it work?"
draft = false
weight = 2
+++

## Backend

[Coner Core Service](https://github.com/caeos/coner-core) encapsulates the core  logic and data storage duties, exposing this functionality via a REST API.

## UI

### Operator UI

Coner will supply an Operator UI where workers can perform their tasks on screens tailored to purpose.

### Other UIs

Possibilities abound for other UIs to leverage the Core Service and present the data to users in awesome ways. Coner would like to supply these also, but these are a lower priority compared to the Operator UI.

- Instant Results Web/Mobile App
- Registration Kiosk
- Standings Kiosk

## Bot

Bots perform a simple, repetitive task.

### Hardware Timer Connector

The Hardware Timer Connector will receive timing signals from your club's dedicated timing hardware and forward them to the Core Service, which will then attach them to the appropriate run automatically.

### Other Bots

Possibilities abound for bots to perform simple, repetitive tasks involving the Core Service.

- Barcode Scanner
- Start/Finish Photo Capture

## Graph

{{<mermaid align="center">}}
graph LR;
    subgraph Backend
        CS[Core Service]
    end
    subgraph UI
        OUI[Operator] --- CS
        IRUI[Instant Results] --- CS
        RKUI[Registration Kiosk] --- CS
        SKUI[Standings Kiosk] --- CS
    end
    subgraph Bots
        HTCB[Hardware Timer Connector] --- CS
        BCSB[Barcode Scanner] --- CS
        SFPCB[Start/Finish Photo Capture] --- CS
    end
{{< /mermaid >}}

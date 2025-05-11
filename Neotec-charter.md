# Charter for Neotec (Network Operations in Telco Cloud) 
 
## Background and Motivation

The Neotec initiative aims to define standardized, underlay-agnostic interfaces—built on top of IETF YANG models—that can be consumed by the requesters of cloud side (e.g., cloud orchestrator or cloud manager). These interfaces enable dynamic coordination between network service orchestrator and cloud infrastructure, allowing the network to adapt in real-time to the scaling and shifting demands of cloud-hosted services, to expose information that could be relevant for cloud operation, etc. 
Telecom operators increasingly rely on edge cloud infrastructure to deliver latency-sensitive and resource-intensive services closer to end users. These edge sites often have more constrained capacity than centralized data centers. However, despite often being managed by the same operator, cloud and network systems are often operated in silos, leading to poor visibility and delayed response to changes. Neotec addresses this challenge by transforming network and service models into APIs that enable cloud service scaling events and queries to be tranlated into actionable network control inputs. This approach enables the network to dynamically respond to changes in service instance placement, scale-in/out events, or application locality shifts, ensuring guaranteed bandwidth, latency, and reliability for services spanning multiple cloud sites.

## Goals and Scope
The Neotec initiative focuses on enabling cloud-aware network operations and network-aware cloud decisions by developing underlay-agnostic abstractions and interfaces that allow cloud orchestrators—such as Kubernetes—to interact with the network in a standardized, intent-driven manner. While existing IETF-developed YANG models (e.g., L2SM, L3SM, L2NM, L3NM) are tied to specific technologies or service types (e.g., L3VPN, L2VPN), Neotec aims to define a technology-neutral interface layer that exposes essential network behaviors and capabilities—such as connectivity, available bandwidth, latency, and path diversity—without requiring the cloud orchestrator to understand the underlying network implementation. Based on developing underlay-agnostic abstractions and interfaces, Neotec will walk through a set of models and assess whether they can address the needs of network cloud coordination. As network operators often rely on equipment, controllers, and network service orchestrators from multiple vendors, standardized and interoperable solutions are essential for the network management and operation to be cloud-aware. 

## Work Items
Neotec will initially focus on the following deliverables:
* Defining abstraction models and APIs that expose dynamic network characteristics (e.g., telemetry, service path metrics, ingress/egress status, and topological information, etc.) in a way that is usable by cloud-native systems for service placement, scaling, and path optimization.

* Designing a extensible shim layer that bridges cloud telemetry and orchestration systems (e.g., Kubernetes, OpenStack, Azure Stack) with existing IETF network models, enabling translation of cloud-scale events (e.g., service up/down, resource scaling) into actionable network control inputs.

* Develop YANG models to provide network controllers with dynamic service instance status, resulting in dynamic network adjustments—including UCMP policy updates and adaptive load balancing—whenever cloud services scale up or down. These updates allow the network to seamlessly accommodate changes without requiring detailed visibility into internal cloud structures.

* Contributing to the YANG2API effort by specifying the semantic and behavioral constructs needed to make IETF YANG models practically consumable via open APIs (e.g., REST, gRPC) in cloud-native environments. 


Neotec will also serve as a platform for the community to exchange requirements, challenges, and experiences related to network management and operation for cloud-based services.


## Out of Scope
It should be noted that Neotec focuses on addressing the network issues, not that of cloud scheduling or management issues. It does not handle service instance placement within cloud environments. Instead, it focuses on providing relevant cloud metrics to network for optimized network performance. It does not aim to develop an orchestrator production system either.

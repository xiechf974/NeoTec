# Charter for Neotec (Network Operations in Telco Cloud) 
 
## Background and Motivation
Telecom operators increasingly rely on edge cloud infrastructure to deliver latency-sensitive and resource-intensive services closer to end users. These edge sites often have more constrained capacity than centralized data centers. However, despite often being managed by the same operator, cloud and network systems are often operated in silos, leading to poor visibility and delayed response to changes. During the past lots of network and service models have been produced, but the applicability of these abstractions to accommodate network cloud coordination cases and constraints is seldomly assessed. Neotec addresses this challenge by defining standardized, underlay-agnostic API interfaces—built on top of IETF YANG models—that can be consumed by the requesters of cloud side (e.g., cloud orchestrator or cloud manager). These interfaces enables the network to dynamically respond to changes in service instance placement, scale-in/out events, or application locality shifts, ensuring guaranteed bandwidth, latency, and reliability for services spanning multiple cloud sites. Based on developing underlay-agnostic abstractions and interfaces, Neotec will walk through a set of models and assess whether they can address the needs of network cloud coordination.

## Goals and Scope
The Neotec initiative focuses on enabling cloud-aware network operations and network-aware cloud decisions by developing underlay-agnostic abstractions and interfaces that allow cloud orchestrators—such as Kubernetes—to interact with the network in a standardized, intent-driven manner. While existing IETF-developed YANG models (e.g., L2SM, L3SM, L2NM, L3NM) are tied to specific technologies or service types (e.g., L3VPN, L2VPN), Neotec aims to define a technology-neutral interface layer that exposes essential network behaviors and capabilities—such as connectivity, available bandwidth, latency, and path diversity—without requiring the cloud orchestrator to understand the underlying network implementation. As network operators often rely on equipment, controllers, and network service orchestrators from multiple vendors, cloud infrastructure is usualy provided by multiple cloud vendors, standardized and interoperable solutions are essential for the network management and operation to be cloud-aware. 

## Work Items
Neotec will initially focus on the following deliverables:
* Defining abstraction models and APIs that expose dynamic network characteristics (e.g., telemetry, service path metrics, ingress/egress status, and topological information, etc.) in a way that is usable by cloud-native systems for service placement and scaling.

* Designing an extensible shim layer that bridges cloud telemetry and orchestration systems (e.g., Kubernetes, OpenStack, Azure Stack) with existing IETF network models, enabling translation of cloud-scale events (e.g., service up/down, resource scaling) into actionable network control inputs.

* Develop YANG models to provide network controllers with cloud service instance status, dynamic adjustment to network connections and traffic steering policies—whenever cloud services scale up or down. These updates allow the network to seamlessly accommodate changes without requiring detailed visibility into internal cloud structures.

* Contributing to the YANG2API effort by specifying the semantic and behavioral constructs needed to make IETF YANG models practically consumable via open APIs (e.g., REST, gRPC) in cloud-native environments. 

Neotec will also serve as a platform for the community to exchange requirements, challenges, and experiences related to network management and operation for cloud-based services.


## Out of Scope
It should be noted that Neotec focuses on addressing the network issues, not that of cloud scheduling or management issues. It does not handle service instance placement within cloud environments. Instead, it focuses on providing relevant information between cloud and network to achieve joint optimization for cloud-based services. It does not aim to develop an orchestrator production system either.

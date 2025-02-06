# Charter for Neotec(Network Operations in Telecom Cloud) 
 Note: "NetOps4Clouds" might be chosen for naming the potential WG after the BoF.

## Background and Motivation

The Neotec(NetOps4Clouds) Working Group focuses on defining standardized interfaces, such as YANG models, to enable dynamic network policy adjustments—such as time-sensitive UCMP (Unequal Cost Multipath) policies for routers—that accommodate the scaling of cloud-hosted services and ensure that assured network resources are adjusted for the services in the clouds. This work will mainly be applied to cloud-aware network operation environment, where network operators manage cloud infrastructures for services requiring strict SLA guarantees. In this case "Telecom clouds" is used to refer to the cloud infrastructure managed by network operators.  

Telecom clouds provide compute, storage, and networks to fulfill the Service Level Objectives (SLOs) required by user applications. Typically, telecom edge clouds undertake this task closer to the customer locations. Telecom edge clouds may have different types of processing resources (CPU, GPU, FPGA, etc.), and be dimensioned with less resource capacity compared to conventional DCs. Also, network management and operation systems (including network controllers) have limited coordination with the cloud system even though they are both managed by the same network operator.

While cloud services can scale dynamically using mechanisms like ACaaS, network controllers are often unaware of these changes timely. Without this awareness, they cannot adjust network resources, load balancing, or time-sensitive UCMP policies, potentially leading to SLA violations and inefficient resource utilization. The Neotec (NetOps4Clouds) Working Group defines standardized interfaces to enable the network controller to dynamically update policies in response to cloud scaling events, ensuring the necessary network adjustments without exposing internal service structures. This limitation also impacts the performance and reliability of cloud-based services such as video and AI/ML applications. Network operations must be aware of cloud resources and service status to provide guaranteed SLA for the services hosted in multiple clouds by providing assured bandwidth and latency. As network operators often rely on equipment and controllers from multiple vendors, standardized and interoperable solutions are essential for the network management and operation to be cloud-aware. The absence of standardized interfaces for cloud-aware network operation and coordination remains a significant challenge.

## Goals and Scope
The Working Group will define standardized mechanisms for dynamic exchange of cloud resource status and service instance changes. A key focus is a shim layer that bridges cloud telemetry and network controllers, ensuring seamless API integration between cloud and network environments. Specifically, it will focus on defining data models to enable dynamic coordination between a cloud-aware service orchestrator and existing network controllers and cloud managers. The term "cloud-aware service orchestrator" refers to a functional component at network operation domain that is capable of dynamically managing networks (e.g., fixed, mobile access, metro networks, or backbone networks etc.) for optimizing services deployment across clouds. These models will provide abstracted cloud resource metrics and service status updates, enabling dynamic network policy adjustments, such as dynamic UCMP changes and adaptive load-balancing—whenever cloud services scale up or down. This ensures that the network can allocate adequate resources to support cloud-hosted services while maintaining SLA guarantees. 

## Work Items
The Neotec(NetOps4Clouds) Working Group will initially focus on the following deliverables:
* Document groundwork via a set of informational Internet-Drafts, not necessarily for publication as RFCs, such as: use cases, requirements, problem statement, gap analysis, applicability analysis, etc.

* Design the framework of network operation aware of cloud resources and service status, including the key mechanism, major components, and main interfaces. Provide a structured framework for policy-based traffic optimization among multi-edge clouds. This document is considered as a "living" document to guide the WG.

* Develop YANG models to provide network controllers with dynamic service instance status, ensuring dynamic network adjustments—including UCMP policy updates and adaptive load balancing—whenever cloud services scale up or down. These updates allow the network to seamlessly accommodate changes without requiring detailed visibility into internal cloud structures.

* Define YANG models to dynamically adjust policies across ingress, intermediate, and egress routers based on dynamic cloud metrics. 

* Define a shim layer acting as middleware between cloud telemetry systems (e.g., AWS CloudWatch, Google Cloud Monitoring, Azure Monitor) and network controllers. Standardize APIs for network controllers to convert cloud metrics into IETF-compliant network telemetry formats (e.g., YANG, gRPC-based streaming, NetConf APIs).

It should be noted that this Working Group focuses on addressing the network operation issues, not cloud scheduling or management issues, they remain outside its scope. It does not aim to develop an orchestrator production system either.

This Working Group will also serve as a platform for the community to exchange requirements, challenges, and experiences related to network management and operation for cloud-based services.

## Out of Scope
* The Working Group does not handle service instance placement within cloud environments. Instead, it focuses on exposing relevant cloud metrics to network controllers for optimized network performance.

* The Working Group will not define new cloud management protocols, but rather standardize the interfaces required for network-cloud coordination.




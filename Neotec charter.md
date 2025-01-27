# Charter for Neotec 

## Background and Motivation

The Neotec Working Group focuses on defining standardized interfaces for cloud-aware network operation and coordination environment, where network operators manage extensive edge cloud infrastructures with services requiring strict SLA guarantees, including low latency and high bandwidth.
Telecom clouds of network operators provide compute, storage, and networks to fulfill the connectivity and Service Level Objectives (SLOs) requirements of user applications, in particular, telecom edge clouds undertake this task closer to the customer locations. The telecom edge clouds could have different types of processing resources (CPU, GPU, FPGA, etc.), and be dimensioned with less resource capacity compared to conventional DCs. Also, network management and operation system (including the network controller) has limited interaction or coordination with the cloud system even though they are both managed by the same operator.
Network operations must be aware of cloud resources and service status to provide guaranteed SLA for the services hosted in multiple clouds by providing assured bandwidth and latency.If the network controller lacks of awareness of cloud resources, status and traffic characteristics of the services they carry, it could not timely adjust network resource when service function instances are scaled up or down, relocated, or could not timely adjust network paths when traffic patterns between service functions change, which results in suboptimal performance, failure to meet SLAs, and inefficient utilization of network resources needed to support the new deployment conditions. This limitation also impacts the performance and reliability of services such as video and AI/ML applications. Network operations must be aware of cloud resources and service status to provide guaranteed SLA for the services hosted in multiple clouds by providing assured bandwidth and latency.

## Goals and Scope
The Neotec Working Group will define standardized mechanisms and interfaces for real-time exchange of cloud resource status, service instance changes, and dynamic connectivity insights to enable efficient network orchestration and traffic engineering across multiple clouds. The Neotec Working Group will focus on defining data models to enable dynamic coordination between a cloud-aware service orchestrator and existing network controllers and cloud managers. The term "cloud-aware service orchestrator" refers to a functional component at network operation domain, it is capable of dynamically managing networks (e.g., fixed, mobile access, metro networks, or backbone networks) for optimizing services deployment across clouds. The information will be provided by these models include: cloud resource metrics, service status in clouds, dynamic adjustment of network load-balancing policies, and inter-cloud network connectivity and status. As operators often rely on equipment and controllers from multiple vendors, standardized and interoperable solutions are essential for the network management and operation to be cloud-aware.

## Work Items
The Neotec Working Group will initially focus on the following deliverables:
* Document groundwork via a set of informational Internet-Drafts, not necessarily for publication as RFCs, such as: use cases, requirements, problem statement and gap analysis.
* Design the framework of network operation perception of cloud resources and service status, including the core mechanism, major components, and key interfaces.
* Develops YANG models for exposing the resources and metric information from Cloud DC into the operation domain of the network to meet service needs. 
* Develop YANG models to provide network controllers with real-time service instance status to adjust network paths, or enable real-time adjustments to load-balancing policies, ensuring real-time policy updates across ingress, intermediate, and egress routers based on real-time service demand and network conditions.
* Develops a general flow scheduling/load balancing policy YANG model that can be applied to various connections (VPN, Internet connection, SD-WAN) to improve the throughput and efficiency of the service across telecom edge clouds. 
* Define models to dynamically adjust UCMP (Unequal Cost Multipath) policies across ingress, intermediate, and egress routers based on real-time cloud metrics. Provide a structured framework for policy-based traffic optimization among multi-edge clouds.
* Define a shim layer acting as middleware between cloud telemetry systems (e.g., AWS CloudWatch, Google Cloud Monitoring, Azure Monitor) and network controllers. Standardize APIs for network controllers to convert cloud metrics into IETF-compliant network telemetry formats (e.g., YANG, gRPC-based streaming, NetConf APIs).
* Analyze the applicability of the standardized mechanisms and interfaces designed above. 

The Neotec Working Group focuses on addressing the network issues, not that of cloud scheduling or management issues, they remain outside its scope. It does not aim to develop an orchestrator production system either.

## Out of Scope
* The Neotec Working Group does not handle service instance placement within cloud environments. Instead, it focuses on exposing relevant cloud metrics to network controllers for optimized network performance.

* The Neotec Working Group will not define new cloud management protocols, but rather standardize the interfaces required for network-cloud coordination.

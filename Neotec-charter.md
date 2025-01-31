# Charter for Networks for Cloud Operations (Net4CloudOps) 

## Background and Motivation

Telecom clouds of network operators provide compute, storage, and networks to fulfill the Service Level Objectives (SLOs) required by user applications. Typically, telecom edge clouds undertake this task closer to the customer locations. Telecom edge clouds may have different types of processing resources (CPU, GPU, FPGA, etc.), and be dimensioned with less resource capacity compared to conventional DCs. Also, network management and operation systems (including, network controllers) have limited coordination with the cloud system even though they are both managed by the same network operator.

If the network controllers lack of awareness of cloud resources, status, and traffic characteristics of the services delivered over the network, they can not timely adjust network resources when service function instances are scaled up or down, relocated, or could not timely adjust network paths when traffic patterns between service functions change, which results in suboptimal performance, failure to meet SLAs, and inefficient utilization of network resources. This limitation also impacts the performance and reliability of cloud-based services such as video and AI/ML applications. Network operations must be aware of cloud resources and service status to provide guaranteed SLA for the services hosted in multiple clouds by providing assured bandwidth and latency. The absence of standardized interfaces for cloud-aware network operation and coordination remains a significant challenge.

## Goals and Scope

The Working Group will define standardized mechanisms and interfaces for dynamic exchange of cloud resource status, service instance changes, and dynamic connectivity insights to enable efficient network orchestration and traffic engineering across multiple clouds. Specifically, it will focus on defining data models to enable dynamic coordination between a cloud-aware service orchestrator and existing network controllers and cloud managers.

The term "cloud-aware service orchestrator" refers to a functional component at network operation domain that is capable of dynamically managing networks (e.g., fixed, mobile access, metro networks, or backbone networks) for optimizing services deployment across clouds. The information that will be provided by these models include: cloud resource metrics, service status in clouds, dynamic adjustment of network load-balancing policies, and inter-cloud network connectivity and status.

As network operators often rely on equipment from multiple vendors, standardized and interoperable solutions are essential for the network management and operation to be cloud-aware.

## Work Items

The Working Group will initially focus on the following deliverables:

1. Document groundwork via a set of Informational Internet-Drafts, not necessarily for publication as RFCs, such as: use cases, requirements, problem statement, and gap analysis.
2. Design the framework of network operation aware of cloud resources and service status, including the key mechanisms, major components, and main interfaces. Provide a structured framework for policy-based traffic optimization among multi-edge clouds.
3. Develop YANG models for exposing the resources and metric information from Cloud DC into the operation domain of the network to meet service needs. 
4. Develop YANG models to provide network controllers with dynamic service instance status to adjust network paths, or enable dynamic adjustments to load-balancing policies, ensuring dynamic policy updates across ingress, intermediate, and egress routers based on actual service demand and network conditions.
5. Develops a general flow scheduling/load balancing policy YANG model that can be applied to various connections (VPN, Internet connection, SD-WAN) to improve the throughput and efficiency of the service across telecom edge clouds. 
6. Define models to dynamically adjust UCMP (Unequal Cost Multipath) policies across ingress, intermediate, and egress routers based on dynamic cloud metrics. 
7. Define a shim layer acting as middleware between cloud telemetry systems and network controllers. Standardize APIs for network controllers to convert cloud metrics into IETF-compliant network telemetry formats (e.g., YANG).
8. Analyze the applicability of the standardized mechanisms and interfaces designed above. 

It should be noted that the Working Group will focus on addressing the network issues, not that of cloud scheduling or management issues. Such matters are out of scope. Also, the WG does not aim to develop an orchestrator production system.

The WG will also serve as a platform for the community to exchange requirements, challenges, and experiences related to network management and operation for cloud-based services.

## Out of Scope

* The WG does not handle service instance placement within cloud environments. Instead, it focuses on exposing relevant cloud metrics to network controllers for optimized network performance.

* The WG will not define cloud management protocols or extensions, but rather standardize the interfaces required for network-cloud coordination.

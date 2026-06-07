# Modern Data Center Fabric: EVPN-VXLAN & SR-MPLS

This project demonstrates a next-generation data center network architecture built on an IETF-standard (RFC 7938) 2-Spine / 4-Leaf Clos topology, fully simulated within the EVE-NG environment.

## Project Overview
The primary objective is to overcome the limitations of traditional Spanning Tree Protocol bottlenecks and VLAN boundaries. This is achieved by optimizing the underlay network with Segment Routing and creating a hardware-independent, multi-tenant overlay network using EVPN-VXLAN.

## Technology Stack
* **Emulation Platform:** EVE-NG
* **Spine Layer:** Cisco IOS-XRv 9000
* **Leaf Layer:** Arista vEOS
* **Underlay Routing:** IS-IS, Segment Routing
* **Overlay Routing:** MP-BGP, L2VPN EVPN
* **Encapsulation & Isolation:** VXLAN, Distributed Anycast Gateway

## Key Features & Outcomes
* **High Availability:** Achieved sub-50ms fast reroute capabilities during simulated link failures without data loss.
* **Active/Active Load Balancing:** Eliminated passive standby links, ensuring 100% bandwidth utilization across the fabric.
* **Micro-Segmentation:** Successfully isolated multi-tenant traffic across the same physical backbone using VRFs, aligning with Zero-Trust architecture principles.

## Repository Structure
* `/configs`: Initial configuration files for all Spine and Leaf routing devices.
* `/topology`: The EVE-NG `.unl` export file and network architecture diagrams.
* `/docs`: Detailed performance analysis, test scenarios, and the comprehensive academic report.

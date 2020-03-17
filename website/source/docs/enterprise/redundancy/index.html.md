---
layout: "docs"
page_title: "Consul Enterprise Redundancy Zones"
sidebar_current: "docs-enterprise-redundancy"
description: |-
  Consul Enterprise redundancy zones enable hot standby servers on a per availability zone basis.
---

# Consul Enterprise Redundancy Zones

> *I want to take advantage of [Enhanced Read Scalability](/docs/enterprise/read-scale/index.html)*
> *by scaling my non-voting members horizontally, however I also want those members to promote to*
> *voting members in the event of a failure scenario*

[Consul Enterprise](https://www.hashicorp.com/consul.html) 
[Redundancy Zones](https://learn.hashicorp.com/consul/day-2-operations/autopilot#redundancy-zones) 
provides both scaling as well as resiliancy benefits by enabling the deployment of non-voting
servers alongside voting servers on a per Availability Zone basis.  

When using Redunancy Zones, if an operator is working across 3 Availability Zones, they 
could have 2 servers (1 voting/1 non-voting) in each zone. In the event that a voting 
member in an availability zone fails, the redundancy zone configuration would automatically 
promote the non-voting member to a voting member. In the event that an entire Availability 
Zone was lost, a non-voting member in one of the existing availability zones would promote 
to a voting member, keeping server quorum. This capability functions as a "hot standby" 
for server nodes while also providing (and expanding) the capabilities of 
[Enhanced Read Scalability](/docs/enterprise/read-scale/index.html) by also including reocvery 
capabilities. 

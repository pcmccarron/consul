---
layout: "docs"
page_title: "Consul Enterprise Enhanced Read Scalability"
sidebar_current: "docs-enterprise-read-scale"
description: |-
  Consul Enterprise supports increased read scalability without impacting write latency by introducing
  non-voting servers.
---

# Consul Enterprise Enhanced Read Scalability

> *My Consul cluster deals with a significantly high amount of transactions. I need to be able to increase*
> *the scale of my Consul cluster without the negative performance impacts (write latency) that comes with*
> *a larger server cluster.*

[Consul Enterprise](https://www.hashicorp.com/consul.html) provides the ability to scale Consul server clusters
to include voting and non-voting servers. Non-voting servers still receive data from the cluster replication
however do not take part in quorum election operations. Expanding your Consul cluster in this way can scale
reads without impacting write latency. 

For more details, review the [Consul Server configuration](https://www.consul.io/docs/agent/options.html) 
documentation and the [-non-voting-server](https://www.consul.io/docs/agent/options.html#_non_voting_server)
configuration flag.
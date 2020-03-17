---
layout: "docs"
page_title: "Consul Enterprise Automated Upgrades"
sidebar_current: "docs-enterprise-upgrades"
description: |-
  Consul Enterprise supports an upgrade pattern that allows operators to deploy a complete cluster of new servers and then just wait for the upgrade to complete.
---

# Consul Enterprise Automated Upgrades

> *How can I upgrade my Consul cluster to the latest version without downtime? Can this upgrade be automated?*

[Consul Enterprise](https://www.hashicorp.com/consul.html) enables the capability of automatically upgrading a Consul cluster to a new
version as updated server nodes join the cluster. This [Automated Upgrade](https://learn.hashicorp.com/consul/day-2-operations/autopilot#upgrade-migrations) (referred to as Autopilot) will monitor a the amount of voting members currently in a cluster, and when an equal 
amount of new server nodes are joined, demote the original servers to non voting members. Demotion of legacy server nodes will not occur until the voting members on the new version match. Once this demotion occurs, the previous versioned servers can be removed from the cluster safely. 

You can review more information about this functionality in the [Consul Operator Autopilot](https://www.consul.io/docs/commands/operator/autopilot.html) documentation.

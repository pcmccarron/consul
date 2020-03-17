---
layout: "docs"
page_title: "Consul Enterprise Automated Backups"
sidebar_current: "docs-enterprise-backups"
description: |-
  Consul Enterprise provides a highly available service that manages taking snapshots, rotation and sending backup files offsite to Amazon S3 (or S3-compatible endpoints), Google Cloud Storage, or Azure Blob Storage.
---

# Consul Enterprise Automated Backups

> *How can I ensure that my Consul cluster has been backed up for the purposes of*
> *Disaster Recovery? How can I ensure this backup process is automated and that*
> *backups are delivered offsite?*

[Consul Enterprise](https://www.hashicorp.com/consul.html) enables customers to run
the snapshot agent within their environment as a service (Systemd as an example)
or scheduled through other means. Once running, this service operates as a highly 
available process that integrates with the snapshot API to automatically manage 
taking snapshots, backup rotation, and sending backup files offsite to Amazon S3 
(or another S3-compatible endpoint), Google Cloud Storage, or Azure Blob Storage.

This capability provides an enterprise solution for backup and restoring the state of Consul servers 
within an environment in an automated manner. These Snapshots are atomic and point-in-time. Consul 
cluster backups include: 

- Key/Value Store Entries
- Service Catalog Registrations 
- Prepared Queries 
- Sessions
- Access Control Lists (ACLs)
- Namespaces

For more experience leveraging Consuls snapshot functionality, we suggest you look through our learn guide for [Datacenter Backups in Consul](https://learn.hashicorp.com/consul/datacenter-deploy/backup). For detailed configuration information on configuring this functional, review the [Consul Snapshot Agent documentation](/docs/commands/snapshot/agent.html).
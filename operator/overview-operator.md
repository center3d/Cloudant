---

copyright:
  years: 2019
lastupdated: "2019-09-26"

keywords: compare

subcollection: cloudant

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:external: target="_blank" .external}

<!-- Acrolinx: 2017-05-10 -->

# Overview
{: #apache-couchdb-operator}

An [Operator](https://kubernetes.io/docs/concepts/extend-kubernetes/operator/){: new_window}{: external} is a method of packaging, deploying, and managing a Kubernetes-native application. 

The Operator for Apache CouchDB facilitates deploying and managing an Apache CouchDB cluster on Kubernetes. 

## Operator Features
{: #operator-features-apache-couchdb}

The following list shows the features of an Operator: 

- Fully-automated deployment and configuration of Apache CouchDB clusters.
- Single Operator deployment can support single, multiple, or all Kubernetes namespaces.

## Apache CouchDB Features
{: #apache-couchdb-features}

The Operator for Apache CouchDB uses the following defaults when deploying a new Apache CouchDB cluster to ensure a secure and highly-available configuration.

### Security
{: #security-overview-operator}

<dl>
<dt><strong>TLS</strong></dt>
<dd>The Operator leverages the Red Hat OpenShift cert-manager to create certificates and enable HTTPS/SSL on the cluster. On other Kubernetes distributions, TLS is supported by using user-provided certificates. It's recommended that you review Apache CouchDB HTTPS (SSL/TLS) Options, or install Jetstack cert-manager to manage this elsewhere.</dd>

<dt><strong>Encryption</strong></dt>
<dd>Encrypted intra-cluster communication, which means that the communication between database nodes is encrypted in addition to TLS on the HTTPS API.</dd>

<dt><strong>Authentication</strong></dt>
<dd>The parameter `require_valid_user` is set to `true`, which means that no requests are allowed from anonymous users. Every request must be authenticated.</dd>

<dt><strong>Authorization</strong></dt>
<dd>Databases are initially accessible by Apache CouchDB admins only.</dd>
</dl>

### High Availability
{: #high-availability-overview-operator}

<dl>
<dt><strong>Nodes</strong></dt>
<dd>Each database node in an Apache CouchDB cluster requires its own Kubernetes node. It's recommended that you run it with a minimum of three nodes for any production deployment.</dd>
<dt><strong>Zones</strong></dt>
<dd>The Apache CouchDB cluster database nodes are spread across available Kubernetes fault zones where available.</dd>
<dt><strong>Replicas</strong></dt>
<dd>The default configuration for each database is eight shards (Q=8) and three shard copies (N=3), where each shard copy is deployed on a separate node in the cluster. </dd> 
</dl>

## Supported Apache CouchDB Versions
{: #couchdb-supported-versions}

The currently supported Apache CouchDB version is [Apache CouchDB 2.3.1](https://docs.couchdb.org/en/2.3.1/){: new_window}{: external}.
 
## Using the Operator
{: #using-operator}

Follow these steps to use Operator for Apache CouchDB to deploy a CouchDB Cluster on Kubernetes:

1. Install the Operator for Apache CouchDB (just once).
2. Configure the CouchDB cluster.
3. Deploy the CouchDB cluster.
4. Access the CouchDB cluster.

## What to do next
{: #what-to-do-next}

Follow the instructions in this section about how to proceed with each step. Instructions vary between Kubernetes distributions and versions. Note that there are different steps for Kubernetes, as well as, Red Hat OpenShift 3.x versus Red Hat OpenShift 4.x.
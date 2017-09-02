# Install Client Tools

This tutorial requires interacting with a number of tools and services which require a specific set of command line utilities to be installed on the machine used to follow this tutorial.

Read up on CloudFlare's PKI toolkit (__cfssl__ and __cfssljson__ below) here:

	https://blog.cloudflare.com/introducing-cfssl/

[Well worth a read for some insight into why managing browser certs is such a pain. Doesn't cover CRLs.]

Install the following client tools and ensure they are in your path:

* [cfssl](https://github.com/mramshaw/cfssl) 1.2.0
* [cfssljson](https://github.com/mramshaw/cfssl) 1.2.0
* [consul](https://www.consul.io/downloads.html) 0.9.2
* [nomad](https://www.nomadproject.io/downloads.html) 0.6.0
* [vault](https://www.vaultproject.io/downloads.html) 0.8.0
* [gcloud](https://cloud.google.com/sdk/) 166.0.0
* [kubectl](https://cloud.google.com/sdk/docs/components) 1.7.3
* [jq](https://stedolan.github.io/jq/download/) 1.5

Upgrading to the latest version of gcloud components:

	gcloud components update

Upgrading/Downgrading to a specific version of gcloud components:

	gcloud components update --version 166.0.0

Verify current version of kubectl (slow):

	kubectl version

Uninstall current version of kubectl:

	gcloud components remove kubectl

Upgrading/Downgrading to a specific version of gcloud components:

	gcloud components update --version 167.0.0

Install kubectl using gcloud (we need __173.0.0__):

	gcloud components install kubectl

[The 166.0.0 gcloud components only offer kubectl 172.0.0 - for this work the specific version of kubectl is more important.]

Next: [Provision The Kubernetes Infrastructure](03-kubernetes-infrastructure.md)

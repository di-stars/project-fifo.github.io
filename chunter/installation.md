---
layout: default
category: chunter
section: chunter/installation
title: Chunter Installation
---
# Chunter Installation

Please read the Chunter section in the current build section above for basic information on chunter and some helpful notes before continuing.

To install "Chunter" we do the following:

<p class="bs-callout bs-callout-info">
Please note that this is for the reelease version of FiFo to installed the current development version use `VERSION=dev` instead of `VERSION=rel`.
</p>

```bash
VERSION=rel
cd /opt
curl -O http://release.project-fifo.net/chunter/${VERSION}/chunter-latest.gz
gunzip chunter-latest.gz
sh chunter-latest
```

Once services have been installed, we then enable the service and ensure that it is running

```bash
svcadm enable epmd chunter
svcs chunter
```

If the service is running you should see.

```

STATE          STIME    FMRI
online         Dec_31   svc:/network/chunter:default
```

Once the service is running FiFO will auto-discover the node and after about a minute the SmartOS node will appear in the FiFO web browser to be managed.

Chunter will try to guess the systems IP, it will look for a `fifo0` vnic, if this doesn't exit it will take the ip of the `admin` nic. If chunter registered with a wrong IP it needs to be changed in the config file, and the hypervisor reregistered. This can be done by [removing it](/sniffle/administration.html) and restarting chunter.

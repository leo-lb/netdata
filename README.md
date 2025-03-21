# Netdata [![Build Status](https://travis-ci.com/netdata/netdata.svg?branch=master)](https://travis-ci.com/netdata/netdata) [![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/2231/badge)](https://bestpractices.coreinfrastructure.org/projects/2231) [![License: GPL v3+](https://img.shields.io/badge/License-GPL%20v3%2B-blue.svg)](https://www.gnu.org/licenses/gpl-3.0) [![analytics](https://www.google-analytics.com/collect?v=1&aip=1&t=pageview&_s=1&ds=github&dr=https%3A%2F%2Fgithub.com%2Fnetdata%2Fnetdata&dl=https%3A%2F%2Fmy-netdata.io%2Fgithub%2Freadme&_u=MAC~&cid=5792dfd7-8dc4-476b-af31-da2fdb9f93d2&tid=UA-64295674-3)]()

[![Code Climate](https://codeclimate.com/github/netdata/netdata/badges/gpa.svg)](https://codeclimate.com/github/netdata/netdata) [![Codacy Badge](https://api.codacy.com/project/badge/Grade/a994873f30d045b9b4b83606c3eb3498)](https://www.codacy.com/app/netdata/netdata?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=netdata/netdata&amp;utm_campaign=Badge_Grade) [![LGTM C](https://img.shields.io/lgtm/grade/cpp/g/netdata/netdata.svg?logo=lgtm)](https://lgtm.com/projects/g/netdata/netdata/context:cpp) [![LGTM JS](https://img.shields.io/lgtm/grade/javascript/g/netdata/netdata.svg?logo=lgtm)](https://lgtm.com/projects/g/netdata/netdata/context:javascript) [![LGTM PYTHON](https://img.shields.io/lgtm/grade/python/g/netdata/netdata.svg?logo=lgtm)](https://lgtm.com/projects/g/netdata/netdata/context:python)

---

**Netdata** is **distributed, real-time, performance and health monitoring for systems and applications**. It is a highly optimized monitoring agent you install on all your systems and containers.

Netdata provides **unparalleled insights**, **in real-time**, of everything happening on the systems it runs (including web servers, databases, applications), using **highly interactive web dashboards**.  It can run autonomously, without any third party components, or it can be integrated to existing monitoring tool chains (Prometheus, Graphite, OpenTSDB, Kafka, Grafana, etc).

_Netdata is **fast** and **efficient**, designed to permanently run on all systems (**physical** & **virtual** servers, **containers**, **IoT** devices), without disrupting their core function._

Netdata is **free, open-source software** and it currently runs on **Linux**, **FreeBSD**, and **MacOS**.

Netdata is not hosted by the CNCF but is the 3rd most starred open-source project in the [Cloud Native Computing Foundation (CNCF) landscape](https://landscape.cncf.io/format=card-mode&grouping=no&sort=stars).

---

People get **addicted to Netdata**.<br/>
Once you use it on your systems, **there is no going back**! *You have been warned...*

![image](https://user-images.githubusercontent.com/2662304/48305662-9de82980-e537-11e8-9f5b-aa1a60fbb82f.png)

[![Tweet about Netdata!](https://img.shields.io/twitter/url/http/shields.io.svg?style=social&label=Tweet%20about%20netdata)](https://twitter.com/intent/tweet?text=Netdata,%20real-time%20performance%20and%20health%20monitoring,%20done%20right!&url=https://my-netdata.io/&via=linuxnetdata&hashtags=netdata,monitoring)


## Contents

1. [How it looks](#how-it-looks) - have a quick look at it
2. [User base](#user-base) - who uses Netdata?
3. [Quick Start](#quick-start) - try it now on your systems
4. [Why Netdata](#why-netdata) - why people love Netdata, how it compares with other solutions
5. [News](#news) - latest news about Netdata
6. [How it works](#how-it-works) - high level diagram of how Netdata works
7. [infographic](#infographic) - everything about Netdata, in a page
8. [Features](#features) - what features does it have
9. [Visualization](#visualization) - unique visualization features
10. [What does it monitor](#what-does-it-monitor) - which metrics it collects
11. [Documentation](#documentation) - read the docs
12. [Community](#community) - discuss with others and get support
13. [License](#license) - check the license of Netdata
14. [Is it any good?](#is-it-any-good) - Yes
15. [Is it awesome?](#is-it-awesome) - Yes

## How it looks

The following animated image, shows the top part of a typical Netdata dashboard.

![peek 2018-11-11 02-40](https://user-images.githubusercontent.com/2662304/48307727-9175c800-e55b-11e8-92d8-a581d60a4889.gif)

*A typical Netdata dashboard, in 1:1 timing. Charts can be panned by dragging them, zoomed in/out with `SHIFT` + `mouse wheel`, an area can be selected for zoom-in with `SHIFT` + `mouse selection`. Netdata is highly interactive and **real-time**, optimized to get the work done!*

> *We have a few online demos to experience it live: [https://www.netdata.cloud](https://www.netdata.cloud/#live-demo)*

## User base

Netdata is used by hundreds of thousands of users all over the world.
Check our [GitHub watchers list](https://github.com/netdata/netdata/watchers).
You will find people working for **Amazon**, **Atos**, **Baidu**, **Cisco Systems**, **Citrix**, **Deutsche Telekom**, **DigitalOcean**,
**Elastic**, **EPAM Systems**, **Ericsson**, **Google**, **Groupon**, **Hortonworks**, **HP**, **Huawei**,
**IBM**, **Microsoft**, **NewRelic**, **Nvidia**, **Red Hat**, **SAP**, **Selectel**, **TicketMaster**,
**Vimeo**, and many more!

### Docker pulls
We provide docker images for the most common architectures. These are statistics reported by docker hub:

[![netdata/netdata (official)](https://img.shields.io/docker/pulls/netdata/netdata.svg?label=netdata/netdata+%28official%29)](https://hub.docker.com/r/netdata/netdata/) [![firehol/netdata (deprecated)](https://img.shields.io/docker/pulls/firehol/netdata.svg?label=firehol/netdata+%28deprecated%29)](https://hub.docker.com/r/firehol/netdata/) [![titpetric/netdata (donated)](https://img.shields.io/docker/pulls/titpetric/netdata.svg?label=titpetric/netdata+%28third+party%29)](https://hub.docker.com/r/titpetric/netdata/)

### Registry
When you install multiple Netdata, they are integrated into **one distributed application**, via a [Netdata registry](registry/#registry). This is a web browser feature and it allows us to count the number of unique users and unique Netdata servers installed. The following information comes from the global public Netdata registry we run:

[![User Base](https://registry.my-netdata.io/api/v1/badge.svg?chart=netdata.registry_entries&dimensions=persons&label=user%20base&units=M&value_color=blue&precision=2&divide=1000000&v43)](https://registry.my-netdata.io/#menu_netdata_submenu_registry) [![Monitored Servers](https://registry.my-netdata.io/api/v1/badge.svg?chart=netdata.registry_entries&dimensions=machines&label=servers%20monitored&units=k&divide=1000&value_color=orange&precision=2&v43)](https://registry.my-netdata.io/#menu_netdata_submenu_registry) [![Sessions Served](https://registry.my-netdata.io/api/v1/badge.svg?chart=netdata.registry_sessions&label=sessions%20served&units=M&value_color=yellowgreen&precision=2&divide=1000000&v43)](https://registry.my-netdata.io/#menu_netdata_submenu_registry)

*in the last 24 hours:*<br/> [![New Users Today](https://registry.my-netdata.io/api/v1/badge.svg?chart=netdata.registry_entries&dimensions=persons&after=-86400&options=unaligned&group=incremental-sum&label=new%20users%20today&units=null&value_color=blue&precision=0&v42)](https://registry.my-netdata.io/#menu_netdata_submenu_registry) [![New Machines Today](https://registry.my-netdata.io/api/v1/badge.svg?chart=netdata.registry_entries&dimensions=machines&group=incremental-sum&after=-86400&options=unaligned&label=servers%20added%20today&units=null&value_color=orange&precision=0&v42)](https://registry.my-netdata.io/#menu_netdata_submenu_registry) [![Sessions Today](https://registry.my-netdata.io/api/v1/badge.svg?chart=netdata.registry_sessions&after=-86400&group=incremental-sum&options=unaligned&label=sessions%20served%20today&units=null&value_color=yellowgreen&precision=0&v42)](https://registry.my-netdata.io/#menu_netdata_submenu_registry)

## Quick Start
![](https://registry.my-netdata.io/api/v1/badge.svg?chart=web_log_nginx.requests_per_url&options=unaligned&dimensions=kickstart&group=sum&after=-3600&label=last+hour&units=installations&value_color=orange&precision=0) ![](https://registry.my-netdata.io/api/v1/badge.svg?chart=web_log_nginx.requests_per_url&options=unaligned&dimensions=kickstart&group=sum&after=-86400&label=today&units=installations&precision=0)

To install Netdata from source on any Linux system (physical, virtual, container, IoT, edge) and keep it up to date with our **nightly releases** automatically, run the following:

```bash
# make sure you run `bash` for your shell
bash

# install Netdata directly from GitHub source
bash <(curl -Ss https://my-netdata.io/kickstart.sh)
```

To learn more about the pros and cons of using *nightly* vs. *stable* releases, see our [notice about the two options](packaging/installer/README.md#nightly-vs-stable-releases).

The above command will:

- Install any required packages on your system (it will ask you to confirm before doing so)
- Compile it, install it, and start it.

More installation methods and additional options can be found at the [installation page](packaging/installer/#installation).

To try Netdata in a docker container, run this:

```
docker run -d --name=netdata \
  -p 19999:19999 \
  -v /proc:/host/proc:ro \
  -v /sys:/host/sys:ro \
  -v /var/run/docker.sock:/var/run/docker.sock:ro \
  --cap-add SYS_PTRACE \
  --security-opt apparmor=unconfined \
  netdata/netdata
```

For more information about running Netdata in docker, check the [docker installation page](packaging/docker/).

![image](https://user-images.githubusercontent.com/2662304/48304090-fd384080-e51b-11e8-80ae-eecb03118dda.png)

From Netdata v1.12 and above, anonymous usage information is collected by default and sent to Google Analytics. To read more about the information collected and how to opt-out, check the [anonymous statistics page](docs/anonymous-statistics.md).

## Why Netdata

Netdata has a quite different approach to monitoring.

Netdata is a monitoring agent you install on all your systems. It is:

- a **metrics collector** - for system and application metrics (including web servers, databases, containers, etc)
- a **time-series database** - all stored in memory (does not touch the disks while it runs)
- a **metrics visualizer** - super fast, interactive, modern, optimized for anomaly detection
- an **alarms notification engine** - an advanced watchdog for detecting performance and availability issues

All the above, are packaged together in a very flexible, extremely modular, distributed application.

This is how Netdata compares to other monitoring solutions:

Netdata|others (open-source and commercial)
:---:|:---:
**High resolution metrics** (1s granularity)|Low resolution metrics (10s granularity at best)
Monitors everything, **thousands of metrics per node**|Monitor just a few metrics
UI is super fast, optimized for **anomaly detection**|UI is good for just an abstract view
**Meaningful presentation**, to help you understand the metrics|You have to know the metrics before you start
Install and get results **immediately**|Long preparation is required to get any useful results
Use it for **troubleshooting** performance problems|Use them to get *statistics of past performance*
**Kills the console** for tracing performance issues|The console is always required for troubleshooting
Requires **zero dedicated resources**|Require large dedicated resources

Netdata is **open-source**, **free**, super **fast**, very **easy**, completely **open**, extremely **efficient**,
**flexible** and integrate-able.

It has been designed by **SysAdmins**, **DevOps** and **Developers** for troubleshooting performance problems,
not just visualize metrics.

## News

`Jul 9th, 2019` - **[Netdata v1.16.0 released!](https://github.com/netdata/netdata/releases)**

Release v1.16.0 contains 40 bug fixes, 31 improvements and 20 documentation updates

**Binary distributions.** To improve the security, speed and reliability of new netdata installations, we are delivering our own, industry standard installation method, with binary package distributions. The RPM binaries for the most common OSs are already available on packagecloud and we’ll have the DEB ones available very soon. All distributions are considered in Beta and, as always, we depend on our amazing community for feedback on improvements.

 - Our stable distributions are at [netdata/netdata @ packagecloud.io](https://packagecloud.io/netdata/netdata)
 - The nightly builds are at [netdata/netdata-edge @ packagecloud.io](https://packagecloud.io/netdata/netdata-edge)

**Netdata now supports TLS encryption!** You can secure the communication to the [web server](https://docs.netdata.cloud/web/server/#enabling-tls-support), the [streaming connections from slaves to the master](https://docs.netdata.cloud/streaming/#securing-the-communication) and the connection to an [openTSDB backend](https://docs.netdata.cloud/backends/opentsdb/#https). 

**This version also brings two long-awaited features to netdata’s health monitoring:**

 - The [health management API](https://docs.netdata.cloud/web/api/health/#health-management-api) introduced in v1.12 allowed you to easily disable alarms and/or notifications while netdata was running. However, those changes were not persisted across netdata restarts. Since part of routine maintenance activities may involve completely restarting a monitoring node, netdata now saves these configurations to disk, every time you issue a command to change the silencer settings. The new [LIST command](https://docs.netdata.cloud/web/api/health/#list-silencers) of the API allows you to view at any time which alarms are currently disabled or silenced.
 - A way for netdata to [repeatedly send alarm notifications](https://docs.netdata.cloud/health/#alarm-line-repeat) for some, or all active alarms, at a frequency of your choosing. As a result, you will no longer have to worry about missing a notification, forgetting about a raised alarm. The default is still to only send a single notification, so that existing users are not surprised by a different behavior.  

As always, we’ve introduced new collectors, 5 of them this time:

 - Of special interest to people with Windows servers in their infrastructure is the [WMI collector](https://docs.netdata.cloud/collectors/go.d.plugin/modules/wmi/), though we are fully aware that we need to continue our efforts to do a proper port to Windows. 
 - The new `perf` plugin collects system-wide CPU performance statistics from Performance Monitoring Units (PMU) using the `perf_event_open()` system call. You can read a wonderful article on why this is useful [here](http://www.brendangregg.com/blog/2017-05-09/cpu-utilization-is-wrong.html).
 - The other three are collectors to monitor [Dnsmasq DHCP leases](https://docs.netdata.cloud/collectors/go.d.plugin/modules/dnsmasq_dhcp/), [Riak KV servers](https://docs.netdata.cloud/collectors/python.d.plugin/riakkv/) and [Pihole instances](https://docs.netdata.cloud/collectors/go.d.plugin/modules/pihole/). 

Finally, the DB Engine introduced in v1.15.0 now uses much less memory and is more robust than before. 

---

`May 21st, 2019` - **[Netdata v1.15.0 released!](https://github.com/netdata/netdata/releases)**

Release v1.15.0 contains 11 bug fixes and 30 improvements.

We are very happy and proud to be able to include two major improvements in this release: The aggregated node view and the [new database engine](https://docs.netdata.cloud/database/engine/). 

*Aggregated node view*

The No. 1 request from our community has been a better way to view and manage their Netdata installations, via an aggregated view. The node menu with the simple list of hosts on the agent UI just didn't do it for people with hundreds, or thousands of instances. This release introduces the node view, which uses the power of [Netdata Cloud](https://blog.netdata.cloud/posts/netdata-cloud-announcement/) to deliver powerful views of a Netdata-based monitoring infrastructure. You can read more about Netdata Cloud and the future of Netdata [here](https://blog.netdata.cloud/posts/netdata-cloud-announcement/).

*New database engine*

Historically, Netdata has required a lot of memory for long-term metrics storage. To mitigate this we've been building a new DB engine for several months and will continue improving until it can become the default `memory mode` for new Netdata installations. The version included in release v1.15.0 already permits longer-term storage of compressed data and we'll continue reducing the required memory in following releases.

*Other major additions*

We have added support for the [AWS Kinesis backend](https://docs.netdata.cloud/backends/aws_kinesis/) and new collectors for [OpenVPN](https://docs.netdata.cloud/collectors/go.d.plugin/modules/openvpn/), the [Tengine web server](https://docs.netdata.cloud/collectors/go.d.plugin/modules/tengine/), [ScaleIO (VxFlex OS)](https://docs.netdata.cloud/collectors/go.d.plugin/modules/scaleio/), [ioping-like latency metrics](https://docs.netdata.cloud/collectors/ioping.plugin/) and [Energi Core node instances](https://docs.netdata.cloud/collectors/python.d.plugin/energid/).

We now have a new, ["text-only" chart type](https://github.com/netdata/netdata/issues/5578), [cpu limits for v2 cgroups](https://github.com/netdata/netdata/issues/5850), [docker swarm metrics](https://docs.netdata.cloud/collectors/go.d.plugin/modules/docker_engine/) and improved [documentation](https://docs.netdata.cloud/).

We continued improving the [Kubernetes helmchart](https://github.com/netdata/helmchart) with liveness probes for slaves, persistence options, a fix for a `Cannot allocate memory` issue and easy configuration for the kubelet, kube-proxy and coredns collectors. 

Finally, we built a process to quickly replace any problematic nightly builds and added more automated CI tests to prevent such builds from being published in the first place.

---

`Apr 26th, 2019` - **[Netdata v1.14.0 released!](https://github.com/netdata/netdata/releases)**

Release 1.14 contains 14 bug fixes and 24 improvements.

The release introduces major additions to Kubernetes monitoring, with tens of new charts for [Kubelet](https://docs.netdata.cloud/collectors/go.d.plugin/modules/k8s_kubelet/), [kube-proxy](https://docs.netdata.cloud/collectors/go.d.plugin/modules/k8s_kubeproxy/) and [coredns](https://github.com/netdata/go.d.plugin/tree/master/modules/coredns) metrics, as well as significant improvements to the Netdata [helm chart](https://github.com/netdata/helmchart/). 
 
Two new collectors were added, to monitor [Docker hub](https://docs.netdata.cloud/collectors/go.d.plugin/modules/dockerhub/) and [Docker engine](https://docs.netdata.cloud/collectors/go.d.plugin/modules/docker_engine/) metrics. 

Finally, v1.14  adds support for [version 2 cgroups](https://github.com/netdata/netdata/pull/5407), [OpenLDAP over TLS](https://github.com/netdata/netdata/pull/5859), [NVIDIA SMI free and per process memory](https://github.com/netdata/netdata/pull/5796/files) and [configurable syslog facilities](https://github.com/netdata/netdata/pull/5792). 

---

`Mar 14th, 2019` - **[Netdata v1.13.0 released!](https://github.com/netdata/netdata/releases)**

Release 1.13.0 contains 14 bug fixes and 8 improvements.

Netdata has taken the first step into the world of Kubernetes, with a beta version of a [Helm chart](https://github.com/netdata/helmchart) for deployment to a k8s cluster and [proper naming](https://github.com/netdata/netdata/pull/5576) of the cgroup containers. We have [big plans](https://github.com/netdata/netdata/issues/5392) for Kubernetes, so stay tuned!

A [major refactoring of the python.d plugin](https://github.com/netdata/netdata/pull/5552) has resulted in a dramatic decrease of the required memory, making Netdata even more resource efficient.

We also added charts for IPC shared memory segments and total memory used.

---

`Feb 28th, 2019` - **[Netdata v1.12.2 released!](https://github.com/netdata/netdata/releases)**

Patch release 1.12.2 contains 7 bug fixes and 4 improvements.

The main motivation behind a new patch release is the introduction of a **stable release channel**.
A "stable" installation and update channel was always on our roadmap, but it became a necessity when we realized that our users in China could not use the nightly releases published on Google Cloud. The "stable" channel is based on our official GitHub releases and uses assets hosted on GitHub.

We are also introducing a new **Oracle DB collector** module, implemented in Python.

---

`Feb 21st, 2019` - **[Netdata v1.12.1 released!](https://github.com/netdata/netdata/releases)**

Patch release 1.12.1 contains 22 bug fixes and 8 improvements.

---

`Feb 14th, 2019` - **[Netdata v1.12.0 released!](https://github.com/netdata/netdata/releases)**

Release 1.12 is made out of 211 pull requests and 22 bug fixes.
The key improvements are:

- Introducing `netdata.cloud`, the free Netdata service for all Netdata users
- High performance plugins with go.d.plugin (data collection orchestrator written in Go)
- 7 new data collectors and 11 rewrites of existing data collectors for improved performance
- A new management API for all Netdata servers
- Bind different functions of the Netdata APIs to different ports
- Improved installation and updates

---

`Nov 22nd, 2018` - **[Netdata v1.11.1 released!](https://github.com/netdata/netdata/releases)**

- Improved internal database to support values above 64bit.
- New data collection plugins: [`openldap`](collectors/python.d.plugin/openldap/), [`tor`](collectors/python.d.plugin/tor/), [`nvidia_smi`](collectors/python.d.plugin/nvidia_smi/).
- Improved data collection plugins: Netdata now supports monitoring network interface aliases, [`smartd_log`](collectors/python.d.plugin/smartd_log/), [`cpufreq`](collectors/proc.plugin/README.md#cpu-frequency), [`sensors`](collectors/python.d.plugin/sensors/).
- Health monitoring improvements: network interface congestion alarm restored, [`alerta.io`](health/notifications/alerta/), `conntrack_max`.
- `my-netdata`menu has been refactored.
- Packaging: `openrc` service definition got a few improvements.

---

`Sep 18, 2018` - **Netdata has its own organization**

Netdata used to be a [firehol.org](https://firehol.org) project, accessible as `firehol/netdata`.

Netdata now has its own github organization `netdata`, so all github URLs are now `netdata/netdata`. The old github URLs, repo clones, forks, etc redirect automatically to the new repo.

## How it works

Netdata is a highly efficient, highly modular, metrics management engine. Its lockless design makes it ideal for concurrent operations on the metrics.

![image](https://user-images.githubusercontent.com/2662304/48323827-b4c17580-e636-11e8-842c-0ee72fcb4115.png)

This is how it works:

Function|Description|Documentation
:---:|:---|:---:
**Collect**|Multiple independent data collection workers are collecting metrics from their sources using the optimal protocol for each application and push the metrics to the database. Each data collection worker has lockless write access to the metrics it collects.|[`collectors`](collectors/#data-collection-plugins)
**Store**|Metrics are stored in RAM in a round robin database (ring buffer), using a custom made floating point number for minimal footprint.|[`database`](database/#database)
**Check**|A lockless independent watchdog is evaluating **health checks** on the collected metrics, triggers alarms, maintains a health transaction log and dispatches alarm notifications.|[`health`](health/#health-monitoring)
**Stream**|An lockless independent worker is streaming metrics, in full detail and in real-time, to remote Netdata servers, as soon as they are collected.|[`streaming`](streaming/#streaming-and-replication)
**Archive**|A lockless independent worker is down-sampling the metrics and pushes them to **backend** time-series databases.|[`backends`](backends/)
**Query**|Multiple independent workers are attached to the [internal web server](web/server/#web-server), servicing API requests, including [data queries](web/api/queries/#database-queries).|[`web/api`](web/api/#api)

The result is a highly efficient, low latency system, supporting multiple readers and one writer on each metric.

## Infographic

This is a high level overview of Netdata feature set and architecture.
Click it to to interact with it (it has direct links to documentation).

[![image](https://user-images.githubusercontent.com/43294513/60951037-8ba5d180-a2f8-11e9-906e-e27356f168bc.png)](https://my-netdata.io/infographic.html)


## Features

![finger-video](https://user-images.githubusercontent.com/2662304/48346998-96cf3180-e685-11e8-9f4e-059d23aa3aa5.gif)

This is what you should expect from Netdata:

### General
- **1s granularity** - the highest possible resolution for all metrics.
- **Unlimited metrics** - collects all the available metrics, the more the better.
- **1% CPU utilization of a single core** - it is super fast, unbelievably optimized.
- **A few MB of RAM** - by default it uses 25MB RAM. [You size it](database).
- **Zero disk I/O** - while it runs, it does not load or save anything (except `error` and `access` logs).
- **Zero configuration** - auto-detects everything, it can collect up to 10000 metrics per server out of the box.
- **Zero maintenance** - You just run it, it does the rest.
- **Zero dependencies** - it is even its own web server, for its static web files and its web API (though its plugins may require additional libraries, depending on the applications monitored).
- **Scales to infinity** - you can install it on all your servers, containers, VMs and IoTs. Metrics are not centralized by default, so there is no limit.
- **Several operating modes** - Autonomous host monitoring (the default), headless data collector, forwarding proxy, store and forward proxy, central multi-host monitoring, in all possible configurations. Each node may have different metrics retention policy and run with or without health monitoring.

### Health Monitoring & Alarms
- **Sophisticated alerting** - comes with hundreds of alarms, **out of the box**! Supports dynamic thresholds, hysteresis, alarm templates, multiple role-based notification methods.
- **Notifications**: [alerta.io](health/notifications/alerta/), [amazon sns](health/notifications/awssns/), [discordapp.com](health/notifications/discord/), [email](health/notifications/email/), [flock.com](health/notifications/flock/), [irc](health/notifications/irc/), [kavenegar.com](health/notifications/kavenegar/), [messagebird.com](health/notifications/messagebird/), [pagerduty.com](health/notifications/pagerduty/), [prowl](health/notifications/prowl/), [pushbullet.com](health/notifications/pushbullet/), [pushover.net](health/notifications/pushover/), [rocket.chat](health/notifications/rocketchat/), [slack.com](health/notifications/slack/), [smstools3](health/notifications/smstools3/), [syslog](health/notifications/syslog/), [telegram.org](health/notifications/telegram/), [twilio.com](health/notifications/twilio/), [web](health/notifications/web/) and [custom notifications](health/notifications/custom/).

### Integrations
- **time-series dbs** - can archive its metrics to **Graphite**, **OpenTSDB**, **Prometheus**, **AWS Kinesis**, **JSON document DBs**, in the same or lower resolution (lower: to prevent it from congesting these servers due to the amount of data collected). Netdata also supports **Prometheus remote write API** which allows storing metrics to **Elasticsearch**, **Gnocchi**, **InfluxDB**, **Kafka**, **PostgreSQL/TimescaleDB**, **Splunk**, **VictoriaMetrics** and a lot of other [storage providers](https://prometheus.io/docs/operating/integrations/#remote-endpoints-and-storage).

## Visualization

- **Stunning interactive dashboards** - mouse, touchpad and touch-screen friendly in 2 themes: `slate` (dark) and `white`.
- **Amazingly fast visualization** - responds to all queries in less than 1 ms per metric, even on low-end hardware.
- **Visual anomaly detection** - the dashboards are optimized for detecting anomalies visually.
- **Embeddable** - its charts can be embedded on your web pages, wikis and blogs. You can even use [Atlassian's Confluence as a monitoring dashboard](web/gui/confluence/).
- **Customizable** - custom dashboards can be built using simple HTML (no javascript necessary).

### Positive and negative values

To improve clarity on charts, Netdata dashboards present **positive** values for metrics representing `read`, `input`, `inbound`, `received` and **negative** values for metrics representing `write`, `output`, `outbound`, `sent`.

![positive-and-negative-values](https://user-images.githubusercontent.com/2662304/48309090-7c5c6180-e57a-11e8-8e03-3a7538c14223.gif)

*Netdata charts showing the bandwidth and packets of a network interface. `received` is positive and `sent` is negative.*

### Autoscaled y-axis

Netdata charts automatically zoom vertically, to visualize the variation of each metric within the visible time-frame.

![non-zero-based](https://user-images.githubusercontent.com/2662304/48309139-3d2f1000-e57c-11e8-9a44-b91758134b00.gif)

*A zero based `stacked` chart, automatically switches to an auto-scaled `area` chart when a single dimension is selected.*

### Charts are synchronized

Charts on Netdata dashboards are synchronized to each other. There is no master chart. Any chart can be panned or zoomed at any time, and all other charts will follow.

![charts-are-synchronized](https://user-images.githubusercontent.com/2662304/48309003-b4fb3b80-e578-11e8-86f6-f505c7059c15.gif)

*Charts are panned by dragging them with the mouse. Charts can be zoomed in/out with`SHIFT` + `mouse wheel` while the mouse pointer is over a chart.*

> The visible time-frame (pan and zoom) is propagated from Netdata server to Netdata server, when navigating via the [node menu](registry#registry).

### Highlighted time-frame

To improve visual anomaly detection across charts, the user can highlight a time-frame (by pressing `ALT` + `mouse selection`) on all charts.

![highlighted-timeframe](https://user-images.githubusercontent.com/2662304/48311876-f9093300-e5ae-11e8-9c74-e3e291741990.gif)

*A highlighted time-frame can be given by pressing `ALT` + `mouse selection` on any chart. Netdata will highlight the same range on all charts.*

> Highlighted ranges are propagated from Netdata server to Netdata server, when navigating via the [node menu](registry#registry).


## What does it monitor

Netdata data collection is **extensible** - you can monitor anything you can get a metric for.
Its [Plugin API](collectors/plugins.d/) supports all programing languages (anything can be a Netdata plugin, BASH, python, perl, node.js, java, Go, ruby, etc).

- For better performance, most system related plugins (cpu, memory, disks, filesystems, networking, etc) have been written in `C`.
- For faster development and easier contributions, most application related plugins (databases, web servers, etc) have been written in `python`.

#### APM (Application Performance Monitoring)
- **[statsd](collectors/statsd.plugin/)** - Netdata is a fully featured statsd server.
- **[Go expvar](collectors/python.d.plugin/go_expvar/)** - collects metrics exposed by applications written in the Go programming language using the expvar package.
- **[Spring Boot](collectors/python.d.plugin/springboot/)** - monitors running Java Spring Boot applications that expose their metrics with the use of the Spring Boot Actuator included in Spring Boot library.
- **[uWSGI](collectors/python.d.plugin/uwsgi/)** - collects performance metrics from uWSGI applications.

#### System Resources
- **[CPU Utilization](collectors/proc.plugin/)** - total and per core CPU usage.
- **[Interrupts](collectors/proc.plugin/)** - total and per core CPU interrupts.
- **[SoftIRQs](collectors/proc.plugin/)** - total and per core SoftIRQs.
- **[SoftNet](collectors/proc.plugin/)** - total and per core SoftIRQs related to network activity.
- **[CPU Throttling](collectors/proc.plugin/)** - collects per core CPU throttling.
- **[CPU Frequency](collectors/proc.plugin/)** - collects the current CPU frequency.
- **[CPU Idle](collectors/proc.plugin/)** - collects the time spent per processor state.
- **[IdleJitter](collectors/idlejitter.plugin/)** - measures CPU latency.
- **[Entropy](collectors/proc.plugin/)** - random numbers pool, using in cryptography.
- **[Interprocess Communication - IPC](collectors/proc.plugin/)** - such as semaphores and semaphores arrays.

#### Memory
- **[ram](collectors/proc.plugin/)** - collects info about RAM usage.
- **[swap](collectors/proc.plugin/)** - collects info about swap memory usage.
- **[available memory](collectors/proc.plugin/)** - collects the amount of RAM available for userspace processes.
- **[committed memory](collectors/proc.plugin/)** - collects the amount of RAM committed to userspace processes.
- **[Page Faults](collectors/proc.plugin/)** - collects the system page faults (major and minor).
- **[writeback memory](collectors/proc.plugin/)** - collects the system dirty memory and writeback activity.
- **[huge pages](collectors/proc.plugin/)** - collects the amount of RAM used for huge pages.
- **[KSM](collectors/proc.plugin/)** - collects info about Kernel Same Merging (memory dedupper).
- **[Numa](collectors/proc.plugin/)** - collects Numa info on systems that support it.
- **[slab](collectors/proc.plugin/)** - collects info about the Linux kernel memory usage.

#### Disks
- **[block devices](collectors/proc.plugin/)** - per disk: I/O, operations, backlog, utilization, space, etc.
- **[BCACHE](collectors/proc.plugin/)** - detailed performance of SSD caching devices.
- **[DiskSpace](collectors/proc.plugin/)** - monitors disk space usage.
- **[mdstat](collectors/proc.plugin/)** - software RAID.
- **[hddtemp](collectors/python.d.plugin/hddtemp/)** - disk temperatures.
- **[smartd](collectors/python.d.plugin/smartd_log/)** - disk S.M.A.R.T. values.
- **[device mapper](collectors/proc.plugin/)** - naming disks.
- **[Veritas Volume Manager](collectors/proc.plugin/)** - naming disks.
- **[megacli](collectors/python.d.plugin/megacli/)** - adapter, physical drives and battery stats.
- **[adaptec_raid](collectors/python.d.plugin/adaptec_raid/)** -  logical and physical devices health metrics.
- **[ioping](collectors/ioping.plugin/)** - to measure disk read/write latency.

#### Filesystems
- **[BTRFS](collectors/proc.plugin/)** - detailed disk space allocation and usage.
- **[Ceph](collectors/python.d.plugin/ceph/)** - OSD usage, Pool usage, number of objects, etc.
- **[NFS file servers and clients](collectors/proc.plugin/)** - NFS v2, v3, v4: I/O, cache, read ahead, RPC calls
- **[Samba](collectors/python.d.plugin/samba/)** - performance metrics of Samba SMB2 file sharing.
- **[ZFS](collectors/proc.plugin/)** - detailed performance and resource usage.

#### Networking
- **[Network Stack](collectors/proc.plugin/)** - everything about the networking stack (both IPv4 and IPv6 for all protocols: TCP, UDP, SCTP, UDPLite, ICMP, Multicast, Broadcast, etc), and all network interfaces (per interface: bandwidth, packets, errors, drops).
- **[Netfilter](collectors/proc.plugin/)** - everything about the netfilter connection tracker.
- **[SynProxy](collectors/proc.plugin/)** - collects performance data about the linux SYNPROXY (DDoS).
- **[NFacct](collectors/nfacct.plugin/)** - collects accounting data from iptables.
- **[Network QoS](collectors/tc.plugin/)** - the only tool that visualizes network `tc` classes in real-time
- **[FPing](collectors/fping.plugin/)** - to measure latency and packet loss between any number of hosts.
- **[ISC dhcpd](collectors/python.d.plugin/isc_dhcpd/)** - pools utilization, leases, etc.
- **[AP](collectors/charts.d.plugin/ap/)** - collects Linux access point performance data (`hostapd`).
- **[SNMP](collectors/node.d.plugin/snmp/)** - SNMP devices can be monitored too (although you will need to configure these).
- **[port_check](collectors/python.d.plugin/portcheck/)** - checks TCP ports for availability and response time.

#### Virtual Private Networks
- **[OpenVPN](collectors/python.d.plugin/ovpn_status_log/)** - collects status per tunnel.
- **[LibreSwan](collectors/charts.d.plugin/libreswan/)** - collects metrics per IPSEC tunnel.
- **[Tor](collectors/python.d.plugin/tor/)** - collects Tor traffic statistics.

#### Processes
- **[System Processes](collectors/proc.plugin/)** - running, blocked, forks, active.
- **[Applications](collectors/apps.plugin/)** - by grouping the process tree and reporting CPU, memory, disk reads, disk writes, swap, threads, pipes, sockets - per process group.
- **[systemd](collectors/cgroups.plugin/)** - monitors systemd services using CGROUPS.

#### Users
- **[Users and User Groups resource usage](collectors/apps.plugin/)** - by summarizing the process tree per user and group, reporting: CPU, memory, disk reads, disk writes, swap, threads, pipes, sockets
- **[logind](collectors/python.d.plugin/logind/)** - collects sessions, users and seats connected.

#### Containers and VMs
- **[Containers](collectors/cgroups.plugin/)** - collects resource usage for all kinds of containers, using CGROUPS (systemd-nspawn, lxc, lxd, docker, kubernetes, etc).
- **[libvirt VMs](collectors/cgroups.plugin/)** - collects resource usage for all kinds of VMs, using CGROUPS.
- **[dockerd](collectors/python.d.plugin/dockerd/)** - collects docker health metrics.

#### Web Servers
- **[Apache and lighttpd](collectors/python.d.plugin/apache/)** - `mod-status` (v2.2, v2.4) and cache log statistics, for multiple servers.
- **[IPFS](collectors/python.d.plugin/ipfs/)** - bandwidth, peers.
- **[LiteSpeed](collectors/python.d.plugin/litespeed/)** - reads the litespeed rtreport files to collect metrics.
- **[Nginx](collectors/python.d.plugin/nginx/)** - `stub-status`, for multiple servers.
- **[Nginx+](collectors/python.d.plugin/nginx_plus/)** - connects to multiple nginx_plus servers (local or remote) to collect real-time performance metrics.
- **[PHP-FPM](collectors/python.d.plugin/phpfpm/)** - multiple instances, each reporting connections, requests, performance, etc.
- **[Tomcat](collectors/python.d.plugin/tomcat/)** - accesses, threads, free memory, volume, etc.
- **[web server `access.log` files](collectors/python.d.plugin/web_log/)** - extracting in real-time, web server and proxy performance metrics and applying several health checks, etc.
- **[HTTP check](collectors/python.d.plugin/httpcheck/)** - checks one or more web servers for HTTP status code and returned content.

#### Proxies, Balancers, Accelerators
- **[HAproxy](collectors/python.d.plugin/haproxy/)** - bandwidth, sessions, backends, etc.
- **[Squid](collectors/python.d.plugin/squid/)** - multiple servers, each showing: clients bandwidth and requests, servers bandwidth and requests.
- **[Traefik](collectors/python.d.plugin/traefik/)** - connects to multiple traefik instances (local or remote) to collect API metrics (response status code, response time, average response time and server uptime).
- **[Varnish](collectors/python.d.plugin/varnish/)** - threads, sessions, hits, objects, backends, etc.
- **[IPVS](collectors/proc.plugin/)** - collects metrics from the Linux IPVS load balancer.

#### Database Servers
- **[CouchDB](collectors/python.d.plugin/couchdb/)** - reads/writes, request methods, status codes, tasks, replication, per-db, etc.
- **[MemCached](collectors/python.d.plugin/memcached/)** - multiple servers, each showing: bandwidth, connections, items, etc.
- **[MongoDB](collectors/python.d.plugin/mongodb/)** - operations, clients, transactions, cursors, connections, asserts, locks, etc.
- **[MySQL and mariadb](collectors/python.d.plugin/mysql/)** - multiple servers, each showing: bandwidth, queries/s, handlers, locks, issues, tmp operations, connections, binlog metrics, threads, innodb metrics, and more.
- **[PostgreSQL](collectors/python.d.plugin/postgres/)** - multiple servers, each showing: per database statistics (connections, tuples read - written - returned, transactions, locks), backend processes, indexes, tables, write ahead, background writer and more.
- **[Proxy SQL](collectors/python.d.plugin/proxysql/)** - collects Proxy SQL backend and frontend performance metrics.
- **[Redis](collectors/python.d.plugin/redis/)** - multiple servers, each showing: operations, hit rate, memory, keys, clients, slaves.
- **[RethinkDB](collectors/python.d.plugin/rethinkdbs/)** - connects to multiple rethinkdb servers (local or remote) to collect real-time metrics.

#### Message Brokers
- **[beanstalkd](collectors/python.d.plugin/beanstalk/)** - global and per tube monitoring.
- **[RabbitMQ](collectors/python.d.plugin/rabbitmq/)** - performance and health metrics.

#### Search and Indexing
- **[ElasticSearch](collectors/python.d.plugin/elasticsearch/)** - search and index performance, latency, timings, cluster statistics, threads statistics, etc.

#### DNS Servers
- **[bind_rndc](collectors/python.d.plugin/bind_rndc/)** - parses `named.stats` dump file to collect real-time performance metrics. All versions of bind after 9.6 are supported.
- **[dnsdist](collectors/python.d.plugin/dnsdist/)** - performance and health metrics.
- **[ISC Bind (named)](collectors/node.d.plugin/named/)** - multiple servers, each showing: clients, requests, queries, updates, failures and several per view metrics. All versions of bind after 9.9.10 are supported.
- **[NSD](collectors/python.d.plugin/nsd/)** - queries, zones, protocols, query types, transfers, etc.
- **[PowerDNS](collectors/python.d.plugin/powerdns/)** - queries, answers, cache, latency, etc.
- **[unbound](collectors/python.d.plugin/unbound/)** - performance and resource usage metrics.
- **[dns_query_time](collectors/python.d.plugin/dns_query_time/)** - DNS query time statistics.

#### Time Servers
- **[chrony](collectors/python.d.plugin/chrony/)** - uses the `chronyc` command to collect chrony statistics (Frequency, Last offset, RMS offset, Residual freq, Root delay, Root dispersion, Skew, System time).
- **[ntpd](collectors/python.d.plugin/ntpd/)** - connects to multiple ntpd servers (local or remote) to provide statistics of system variables and optional also peer variables.

#### Mail Servers
- **[Dovecot](collectors/python.d.plugin/dovecot/)** - POP3/IMAP servers.
- **[Exim](collectors/python.d.plugin/exim/)** - message queue (emails queued).
- **[Postfix](collectors/python.d.plugin/postfix/)** - message queue (entries, size).

#### Hardware Sensors
- **[IPMI](collectors/freeipmi.plugin/)** - enterprise hardware sensors and events.
- **[lm-sensors](collectors/python.d.plugin/sensors/)** - temperature, voltage, fans, power, humidity, etc.
- **[Nvidia](collectors/python.d.plugin/nvidia_smi/)** - collects information for Nvidia GPUs.
- **[RPi](collectors/charts.d.plugin/sensors/)** - Raspberry Pi temperature sensors.
- **[w1sensor](collectors/python.d.plugin/w1sensor/)** - collects data from connected 1-Wire sensors.

#### UPSes
- **[apcupsd](collectors/charts.d.plugin/apcupsd/)** - load, charge, battery voltage, temperature, utility metrics, output metrics
- **[NUT](collectors/charts.d.plugin/nut/)** - load, charge, battery voltage, temperature, utility metrics, output metrics
- **[Linux Power Supply](collectors/proc.plugin/)** - collects metrics reported by power supply drivers on Linux.

#### Social Sharing Servers
- **[RetroShare](collectors/python.d.plugin/retroshare/)** - connects to multiple retroshare servers (local or remote) to collect real-time performance metrics.

#### Security
- **[Fail2Ban](collectors/python.d.plugin/fail2ban/)** - monitors the fail2ban log file to check all bans for all active jails.

#### Authentication, Authorization, Accounting (AAA, RADIUS, LDAP) Servers
- **[FreeRadius](collectors/python.d.plugin/freeradius/)** - uses the `radclient` command to provide freeradius statistics (authentication, accounting, proxy-authentication, proxy-accounting).

#### Telephony Servers
- **[opensips](collectors/charts.d.plugin/opensips/)** - connects to an opensips server (localhost only) to collect real-time performance metrics.

#### Household Appliances
- **[SMA webbox](collectors/node.d.plugin/sma_webbox/)** - connects to multiple remote SMA webboxes to collect real-time performance metrics of the photovoltaic (solar) power generation.
- **[Fronius](collectors/node.d.plugin/fronius/)** - connects to multiple remote Fronius Symo servers to collect real-time performance metrics of the photovoltaic (solar) power generation.
- **[StiebelEltron](collectors/node.d.plugin/stiebeleltron/)** - collects the temperatures and other metrics from your Stiebel Eltron heating system using their Internet Service Gateway (ISG web).

#### Game Servers
- **[SpigotMC](collectors/python.d.plugin/spigotmc/)** - monitors Spigot Minecraft server ticks per second and number of online players using the Minecraft remote console.

#### Distributed Computing
- **[BOINC](collectors/python.d.plugin/boinc/)** - monitors task states for local and remote BOINC client software using the remote GUI RPC interface. Also provides alarms for a handful of error conditions.

#### Media Streaming Servers
- **[IceCast](collectors/python.d.plugin/icecast/)** - collects the number of listeners for active sources.

### Monitoring Systems
- **[Monit](collectors/python.d.plugin/monit/)** - collects metrics about monit targets (filesystems, applications, networks).

#### Provisioning Systems
- **[Puppet](collectors/python.d.plugin/puppet/)** - connects to multiple Puppet Server and Puppet DB instances (local or remote) to collect real-time status metrics.

You can easily extend Netdata, by writing plugins that collect data from any source, using any computer language.

---

## Documentation

The Netdata documentation is at [https://docs.netdata.cloud](https://docs.netdata.cloud). But you can also find it inside the repo, so by just navigating the repo on github you can find all the documentation.

Here is a quick list:

Directory|Description
:---|:---
[`installer`](packaging/installer/)|Instructions to install Netdata on your systems.
[`docker`](packaging/docker/)|Instructions to install Netdata using docker.
[`daemon`](daemon/)|Information about the Netdata daemon and its configuration.
[`collectors`](collectors/)|Information about data collection plugins.
[`health`](health/)|How Netdata's health monitoring works, how to create your own alarms and how to configure alarm notification methods.
[`streaming`](streaming/)|How to build hierarchies of Netdata servers, by streaming metrics between them.
[`backends`](backends/)|Long term archiving of metrics to industry standard time-series databases, like `prometheus`, `graphite`, `opentsdb`.
[`web/api`](web/api/)|Learn how to query the Netdata API and the queries it supports.
[`web/api/badges`](web/api/badges/)|Learn how to generate badges (SVG images) from live data.
[`web/gui/custom`](web/gui/custom/)|Learn how to create custom Netdata dashboards.
[`web/gui/confluence`](web/gui/confluence/)|Learn how to create Netdata dashboards on Atlassian's Confluence.

You can also check all the other directories. Most of them have plenty of documentation.

## Community

We welcome [contributions](CONTRIBUTING.md). So, feel free to join the team.

To report bugs, or get help, use [GitHub Issues](https://github.com/netdata/netdata/issues).

You can also find Netdata on:

- [Facebook](https://www.facebook.com/linuxnetdata/)
- [Twitter](https://twitter.com/linuxnetdata)
- [OpenHub](https://www.openhub.net/p/netdata)
- [Repology](https://repology.org/metapackage/netdata/versions)
- [StackShare](https://stackshare.io/netdata)

## License

Netdata is [GPLv3+](LICENSE).

Netdata re-distributes other open-source tools and libraries. Please check the [third party licenses](REDISTRIBUTED.md).

## Is it any good?

Yes.

*When people first hear about a new product, they frequently ask if it is any good. A Hacker News user [remarked](https://news.ycombinator.com/item?id=3067434):*

> Note to self: Starting immediately, all raganwald projects will have a “Is it any good?” section in the readme, and the answer shall be “yes.".

So, we follow the tradition...

## Is it awesome?

[These people](https://github.com/netdata/netdata/stargazers) seem to like it.

---
title: Ship system metrics via Telegraf
logo:
  logofile: telegraf-logo-preview.svg
  orientation: vertical
data-source: System metrics over Telegraf
templates: ["docker"]
contributors:
  - daniel-tk
  - nshishkin
shipping-tags:  
  - prometheus
order: 800
---


## Overview

Telegraf is a plug-in driven server agent for collecting and sending metrics and events from databases, systems and IoT sensors.

To send your Prometheus-format System metrics to Logz.io, you need to add multiple system-related inputs and **outputs.http** plug-ins to your Telegraf configuration file.

#### Configuring Telegraf to send your metrics data to Logz.io

<div class="tasklist">

##### Set up Telegraf v1.17 or higher

On Windows:

{% include metric-shipping/telegraf-setup-win.md %}

On MacOS:

{% include metric-shipping/telegraf-setup-mac.md %}

On Linux:

{% include metric-shipping/telegraf-setup-linux.md %}

##### Add the inputs plug-in

First you need to configure the input plug-in to enable Telegraf to scrape the PostgreSQL data from your hosts. To do this, add the following code to the configuration file:


``` ini
[[inputs.cpu]]
  # Whether to report per-cpu stats or not
  percpu = false
  
  # Whether to report total system cpu stats or not
  totalcpu = true
  
  # If true, collect raw CPU time metrics.
  collect_cpu_time = true
  
  # If true, compute and report the sum of all non-idle CPU states.
  report_active = true
  
[[inputs.mem]]
[[inputs.system]]
[[inputs.disk]]
  ignore_fs = ["tmpfs", "devtmpfs", "devfs", "iso9660", "overlay", "aufs", "squashfs"]
[[inputs.diskio]]
[[inputs.net]]
[[inputs.processes]]
```

<!-- info-box-start:info -->
The full list of data scraping and configuring options can be found [here](https://docs.influxdata.com/telegraf/v1.18/plugins/).
{:.info-box.note}
<!-- info-box-end -->

##### Add the outputs.http plug-in

{% include metric-shipping/telegraf-outputs.md %}
{% include general-shipping/replace-placeholders-prometheus.html %}

##### Check Logz.io for your metrics

Give your data some time to get from your system to ours, then log in to your Logz.io Metrics account, and open [the Logz.io Metrics tab](https://app.logz.io/#/dashboard/metrics/).


</div>
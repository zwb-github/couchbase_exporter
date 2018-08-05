Couchbase Exporter
==================

[![Build Status](https://travis-ci.org/blakelead/couchbase_exporter.svg?branch=master)](https://travis-ci.org/blakelead/couchbase_exporter) [![Coverage Status](https://coveralls.io/repos/github/blakelead/couchbase_exporter/badge.svg?branch=master)](https://coveralls.io/github/blakelead/couchbase_exporter?branch=master) [![Release](https://img.shields.io/badge/release-0.1.0-blue.svg)](https://github.com/blakelead/couchbase_exporter/releases/latest) [![Software License](https://img.shields.io/badge/license-MIT-green.svg)](/LICENSE.md)

Expose metrics from *Couchbase Community 4.5.1* cluster for consumption by Prometheus.

> WIP: each release will introduce new metrics and probably lots of breaking changes.

Getting Started
---------------

Run from terminal:

```bash
./couchbase_exporter [flags]
```

Available flags:

| argument            | description                                | default               |
|---------------------|--------------------------------------------|-----------------------|
| -web.listen-address | The address to listen on for HTTP requests | :9191                 |
| -web.telemetry-path | Path under which to expose metrics         | /metrics              |
| -db.url             | The address of Couchbase cluster           | http://localhost:8091 |
| -db.user            | The administrator username                 | admin                 |
| -db.pwd             | The administrator password                 | password              |
| -help               | Command line help                          |                       |

Metrics
-------

| name                                      | description                             |
|-------------------------------------------|-----------------------------------------|
| cb_up                                     | State of last cluster scrape            |
| cb_node_status                            | Status of couchbase node                |
| cb_node_cluster_membership                | Status of node cluster membership       |
| cb_node_cpu_utilization_rate              | CPU utilization rate                    |
| cb_node_ram_usage_bytes                   | RAM used per node in bytes              |
| cb_cluster_ram_total_bytes                | Total RAM in the cluster                |
| cb_cluster_ram_used_bytes                 | Used RAM in the cluster                 |
| cb_cluster_ram_used_by_data_bytes         | Used RAM by data in the cluster         |
| cb_cluster_ram_quota_total_bytes          | Total quota RAM in the cluster          |
| cb_cluster_ram_quota_total_per_node_bytes | Total quota RAM per node in the cluster |
| cb_cluster_ram_quota_used_bytes           | Used quota RAM in the cluster           |
| cb_cluster_ram_quota_used_per_node_bytes  | Used quota RAM per node in the cluster  |
| cb_cluster_disk_total_bytes               | Total disk in the cluster               |
| cb_cluster_disk_quota_total_bytes         | Disk quota in the cluster               |
| cb_cluster_disk_used_bytes                | Used disk in the cluster                |
| cb_cluster_disk_used_by_data_bytes        | Disk used by data in the cluster        |
| cb_cluster_disk_free_bytes                | Free disk in the cluster                |
| cb_cluster_fts_ram_quota_bytes            | RAM quota for Full text search bucket   |
| cb_cluster_index_ram_quota_bytes          | RAM quota for Index bucket              |
| cb_cluster_data_ram_quota_bytes           | RAM quota for Data bucket               |

Author Information
------------------

Adel Abdelhak
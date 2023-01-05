# cyberdinge.prometheus

This will be the description of the role

## Requirements

a,b und c

https://relabeler.promlabs.com/

## Defaults

``` YAML title="defaults/main.yaml"
--8<-- "./prometheus/defaults/main.yaml"
```


## Scrape config

### Static

``` YAML
---

- labels:
    job: job_name
    domain: something_something
  targets:
  - "targeturl"
```

## promtool

### check config

``` BASH
promtool check config /etc/prometheus/prometheus.yml
docker compose exec prometheus promtool check config /etc/prometheus/prometheus.yml
```


### delete a series

``` BASH
curl -X POST -g 'http://localhost:9090/api/v1/admin/tsdb/delete_series?match[]={instance="sbcode.net:9100"}'
```
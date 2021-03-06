# dnsdrone

dnsdrone is a testing tool that creates an on going load of DNS queries on a server.

It produces metrics via Prometheus.

## Usage

```
Usage of ./dnsdrone:
  -delay duration
        Time to wait before sending queries
  -local-resolver
        Use local resolver (default true)
  -names string
        Comma separated list of hostnames
  -prom string
        Prometheus endpoint (default ":9696")
  -qps int
        DNS queries per second (default 1)
  -timeout duration
        Timeout for DNS queries (for non-local resolver) (default 5s)
  -verbose
        Verbose log output

```

## Metrics

* *dnsdrone_request_count_total*: Counter of DNS requests sent
* *dnsdrone_response_count_total{rcode}*: Counter of DNS responses
* *dnsdrone_response_lost_count_total*: Counter of DNS responses lost
* *dnsdrone_request_duration_seconds*: Histogram of the time (in seconds) each request took

Prometheus

const apiMetrics = require('prometheus-api-metrics');

app.use(apiMetrics({
  metricsPrefix: 'api_metrics',
  durationBuckets: [0.001, 0.005, 0.015, 0.05, 0.1, 0.2, 0.3, 0.4, 0.5],
  requestSizeBuckets: [5, 10, 25, 50, 100, 250, 500, 1000, 2500, 5000, 10000],
  responseSizeBuckets: [5, 10, 25, 50, 100, 250, 500, 1000, 2500, 5000, 10000]
}));

About Prom Client

Counter - It only goes up (and resets), counts something. e.g, the number of requests served, tasks completed, or errors.
Gauge - It goes up and down, snapshot of state. e.g, temperatures or current memory usage, etc
Summary - It samples observations, espeically over a sliding time window. e.g, rate(http_request_duration_seconds_sum[5m])
Histogram - It samples observations and counts them in configurable buckets.

Build Up a Query

avg(api_metrics_http_request_size_bytes_bucket)
count(api_metrics_http_request_size_bytes_bucket)
sum(api_metrics_http_request_size_bytes_bucket)
sum(api_metrics_http_request_size_bytes_bucket{route="/users"})
rate(api_metrics_http_request_duration_seconds_bucket{route="/users"}[1h])
histogram_quantile(0.50, rate(api_metrics_http_request_duration_seconds_bucket[30m]))
avg(api_metrics_http_request_duration_seconds_count) by (route)

Challenges

Median Response Time for Creating Users

histogram_quantile(0.50, rate(api_metrics_http_request_duration_seconds_bucket{method="POST",route="/users"}[10m])) by (le)

95th Response Time by specific route and status code

histogram_quantile(0.95, sum(rate(api_metrics_http_request_duration_seconds_bucket{route="/conferences", code="201"}[10m])) by (le))

Apdex for Conferences Endpoint

sum(rate(api_metrics_http_request_duration_seconds_bucket{route="/conferences", code="201", le="0.1"}[1h]))
+ (sum(rate(api_metrics_http_request_duration_seconds_bucket{route="/conferences", code="201", le="0.5"}[1h]) / 2)) / sum(rate(api_metrics_http_request_duration_seconds_count{route="/conferences", code="201"}[1h]))

Alert Manager

Trigger an alert by killing the app!

Add an alert, we know about expressions

 - alert: 404 Status Codes
    expr: count({code="404"}) > 0
    for: 1m
    labels:
      severity: warning
    annotations:
      summary: "404 Status Codes"
      description: "job {{$labels.job}} has returned 404 errors."

Alert Challenge!

Setting Your Normal Exercise



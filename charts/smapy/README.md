This chart installs [SMApy](https://github.com/jonkerj/smapy) on your k8s
cluster using Helm. You'll need to provision just a couple of things:

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| config.sma.url | string | https://sma.home.lan | URL to web interface of SMA inverter |
| config.sma.group | string | usr | Username. Either `usr` or `inst` |
| config.influxdb | object |  | key value pairs passed to `InfluxDBClient`. See [Python docs](https://influxdb-python.readthedocs.io/en/latest/api-documentation.html#influxdbclient) |
| config.tags | object |  | tags to put on points submitted to Influx |
| config.interval | int | 30 | interval between two measurements |
| secrets | object | | object that's going to be merged with `config`, but stored in a `Secret` |
| secrets.sma.password | string |  | Password in SMA web UI |

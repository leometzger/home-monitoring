# Networks Monitoring

The data is collected by **nProbe**, and is stored into influxdb for
further queries and visualization. 

It has a grafana container. If you want to create a dashboard and visualize
influx data. It has not a built-in dashboard.

## Documentations

* [ntopng](https://www.ntop.org/guides/ntopng/);
* [nProbe](https://www.ntop.org/guides/nprobe/)
* [influxdb](https://docs.influxdata.com/influxdb/v2.0/)

## nProbe (sensor) Configuration

To collect data, install nprobe and run the following command:

```
nprobe --zmq "tcp://<ip address of ntopng>:5556" --zmq-probe-mode -i eno1 -n none -T "@NTOPNG@"
```

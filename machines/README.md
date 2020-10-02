# Home Monitoring

This repository contains a `docker-compose` based host-monitoring monitoring for your home/lab. 
Creates a dashboard to monitor devices on your network using 
`prometheus` and `grafana`.

## Pre Requisites 

- [Docker](https://docs.docker.com/get-docker/) installed;


## Usage

Clone the repository

```
git clone https://github.com/leometzger/home-monitoring
```

Change grafana password by modifying `secrets.env`

Run `docker-compose`

```
docker-compose-up -d
```

### Configuring Prometheus

Change `prometheus/prometheus.yml` on `node_exporter` section and add your IP to it.

* (It is recommended to have reserved DHCP IP for your host)

### Configuring Grafana

After that it is necessary configure your dashboard on grafana.

Open grafana accessing `localhost:3000`.

Configure the datasource and dashboard.

![Creating Datasource](https://user-images.githubusercontent.com/15220162/88278358-9c817500-ccb8-11ea-9e4a-d2ed09884b0a.gif)

Import dashboard of your preference. [(Dashboards)](https://grafana.com/grafana/dashboards)


![Importing Dashboard](https://user-images.githubusercontent.com/15220162/88282491-0e10f180-ccc0-11ea-896a-5508ba81cbc6.gif)


After that you can monitor your PC on grafana. =)

## Other devices

To monitor other devices of your network, you need to install [Node Exporter] on them and 
add the IP address on `prometheus/prometheus.yml` file and make sure that port `9100` is open.


## License

MIT
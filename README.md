# Monitoring

This repository contains a set of `docker-compose` projects that aims monitor your environment. 

All Projects follow the same rules. You need to install a sensor or agent
where you want to monitor, and then run the project with `docker-compose`.
Specific instructions may be finded at specific `README` in the folders.

## Pre Requisites 

- [Docker](https://docs.docker.com/get-docker/) installed;

## Projects

* **Machines**: Monitoring devices and machines of your environment. It can be visualized
using grafana dashboards;
* **Networks**: Monitor your networks and store the data into a timeseries database.

## Usage

Clone the repository

```
git clone https://github.com/leometzger/home-monitoring
```

Enter in directory `machines` or `networks`.

Run `docker-compose`

```
docker-compose-up -d
```

## License

MIT
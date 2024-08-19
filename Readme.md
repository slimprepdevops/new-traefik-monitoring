## Traefik Monitoring System

- features
    - three apps
    - traefik
    - prometheus
    - grafana
    - cadvisor
    - alertmanager
    - node-exporter

- setup requirements
    - install docker and docker-compose
    - from `/traefik/letsencrypt` change the permissions for the `acme.json` file : `chmod 600 acme.json`
    - create a docker network called `proxy` : `docker network create proxy`
    - replace all the `*.c4.slimprepdevops.com` with your domain name
    - update `/prometheus/prometheus.yml` line 41 with the IP of the server where `docker-deamon` has been enabled (see notion notes for how to enable deamon metrics)
    - update `/alertmanager/alertmanager.yml` with the credentials of an email provider you have access to
    - run `docker-compose up -d` for `/traefik` first then do same for other folders



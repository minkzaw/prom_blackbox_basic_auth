# prom_blackbox_basic_auth
Testing purpose for prometheus and blackbox secure connection

# Blackbox exporter
Use basic auth by itself to avoid unauthorized access from using the blackbox exporter and prevent the scraping.
### Configuration
Declare credential under prom/bb_config/web.yml and use it as ['--web.config-file'] command while initializing the blackbox exporter service can be found under docker-compose.


# Prometheus
Prometheus then request to blackbox exporter with basic auth and blackbox exporter then grant the access to pull its scrape from the authenticated prometheus server.
### Configuration
Define credential under prom/prom_config/prometheus.yml as ['basic-auth'].


# Generating password to use in basic auth
htpasswd -nBC 10 "" | tr -d ':\n'

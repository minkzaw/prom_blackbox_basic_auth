# prom_blackbox_basic_auth
Testing purpose for prometheus and blackbox secure connection

# Blackbox exporter
Use basic auth by itself to avoid unauthorized access from using the blackbox exporter and prevent the scraping.
## Configuration



# Prometheus
Prometheus then request to blackbox exporter with basic auth and blackbox exporter then grant the access to pull its scrape from the authenticated prometheus server.



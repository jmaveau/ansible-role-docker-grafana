# ansible-role-docker-grafana
Ansible role with grafana container and Diamond dashboards

# Directories
- `/var/lib/grafana` - data directory

# Ports
Grafana exposed port 3000

# Dashboards
- Carbon - basic stats from carbon-cache
- Days - common metrics for last 4 days
- Disk - iostats for each disk (templated)
- Drupal - some drupal metrics from [Drupal statsd module](https://www.drupal.org/project/statsd)
- Drupals - some metrics about drupals from drupal-table
- Site - metrics from drupal-table for one site (templated)
- System - common system metrics

# TODO
- [ ] grafana api key add
- [ ] grafana password set up
- [ ] grafana not creates dashboards, only updates, need to set id: null, http://docs.grafana.org/reference/http_api/ or import dashboards manually first-time
- [ ] modified dashboards has status 'success' instead of 'changed'
- [ ] container duplicates! ansible creates duplicate containers without name and outputs error: "Docker API Error: Cannot start container d77686b3ab769db11aa702e6dd43659e4f1851d7bb809c681665acfd92eb5ac9: Cannot find child for /grafana" 
- [ ] ansible docker runner from hexlet.io - http://habrahabr.ru/company/hexlet/blog/258815/ 
- [ ] nginx site setup

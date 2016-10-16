# Floodlight controller
[![](https://images.microbadger.com/badges/image/glefevre/floodlight.svg)](https://microbadger.com/images/glefevre/floodlight "Get your own image badge on microbadger.com") [![](https://images.microbadger.com/badges/version/glefevre/floodlight.svg)](https://microbadger.com/images/glefevre/floodlight "Get your own version badge on microbadger.com")

*(SDN Openflow Controller)*

Floodlight is an OpenFlow controller, usefull to control and orchestrate network of switches that speak the openflow protocol on your infrastructure.

Floodlight is traditionally used in conjunction with applications on top of it (Openstack Neutron, others...)

[Floodlight Home](http://www.projectfloodlight.org/floodlight/)
[Floodlight Documentation](https://floodlight.atlassian.net/wiki/display/floodlightcontroller/Floodlight+Documentation)

## Supported tags
- latest

## What's inside ?
- Based on anapsix/alpine-java:8_jdk
- Firewall and forwarding module
- Exposed port 6653 (Openflow) and 8080 (WebUI/REST api)

## How to use it ?
### Run container
`docker run -d -p 6653:6653 -p 8080:8080 --name=floodlight glefevre/alpine-floodlight`

### Call firewall API
`curl http://localhost:8080/wm/firewall/module/status/json` 
See [Firewall REST API](https://floodlight.atlassian.net/wiki/display/floodlightcontroller/Firewall+REST+API)

### Access Web interface
`http://localhost:8080/ui/pages/index.html ` 



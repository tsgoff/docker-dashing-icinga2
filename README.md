docker-dashing-icinga2
========

https://github.com/Icinga/dashing-icinga2
https://registry.hub.docker.com/u/bios/docker-dashing-icinga2/  

**Docker image to start dashing-icinga2**

Quickstart
----------

    docker run --name dashingicinga2 -d bios/docker-dashing-icinga2

Options
-------
 - ICINGA2_API_HOST="icingahost" 
 - ICINGA2_API_USERNAME="username" 
 - ICINGA2_API_PASSWORD="apipw" 
 - ICINGA2_API_NODENAME="hostname" 
 - ICINGAWEB2_URL="icingaweb2" 

Example
-------
Mount config file and define custom port

    docker run --name dashingicinga2 -d \
    -v /data/icinga2.erb:/usr/share/dashing-icinga2/dashboards/icinga2.erb \
    -e ICINGA2_API_HOST="icingahost" \
    -e ICINGA2_API_USERNAME="user" \
    -e ICINGA2_API_PASSWORD="apipw" bios/docker-dashing-icinga2


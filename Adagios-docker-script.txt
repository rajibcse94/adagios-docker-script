

# ubuntu_adagios_docker_script
version: '3'
services:
  nagios:
    image: ethnchao/nagios:latest
    container_name: nagios
    restart: always
    ports:
     - 8081:80
    environment:
     - NAGIOSADMIN_USER=nagiosadmin
     - NAGIOSAMDIN_PASS=nagios
     - NAGIOS_TIMEZONE=Asia/Dhaka
    volumes:
    - /root/nagios-docker-03/nagiosetc:/opt/nagios/etc
    - /root/nagios-docker-03/nagiosvar:/opt/nagios/var
    - /root/nagios-docker-03/customplugins:/opt/Custom-Nagios-Plugins
    - /root/nagios-docker-03/nagiosgraphvar:/opt/nagiosgraph/var
    - /root/nagios-docker-03/nagiosgraphetc:/opt/nagiosgraph/etc
volumes:
    nagiosetc:
    nagiosvar:
    customplugins:
    nagiosgraphvar:
    nagiosgraphetc:

# mkdir -p /root/nagios-docker-03/nagiosetc /root/nagios-docker-03/nagiosvar /root/nagios-docker-03/customplugins /root/nagios-docker-03/nagiosgraphvar /root/nagios-docker-03/nagiosgraphetc

# vim docker-compose.yaml
# docker-compose down && docker-compose up
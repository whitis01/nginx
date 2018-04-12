FROM haproxy:latest

COPY haproxy.cfg /usr/local/etc/haproxy/haproxy.cfg

CMD export DOCKER_HOST=$(/sbin/ip route | awk '/default/ { print $3 }') && haproxy -f /usr/local/etc/haproxy/haproxy.cfg

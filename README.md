# netcatrelay
Containerized netcat relay
launch container with docker run -d --rm -p 192.168.1.25:65534:65534 netcat /bin/sh -c /backdoor.sh, or just comment out that line entirely and just run 'docker run -d --rm -p <forwardinghost>:port:port /bin/sh -c 'nc -l -p 11111 0<backpipe | nc 192.168.1.201 55555 | tee backpipe' at the commandline. Maybe one day I'll use ncat and encryption. Whatever.

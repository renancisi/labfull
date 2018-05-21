# labfull

To use the proposed test I left a hosts file containing an ec2 with dns lab01.omnitask.com.br, credentials inside the file.

Default call: "ansible-playbook site.yml -i hosts"

- For the build module I made a fork of the ansistrano project (https://github.com/ansistrano/deploy);
- For the LB module, I created a cluster with node doing LB according to the limit of available CPUs in the environment having a nginx doing 80: 3000 reverse proxy;
- To guarantee the availability of service I used the monit monitoring the PIDs of the node / nginx
- For load testing I have created a simple script to handle siege output
- For the log parse has been configured a logrotate for web / load test

## Internal Domain Resolution
Local DNS resolution is carried out through Nginx Proxy Manager instead of Pi-hole. By adding a Type A DNS record for the domain which points to the Nginx LXC container IP address, alongside wildcard CNAME records in Nginx, internal service domains can be resolved locally without exposing ports to the internet.
## Pi-hole DNS Filtering
The pfSense router explicitly uses the Pi-hole service for DNS resolution, ensuring that user requests are filtered against blocked domains accordingly. Pi-hole provides network-wide DNS filtering and currently blocks over 7 million domains across configured blocklists.

# Deploying a site
## programs used
- cloudflare: DNS control
- digitalocean 
- run cloud, intermediary for digital ocean, GUI tools to make it easer

## DNS STUFF
1. On runcloud we grab the ip address, then do to the cloud flare. 
2. Have cloudflare set up well in advance. 
3. You have an ip address, servers will assign you an IP address. Sometimes services give you an ip address but they don’t want you to use it so instead of pointing it to IP address, point it to a domain which may be another record which is like CNAME. 

If the A record is pointing to an IP address, and later something happens and if something happens it will crash the site. If you have a CNAME this is will be able to point to a domain which will be able to act as a backup. 

## SSL 
1. 
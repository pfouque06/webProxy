##lecture:  

    https://dolphinandmermaids.com/blog/docker-nginx-letsencrypt  

###letsencrypt companion twiki :  
    https://github.com/nginx-proxy/docker-letsencrypt-nginx-proxy-companion/wiki   

###Force certificates renewal:  
If needed, you can force a running letsencrypt-nginx-proxy-companion container to renew all certificates that are currently in use with the following command:  

    $ docker exec nginx-letsencrypt /app/force_renew  

###Manually trigger the service loop:  
You can trigger the execution of the service loop before the hourly execution with:  
Unlike the previous command, this won't force renewal of certificates that don't need to be renewed.  

    $ docker exec nginx-letsencrypt /app/signal_le_service  

###Show certificates informations  
To display informations about your existing certificates, use the following command:   

    $ docker exec nginx-letsencrypt /app/cert_status  

#### also :  
  https://medium.com/swlh/dockerizing-two-web-servers-to-respond-to-the-same-domain-eb9c15734a68  
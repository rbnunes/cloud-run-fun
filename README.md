# Cloud Run Fun

Cloud Run Fun is a drawer of small projects I'm playing with using Cloud Run.

## /nginx: Editable nginx 

Docker image running nginx which loads it's config from a $CONFIG enviroment variable. This allows for quick edits and iterative config development in Cloud Run without rebuilding a new Docker image each time.

Container: [`gcr.io/cloud-run-fun/nginx`](https://gcr.io/cloud-run-fun/nginx)

[![Run on Google Cloud](https://deploy.cloud.run/button.svg)](https://console.cloud.google.com/run/create?image=gcr.io%2Fcloud-run-fun%2Fnginx:latest)

For more info, see this blogpost: https://dev.to/bamnet/dynamic-nginx-config-on-cloud-run-hpc.

Obs:
I did this fork to enable a bigger config on ngnix and pass just the url to proxy

I also tryed other ways to redirect to try to make this compatible with ngrok
like
#rewrite ^/(.*)$ http://www.domain2.com/$1 redirect;  alte
#return  308 https://$server_name$request_uri;
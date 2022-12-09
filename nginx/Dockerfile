FROM nginx
RUN rm /etc/nginx/conf.d/default.conf
COPY site.template /etc/nginx/conf.d/site.template
CMD /bin/bash -c "envsubst '\$CONFIG' < /etc/nginx/conf.d/site.template > /etc/nginx/conf.d/site.conf && cat /etc/nginx/conf.d/site.conf && exec nginx -v -g 'daemon off;'"

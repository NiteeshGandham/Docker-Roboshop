FROM nginx:1.24.0
RUN rm -rf /usr/share/nginx/html/html.index
RUN rm -rf /usr/share/nginx/html/nginx.conf
COPY content /usr/share/nginx/html/
COPY nginx.conf /usr/share/nginx/html/


FROM wordpress:latest

EXPOSE 80

# Set workdir
WORKDIR /var/www/html

# Copy php uploads config file
COPY ./wordpress/uploads.ini /usr/local/etc/php/conf.d/uploads.ini

# Copy wordpress content
COPY ./wordpress/starter_content/plugins /usr/src/wordpress/wp-content/plugins
COPY ./wordpress/startercontent/themes /usr/src/wordpress/wp-content/themes

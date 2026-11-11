
FROM httpd:latest

# Copy application files
COPY index.html /usr/local/apache2/htdocs/

# Copy security configuration
COPY security.conf /usr/local/apache2/conf/extra/security.conf

# Enable Apache headers module and include security config
RUN sed -i 's/^#LoadModule headers_module/LoadModule headers_module/' /usr/local/apache2/conf/httpd.conf \
    && echo 'Include conf/extra/security.conf' >> /usr/local/apache2/conf/httpd.conf

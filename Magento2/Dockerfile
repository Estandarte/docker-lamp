FROM estandarte/lamp:latest

RUN apt-get update \
   && apt-get install -y php5-mysql \
   && apt-get install -y libxml2-dev \
       && apt-get install -y php-soap \
   && apt-get install -y libmcrypt4 libmcrypt-dev \
       && apt-get install -y php5-mcrypt \
   && apt-get install -y libxslt-dev \
       && apt-get install -y php5-xsl \
   && apt-get install -y libicu-dev \
       && apt-get install -y php5-intl \
   && apt-get install -y libpng12-dev libjpeg-dev \
       && apt-get install -y php5-gd \
   && apt-get install -y zlib1g-dev \
   && apt-get install -y curl \
   && apt-get install -y php5-curl \
   && apt-get install -y nano \
   && rm -rf /var/lib/apt/lists/*

RUN a2enmod headers

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www
RUN rm -rf /var/www/html && ln -s /magento/pub /var/www/html

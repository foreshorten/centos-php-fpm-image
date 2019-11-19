This is a CentOS 7 image with php-fpm installed and running on port 9000.   It is designed as a parent image for subsequent images therefore using CMD and not ENTRYPOINT.  This image executes php-fpm with the following exec parameters and stops clean with exit 0 and SIGINIT:

> CMD ["php-fpm", "--allow-to-run-as-root", "--nodaemonize"]

## RUN:

    $ docker run --rm -it -p 9000:9000 foreshorten/centos7-php-fpm-image:php54


## Builds:

There are currently 6 builds with Tags of  the following:
 - php54
 - php56
 - php70
 - php72
 - php73
 - php74

## PHP Modules:

The following php modules installed: 

**NOTE:** php-sqlsrv not installed in php54 or php56

 - php-fpm 
 - cli
 - gd 
 - intl 
 - ldap 
 - mbstring 
 - mcrypt 
 - opcache 
 - pdo-dblib 
 - soap 
 - xml 
 - gmp
 - bcmath 
 - mhash 
 - xsl 
 - pear 
 - soap 
 - sqlsrv   (only installed on php70 and up)
 - tidy 
 - pecl-uuid 
 - pecl-zip 
 - pecl-imagick 
 - pecl-apcu

Keep in mind, the Dockerfile won't show all the packages installed since some are installed as a dependency,  i.e. php-common, php-cli.  To see php packages installed you can use the following Linux command:

    $ docker run --rm -it  -p 9000:9000  foreshorten/centos7-php-fpm-image:php54 rpm -qa | grep php



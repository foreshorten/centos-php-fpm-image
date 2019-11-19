# centos-php-fpm-image
This is a CentOS 7 image with php-fpm installed and running on port 9000.   It is designed as a parent image for subsequent images therefore using CMD and not ENTRYPOINT.  This image executes php-fpm with the following exec parameters and stops clean with exit 0 using SIGINIT:

> CMD ["php-fpm", "--allow-to-run-as-root", "--nodaemonize"]

There are currently 6 Tags/builds of php54, php56, php70, php72, php73 and php74, each has the following php modules installed: 
**NOTE:** php-sqlsrv not installed in php54 or php56
 - fpm 
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


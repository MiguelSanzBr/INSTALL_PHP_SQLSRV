<pre>
sudo su
apt -y install gcc make php-pear php$(php -v | tr -d '\n' | cut -d' ' -f2 | cut -c1-3)-pdo php-dev build-essential unixodbc-dev;
pecl channel-update pecl.php.net; 
pecl install sqlsrv pdo_sqlsrv; 
echo 'extension=pdo_sqlsrv.so' > /etc/php/$(php -v | tr -d '\n' | cut -d' ' -f2 | cut -c1-3)/mods-available/pdo_sqlsrv.ini; 
echo 'extension=sqlsrv.so' > /etc/php/$(php -v | tr -d '\n' | cut -d' ' -f2 | cut -c1-3)/mods-available/sqlsrv.ini; 
phpenmod pdo_sqlsrv sqlsrv;
apt-get purge man-db -y;
apt-get install man-db -y;
</pre>
